---
title: "Integrate your iOS app with the client-side SDK for user notifications"
description: "Integrate your iOS app with user notifications client SDK."
localization_priority: Priority
ms.prod: "Microsoft Graph notifications"
---
[!NOTE] 
If you're using the Rome SDK, you should follow instructions on the Rome SDK github site: https://github.com/microsoft/project-rome.

# Integrate your iOS app with the client-side SDK for user notifications

After you [register your app](notifications-integration-app-registration.md) in the Azure Portal and onboard your [cross-device experiences](notifications-integration-cross-device-experiences-onboarding.md) in the Partner Dev Center, the next step is to integrate your client app with the client-side SDK foriOS apps.  

With the client-side SDK, your app can perform the necessary registration steps to start receiving notifications published from your app server targeted at the user who is currently signed in. The SDK then manages the notifications on the client side, including receiving new incoming notifications, managing the state of notifications to achieve scenarios like universal dismiss, and retrieving full notification history. 

## New incoming notification flow

For receiving new incoming notifications, the data flow is shown in the following diagram.

![New notification flow for iOS app](images/notifications-new-notification-ios.png)

The process involves a few components:

* App server - The back end of your application
* App client - The front end of your application (a UWP app, an Android app, or an iOS app)
* Microsoft Graph notifications - The service component that enables user notifications to be published, stored, and synced across different instances of app clients across devices and platforms
* APNs - The Apple Push Notification Service provided by Apple for iOS apps. Microsoft Graph notifications use this service to signal the iOS app clients about user notification data changes.  

The diagram shows the following steps: 

1. Application logic. This step captures what triggers the notification to be published to the user. This is app-specific logic, and can be an event or data update about something else in Microsoft Graph, such as a new calendar event or task assignment, or else your app service wants to notify the user about.
2. The app server publishes a notification to the targeted user via the Microsoft Graph notifications API. For more details, see [server side integration](notifications-integrating-app-server.md).
3. On receiving the web request containing the new notification, Microsoft Graph notifications persists the content of the notification securely in the cloud for this app and this user.
4. For each app client instance subscribing to receive notifications for this user, Microsoft Graph notifications sends a signal to notify the app client, via the native push service provided by the operating system. In this case, the application is an iOS app, and it uses [APNs background update notification] to send the signal. 
5. After the application is signaled by the incoming push notification, it asks the SDK to fetch for the changes in the user notification store. 
6. The SDK establishes a secure and compliant connection with the user notifications store in Microsoft Graph.
7. The SDK gets the data changes - in this case, the new notification contents. 
8. The SDK fires event callbacks to notify the app after the changes are successfully retrieved. 
9. Application logic. This step captures what your app chooses to do inside the event callback. Usually, this results in local app data changes and local UI updates. In this case,  the app usually constructs an iOS alert to notify the user about the notification contents.

## Notification update flow

One of the main benefits for using Microsoft Graph notifications is that it persists notifications in the cloud securely and turns them into a stateful resource type. Therefore, it can help your application to manage and sync the correct state of the notifications across different devices for the same signed in user in a cross-device scenario. When a notification is marked as dismissed, or marked as read on one device, the other devices can be notified in real-time. "Handled once, dismissed everywhere" can become a true promise as part of the notification experience for your users. 

The following diagram shows the data flow for changing the state of a notification or deleting the notification on one device, and receiving/handling the state change or the deletion on another device.

![Update notification flow for iOS app](images/notifications-notification-update-ios.png)

Notice that the second part of the flow is similar to the flow for handling new incoming notifications. This is by design - the  programming pattern of the SDK is designed so that the application client can handle all types of user notification data changes (new incoming notifications, notification state changes, notification deleted) in a similar way.  

The diagram shows the following steps:

1. Application logic. Something triggers the notification to be changed or deleted. In general, any event can trigger a notification to change. 
2. App calling into the client SDK to update or delete a notification. Currently, we expose two properties regarding state changes - **userActionState** and **readState** - but your application can define these states and when they need to be updated. For example, when a user dismisses the notification popup, you can update the **userActionState** to be Dismissed. When a user clicks the notification popup and launches the app to consume corresponding app content, you can update the **userActionState** to be Activated and update the **readState** to be Read. 
3. After the corresponding API is called to update or delete a notification, the SDK will call into the user notification store in the cloud in order to fan-out this change to the other app client instances with the same signed in user. 
4. On receiving the update/delete request from a client, Microsoft Graph notifications will update the notification store, and identify the other app client instances that subscribed to this change.
5. For each app client subscription, Microsoft Graph notifications sends a signal to notify the app client, via the native push service provided by the operating system. In this case, this is an iOS, and it uses [APNs background update notification](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html#//apple_ref/doc/uid/TP40008194-CH10-SW8) to send the signal. 
6. After the application is signaled by the incoming push notification, it asks the SDK to fetch for the changes in the user notification store. 
7. The SDK establishes a secure and compliant connection with the user notifications store in Microsoft Graph.
8. The SDK gets the data changes - in this case, the changes are notification state updates or notification deletions. 
9. The SDK fires event callbacks to notify the app after the changes are successfully retrieved. 
10. Application logic. This step captures what your app chooses to do inside the event callback. Usually, this results in local app data changes and local UI updates. In this case, because there are notification updates, the app should update the UI locally to reflect the state change. For example, if a notification is marked as activated, you can remove the corresponding alert UI inside the iOS notification center to achieve "handled once, dismissed everywhere". 

For more information about Microsoft Graph notifications, see [Microsoft Graph Notifications overview](notifications-concept-overview.md). For more information about the steps required to integrate with Microsoft Graph notifications from end to end, see Microsoft Graph notifications [integration overview](notifications-integration-e2e-overview.md).

## Adding the SDK to your project

The simplest way to add the lightweight client SDK to your iOS app is by using the [CocoaPods](https://cocoapods.org/) dependency manager. Go to your iOS project's *Podfile* and insert the following entry:

```ObjectiveC
platform :ios, "10.0"
workspace 'iOSSample'

target 'iOSSample' do
  # Uncomment the next line if you're using Swift or would like to use dynamic frameworks
  # use_frameworks!

	pod install 'microsoft/user-notifications-client'

  # Pods for iOSSample
```

> [!NOTE]
> In order to consume CocoaPod, you must use the _.xcworkspace_ file in your project.


## Signing in your user

Microsoft Graph notifications, like many other resource types inside Microsoft Graph, are centralized around users. In order for your app to subscribe to and start receiving notifications for the signed in user, you first need to obtain a valid OAuth token to be used in the registration process. You can use your preferred method of generating and managing the OAuth tokens. The sample app uses ADAL. 

If you're using a Microsoft account, you will need to include the following permissions in your sign-in request: `wl.offline_access"`, `ccs.ReadWrite`, `wns.connect`, `asimovrome.telemetry`, and `https://activity.windows.com/UserActivity.ReadWrite.CreatedByApp`. 

If you're using an Azure AD account, you'll need to request the following audience: `https://cdpcs.access.microsoft.com`.
 
```

## Subscribing to receive user's notifications 

You need to instantiate a **UserDataFeed** object for your application for this signed in user. Your application is identified by the cross-platform app ID you provided during the [Cross-Device Experiences onboarding](notifications-integration-cross-device-experiences-onboarding.md) process.

```ObjectiveC
    accessToken = ...; // the access token obtained from "Signing in your user" section
    // create an instance of UserNotificationApiImpl
     UserNotificationWebAPI userNotificationWebAPI = [[UserNotificationWebAPI alloc] init];
     [userNotificationWebAPI setOAuthAccessToken: accessToken];
    //  create a new Graph Notifications push notification subscription and set it as the current one for this client instance, or update the current subscription if one already exists. 

[sharedListener subscribeToUserNotificationsAsync:APNSPushNotificationToken
                                               appPackageNameForPushPlatform:@"com.microsoft.GraphNotificationsExample"
                                               appDisplayNameForUnsAnalytics:@"GraphNotificationsExample Dsiplay"
                                                           completionHandler:^(UserNotificationSusbscriptionResult *result) {
                                                           
                                                           }]; 
```

## Receiving and managing user notifications

The flow diagram earlier in this topic shows that the programming patterns to handle a new incoming notifications from an app server and a notification update or deletion initiated from another app client instance are similar. The following are the steps for handling these data changes. 

### Handling incoming push notification signal

All types of user notification data changes generate a signal that gets delivered to the app clients as a push notification. In the case of an iOS app, the signal is delivered as an APNs background update notification. On receiving the data message signal, the app should call userNotificationApiImpl.processPushNotificationAsync(notificationPayload: string) to trigger the SDK to fetch from the Microsoft Graph notifications service for the actual data changes.

```ObjectiveC
[userNotificationWebApi processPushNotificationAsync:notificationInfo completionHandler:^(ProcessPushNotificationResult * result) {
        NSMutableArray<UserNotification*>*userNotificationList =  [result getUserNotifications];
        if(result.isUserNotificationPush)
        {
            UserNotification* notification = [userNotificationList objectAtIndex:0];
            UNMutableNotificationContent *content = [[UNMutableNotificationContent alloc] init];
            RawNotificationPayload* payLoad = (RawNotificationPayload*)[notification getNotificationPayload];
            content.body = payLoad.rawContent;
            NSDictionary* userInfo = @{@"message:":payLoad.rawContent};
            content.userInfo = userInfo;
            content.sound = [UNNotificationSound defaultSound];
            [content setValue:@(YES) forKeyPath:@"shouldAlwaysAlertWhileAppIsForeground"];
            
            UNNotificationRequest *request = [UNNotificationRequest requestWithIdentifier:@"Notif" content:content trigger:nil];
            [[UNUserNotificationCenter currentNotificationCenter] addNotificationRequest:request withCompletionHandler:^(NSError * _Nullable error) {

            }];
        }
Notes:
  - Some Graph Notifications push notifications embed the Graph notifications to which they refer, but not all do. 
  For those that don’t, this function will attempt to fetch all Graph notifications since the last time it was called with a Graph Notifications push notification (whether or not that last one had embedded payload). 
  However, it is not guaranteed that the fetch will succeed or will get all matching notifications, especially because the number of network requests this function may make may be limited
  - In order to successfully perform the incremental fetch of Graph notifications just described, this function will persist in per-app non-volatile storage the timestamp of the last Graph Notifications push notification it has been successfully called with.
  Initially, that timestamp will be the beginning of the user’s notification feed
```

### Update state of a notification

If a notification state change is initiated from this app client instance (for example, if the toast notification popup on this device is activated by the user), the app needs to call the SDK to update the notification's state in order to have this state change synced across all devices used by the same user. 

```ObjectiveC
UserNotificationApiImpl* userNotificationApiImpl = ...; // create an instance of the UserNotificationApiImpl
NSString* notificationId = ...; // obtain the notification id for which the read state needs to be changed
BOOL readState = true; // change the read state to true
[sharedListener updateNotificationReadStateAsync:notificationId readState:readState completionHandler:^(BOOL *successResult) {
  //do your own processing or update your local notifications here
}];
```

### Delete a notifications

If a notification deletion is initiated from this app client instance (for example, if the task corresponding to this notification is marked as complete and is removed from your app's database), the app needs to call the SDK to delete the notification in order to have this delete operation synced across all devices used by the same user. 

A notification is removed from the user notification store only if it is expired or explicitly deleted. A user notification is not deleted when you update the **UserActionState** to be Dismissed, because the semantic definition of **UserActionState** is defined by the application itself.

```Obj-C
UserNotificationApiImpl* userNotificationApiImpl = ...; // create an instance of the UserNotificationApiImpl
NSString* notificationId = ...; // obtain the notification id for which the read state needs to be changed
 [sharedListener deleteNotificationAsync:notificationId completionHandler:^(NSDate *Date) {
 
 ]};
```

## See also

- [API reference](https://docs.microsoft.com/windows/project-rome/notifications/api-reference-for-ios/) for the full set of APIs related to notification features in the SDK. 
- [Client-side sample](https://github.com/Microsoft/project-rome/tree/master/iOS/samples/GraphNotifications) for Android apps.
- [App server sample](notifications-integrating-app-server.md) for publishing notifications. 
