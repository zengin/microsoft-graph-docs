---
title: "group resource type"
description: "Represents an Azure Active Directory (Azure AD) group, which can be a Microsoft 365 group, or a security group. "
localization_priority: Priority
author: "yyuank"
ms.prod: "groups"
doc_type: resourcePageType
---

# group resource type

Namespace: microsoft.graph

Represents an Azure Active Directory (Azure AD) group, which can be a Microsoft 365 group, or a security group.

Inherits from [directoryObject](directoryobject.md).

For performance reasons, the [create](../api/group-post-groups.md), [get](../api/group-get.md), and [list](../api/group-list.md) operations return only a subset of more commonly used properties by default. These _default_ properties are noted in the [Properties](#properties) section. To get any of the properties that are not returned by default, specify them in a `$select` OData query option.

This resource supports:

- Adding your own data to custom properties as [extensions](/graph/extensibility-overview).
- Subscribing to [change notifications](/graph/webhooks).
- Using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/user-delta.md) function.


## Methods

| Method | Return Type | Description |
|:------ |:----------- |:----------- |
| **Group management** |||
| [Create group](../api/group-post-groups.md) | [group](group.md) | Create a new group. It can be a Microsoft 365 group, dynamic group, or security group. |
| [Get group](../api/group-get.md) | [group](group.md) | Read properties of a group object. |
| [List groups](../api/group-list.md) | [group](group.md) collection | List group objects and their properties. |
| [Update group](../api/group-update.md) | None | Update the properties of a group object. |
| [Delete group](../api/group-delete.md) | None | Delete group object. |
| [delta](../api/group-delta.md) | group collection | Get incremental changes for groups. |
| [Add member](../api/group-post-members.md) | None | Add a user or group to this group by posting to the **members** navigation property (supported for security groups and mail-enabled security groups only). |
| [Add owner](../api/group-post-owners.md) | None | Add a new owner for the group by posting to the **owners** navigation property (supported for security groups and mail-enabled security groups only). |
| [Create setting](../api/groupsetting-post-groupsettings.md) | [groupSetting](groupsetting.md) | Create a setting object based on a groupSettingTemplate. The POST request must provide settingValues for all the settings defined in the template. Only groups specific templates may be used for this operation. |
| [Delete setting](../api/groupsetting-delete.md) | None | Delete a setting object. |
| [Get setting](../api/groupsetting-get.md) | [groupSetting](groupsetting.md) | Read properties of a specific setting object. |
| [List groupLifecyclePolicies](../api/group-list-grouplifecyclepolicies.md)  | [groupLifecyclePolicy](grouplifecyclepolicy.md) collection | List group lifecycle policies. |
| [List members](../api/group-list-members.md) | [directoryObject](directoryobject.md) collection | Get the users and groups that are direct members of this group from the **members** navigation property. |
| [List owners](../api/group-list-owners.md) | [directoryObject](directoryobject.md) collection | Get the owners of the group from the **owners** navigation property. |
| [List settings](../api/groupsetting-list.md) | [groupSetting](groupsetting.md) collection | List properties of all setting objects. |
| [List transitive members](../api/group-list-transitivemembers.md) | [directoryObject](directoryobject.md) collection | Get the users, groups and devices that are members, including nested members of this group. |
| [List transitive memberOf](../api/group-list-transitivememberof.md) | [directoryObject](directoryobject.md) collection | List the groups that this group is a member of. This operation is transitive and includes the groups that this group is a nested member of. |
| [Remove member](../api/group-delete-members.md) | None | Remove a member from a Microsoft 365 group, a security group or a mail-enabled security group through the **members** navigation property. You can remove users or other groups. |
| [Remove owner](../api/group-delete-owners.md) | None | Remove an owner from a Microsoft 365 group, a security group or a mail-enabled security group through the **owners** navigation property. |
| [Update setting](../api/groupsetting-update.md) | [groupSetting](groupsetting.md) | Update a setting object. |
| [assignLicense](../api/group-assignlicense.md) | [group](group.md) | Add or remove subscriptions for the group. You can also enable and disable specific plans associated with a subscription. |
| [checkMemberGroups](../api/group-checkmembergroups.md) | String collection | Check this group for membership in a list of groups. The function is transitive. |
| [checkMemberObjects](../api/group-checkmemberobjects.md) | String collection | Check for membership in a list of group, directory role, or administrative unit objects. The function is transitive. |
| [getMemberGroups](../api/group-getmembergroups.md) | String collection | Return all the groups that the group is a member of. The function is transitive. |
| [getMemberObjects](../api/group-getmemberobjects.md) | String collection | Return all of the groups that the group is a member of. The function is transitive. |
| [renew](../api/group-renew.md) | Boolean | Renews a group's expiration. When a group is renewed, the group expiration is extended by the number of days defined in the policy. |
| [validateProperties](../api/group-validateproperties.md) | JSON | Validate that a Microsoft 365 group's display name or mail nickname complies with naming policies. |
| **App role assignments** |||
| [List appRoleAssignments](../api/group-list-approleassignments.md) | [appRoleAssignment](approleassignment.md) collection | Get the apps and app roles which this group has been assigned. |
| [Add appRoleAssignment](../api/group-post-approleassignments.md) | [appRoleAssignment](approleassignment.md) | Assign an app role to this group. |
| [Remove appRoleAssignment](../api/group-delete-approleassignments.md) | None. | Remove an app role assignment from this group. |
| **Calendar** |||
| [Create event](../api/group-post-events.md) | [event](event.md) | Create a new event by posting to the events collection. |
| [Get event](../api/group-get-event.md) | [event](event.md) | Read properties of an event object. |
| [List events](../api/group-list-events.md) | [event](event.md) collection | Get an event object collection. |
| [Update event](../api/group-update-event.md) | None | Update the properties of an event object. |
| [Delete event](../api/group-delete-event.md) | None | Delete event object. |
| [List calendarView](../api/group-list-calendarview.md) | [event](event.md) collection | Get a collection of events in a specified time window.|
| **Conversations** |||
| [Create conversation](../api/group-post-conversations.md) | [conversation](conversation.md) | Create a new conversation by posting to the conversations collection. |
| [Get conversation](../api/group-get-conversation.md) | [conversation](conversation.md) | Read properties of a conversation object. |
| [List conversations](../api/group-list-conversations.md) | [conversation](conversation.md) collection | Get a conversation object collection. |
| [Delete conversation](../api/group-delete-conversation.md) | None | Delete conversation object. |
| [Create thread](../api/group-post-threads.md) | [conversationThread](conversationthread.md) | Create a new conversation thread. |
| [Get thread](../api/group-get-thread.md) | [conversationThread](conversationthread.md) | Read properties of a thread object. |
| [List threads](../api/group-list-threads.md) | [conversationThread](conversationthread.md) collection | Get all the threads of a group. |
| [Update thread](../api/group-update-thread.md) | None | Update properties of a thread object. |
| [Delete thread](../api/group-delete-thread.md) | None | Delete thread object. |
| [List acceptedSenders](../api/group-list-acceptedsenders.md) | [directoryObject](directoryobject.md) collection | Get a list of users or groups that are in the accepted-senders list for this group. |
| [Add acceptedSender](../api/group-post-acceptedsenders.md) | [directoryObject](directoryobject.md) | Add a User or Group to the acceptSenders collection. |
| [Remove acceptedSender](../api/group-delete-acceptedsenders.md) | [directoryObject](directoryobject.md) | Remove a User or Group from the acceptedSenders collection. |
| [List rejectedSenders](../api/group-list-rejectedsenders.md) | [directoryObject](directoryobject.md) collection | Get a list of users or groups that are in the rejected-senders list for this group. |
| [Add rejectedSender](../api/group-post-rejectedsenders.md)  | [directoryObject](directoryobject.md) | Add a new User or Group to the rejectedSenders collection. |
| [Remove rejectedSender](../api/group-delete-rejectedsenders.md) | [directoryObject](directoryobject.md) | Remove new User or Group from the rejectedSenders collection. |
| [Create setting](../api/groupsetting-post-groupsettings.md) | [groupSetting](groupsetting.md) | Create a setting object based on a groupSettingTemplate. The POST request must provide settingValues for all the settings defined in the template. Only groups specific templates may be used for this operation. |
| [Get setting](../api/groupsetting-get.md) | [groupSetting](groupsetting.md) | Read properties of a specific setting object. |
| [List settings](../api/groupsetting-list.md) | [groupSetting](groupsetting.md) collection | List properties of all setting objects. |
| [Update setting](../api/groupsetting-update.md) | None | Update a setting object. |
| [Delete setting](../api/groupsetting-delete.md) | None | Delete a setting object. |
| [Get setting template](../api/groupsettingtemplate-get.md) | None | Read properties of a setting template. |
| [List setting template](../api/groupsettingtemplate-list.md) | None | List properties of all setting templates. |
| **Open extensions** |||
| [Create open extension](../api/opentypeextension-post-opentypeextension.md) | [openTypeExtension](opentypeextension.md) | Create an open extension and add custom properties to a new or existing resource. |
| [Get open extension](../api/opentypeextension-get.md) | [openTypeExtension](opentypeextension.md) collection | Get an open extension identified by the extension name. |
| **Schema extensions** |||
| [Add schema extension values](/graph/extensibility-schema-groups) | None | Create a schema extension definition and then use it to add custom typed data to a resource. |
| **Other group resources** |||
| [List photos](../api/group-list-photos.md) | [profilePhoto](photo.md) collection | Get a collection of profile photos for the group. |
| [List plannerPlans](../api/plannergroup-list-plans.md) | [plannerPlan](plannerplan.md) collection | Get Planner plans owned by the group. |
| **User settings** |||
| [addFavorite](../api/group-addfavorite.md) | None | Add the group to the list of the signed-in user's favorite groups. Supported for only Microsoft 365 groups. |
| [removeFavorite](../api/group-removefavorite.md) | None | Remove the group from the list of the signed-in user's favorite groups. Supported for only Microsoft 365 groups. |
| [List memberOf](../api/group-list-memberof.md) | [directoryObject](directoryobject.md) collection | Get the groups and administrative units that this user is a direct member of, from the **memberOf** navigation property. |
| [subscribeByMail](../api/group-subscribebymail.md) | None | Set the isSubscribedByMail property to **true**. Enabling the signed-in user to receive email conversations. Supported for only Microsoft 365 groups. |
| [unsubscribeByMail](../api/group-unsubscribebymail.md) | None | Set the isSubscribedByMail property to **false**. Disabling the signed-in user from receive email conversations. Supported for only Microsoft 365 groups. |
| [resetUnseenCount](../api/group-resetunseencount.md) | None | Reset the unseenCount to 0 of all the posts that the signed-in user has not seen since their last visit. Supported for only Microsoft 365 groups. |

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|allowExternalSenders|Boolean| Indicates if people external to the organization can send messages to the group. Default value is **false**. <br><br>Returned only on $select. |
|assignedLabels|[assignedLabel](assignedlabel.md) collection|The list of sensitivity label pairs (label ID, label name) associated with an Microsoft 365 group. <br><br>Returned only on $select. Read-only.|
|assignedLicenses|[assignedLicense](assignedlicense.md) collection|The licenses that are assigned to the group. <br><br>Returned only on $select. Read-only.|
|autoSubscribeNewMembers|Boolean|Indicates if new members added to the group will be auto-subscribed to receive email notifications. You can set this property in a PATCH request for the group; do not set it in the initial POST request that creates the group. Default value is **false**. <br><br>Returned only on $select.|
|classification|String|Describes a classification for the group (such as low, medium or high business impact). Valid values for this property are defined by creating a ClassificationList [setting](groupsetting.md) value, based on the [template definition](groupsettingtemplate.md).<br><br>Returned by default.|
|createdDateTime|DateTimeOffset| Timestamp of when the group was created. The value cannot be modified and is automatically populated when the group is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. <br><br>Returned by default. Read-only. |
|deletedDateTime|DateTimeOffset| For some Azure Active Directory objects (user, group, application), if the object is deleted, it is first logically deleted, and this property is updated with the date and time when the object was deleted. Otherwise this property is null. If the object is restored, this property is updated to null. |
|description|String|An optional description for the group. <br><br>Returned by default.|
|displayName|String|The display name for the group. This property is required when a group is created and cannot be cleared during updates. <br><br>Returned by default. Supports $filter and $orderby. |
|expirationDateTime|DateTimeOffset| Timestamp of when the group is set to expire. The value cannot be modified and is automatically populated when the group is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. <br><br>Returned by default. Read-only. |
|groupTypes|String collection| Specifies the group type and its membership.  <br><br>If the collection contains `Unified`, the group is a Microsoft 365 group; otherwise, it's either a security group or distribution group. For details, see [groups overview](groups-overview.md).<br><br>If the collection includes `DynamicMembership`, the group has dynamic membership; otherwise, membership is static.  <br><br>Returned by default. Supports $filter.|
|hasMembersWithLicenseErrors|Boolean|Indicates whether there are members in this group that have license errors from its group-based license assignment. <br><br>This property is never returned on a GET operation. You can use it as a $filter argument to get groups that have members with license errors (that is, filter for this property being true). See an [example](../api/group-list.md).|
|hideFromAddressLists |Boolean |True if the group is not displayed in certain parts of the Outlook UI: the **Address Book**, address lists for selecting message recipients, and the **Browse Groups** dialog for searching groups; otherwise, false. Default value is **false**. <br><br>Returned only on $select.|
|hideFromOutlookClients |Boolean |True if the group is not displayed in Outlook clients, such as Outlook for Windows and Outlook on the web; otherwise, false. Default value is **false**. <br><br>Returned only on $select.|
|id|String|The unique identifier for the group. <br><br>Returned by default. Inherited from [directoryObject](directoryobject.md). Key. Not nullable. Read-only.|
|isSubscribedByMail|Boolean|Indicates whether the signed-in user is subscribed to receive email conversations. Default value is **true**. <br><br>Returned only on $select. |
|licenseProcessingState|String|Indicates status of the group license assignment to all members of the group. Default value is **false**. Read-only. Possible values: `QueuedForProcessing`, `ProcessingInProgress`, and `ProcessingComplete`.<br><br>Returned only on $select. Read-only.|
|mail|String|The SMTP address for the group, for example, "serviceadmins@contoso.onmicrosoft.com". <br><br>Returned by default. Read-only. Supports $filter.|
|mailEnabled|Boolean|Specifies whether the group is mail-enabled. <br><br>Returned by default.|
|membershipRule|String|The rule that determines members for this group if the group is a dynamic group (groupTypes contains `DynamicMembership`). For more information about the syntax of the membership rule, see [Membership Rules syntax](/azure/active-directory/users-groups-roles/groups-dynamic-membership). <br><br>Returned by default. |
|membershipRuleProcessingState|String|Indicates whether the dynamic membership processing is on or paused. Possible values are "On" or "Paused". <br><br>Returned by default. |
|onPremisesSamAccountName|String|Contains the on-premises **SAM account name** synchronized from the on-premises directory. The property is only populated for customers who are synchronizing their on-premises directory to Azure Active Directory via Azure AD Connect.<br><br>Returned by default. Read-only. |
|onPremisesSecurityIdentifier|String|Contains the on-premises security identifier (SID) for the group that was synchronized from on-premises to the cloud. <br><br>Returned by default. Read-only. |
|onPremisesSyncEnabled|Boolean|**true** if this group is synced from an on-premises directory; **false** if this group was originally synced from an on-premises directory but is no longer synced; **null** if this object has never been synced from an on-premises directory (default). <br><br>Returned by default. Read-only. Supports $filter.|
|preferredDataLocation|String|The preferred data location for the group. For more information, see  [OneDrive Online Multi-Geo](/sharepoint/dev/solution-guidance/multigeo-introduction). <br><br>Returned by default.|
|preferredLanguage|String|The preferred language for an Microsoft 365 group. Should follow ISO 639-1 Code; for example "en-US". <br><br>Returned by default. |
|proxyAddresses|String collection| Email addresses for the group that direct to the same group mailbox. For example: `["SMTP: bob@contoso.com", "smtp: bob@sales.contoso.com"]`. The **any** operator is required to filter expressions on multi-valued properties. <br><br>Returned by default. Read-only. Not nullable. Supports $filter. |
|renewedDateTime|DateTimeOffset| Timestamp of when the group was last renewed. This cannot be modified directly and is only updated via the [renew service action](../api/group-renew.md). The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. <br><br>Returned by default. Read-only.|
|resourceBehaviorOptions|String collection|Specifies the group behaviors that can be set for a Microsoft 365 group during creation. This can be set only as part of creation (POST). Possible values are `AllowOnlyMembersToPost`, `HideGroupInOutlook`, `SubscribeNewGroupMembers`, `WelcomeEmailDisabled`. For more information, see [Set Microsoft 365 group behaviors and provisioning options](/graph/group-set-options).|
|resourceProvisioningOptions|String collection|Specifies the group resources that are provisioned as part of Microsoft 365 group creation, that are not normally part of default group creation. Possible value is `Team`. For more information, see [Set Microsoft 365 group behaviors and provisioning options](/graph/group-set-options).|
|securityEnabled|Boolean|Specifies whether the group is a security group. <br><br>Returned by default. Supports $filter.|
|securityIdentifier|String|Security identifier of the group, used in Windows scenarios. <br><br>Returned by default.|
|theme|String|Specifies an Microsoft 365 group's color theme. Possible values are `Teal`, `Purple`, `Green`, `Blue`, `Pink`, `Orange` or `Red`. <br><br>Returned by default. |
|unseenCount|Int32|Count of conversations that have received new posts since the signed-in user last visited the group. <br><br>Returned only on $select. |
|visibility|String| Specifies the group join policy and group content visibility for groups. Possible values are: `Private`, `Public`, or `Hiddenmembership`. `Hiddenmembership` can be set only for Microsoft 365 groups, when the groups are created. It can't be updated later. Other values of visibility can be updated after group creation.<br> If visibility value is not specified during group creation on Microsoft Graph, a security group is created as `Private` by default and Microsoft 365 group is `Public`. See [group visibility options](#group-visibility-options) to learn more. <br><br>Returned by default.|


### Group visibility options

Here's what each **visibility** property value means:

|Value|Description|
|:----|-----------|
| Public | Anyone can join the group without needing owner permission.<br>Anyone can view the contents of the group.|
| Private | Owner permission is needed to join the group.<br>Non-members cannot view the contents of the group.|
| Hiddenmembership | Owner permission is needed to join the group.<br>Non-members cannot view the contents of the group.<br>Non-members cannot see the members of the group.<br>Administrators (global, company, user, and helpdesk) can view the membership of the group.<br>The group appears in the global address book (GAL).|


## Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|acceptedSenders|[directoryObject](directoryobject.md) collection|The list of users or groups that are allowed to create post's or calendar events in this group. If this list is non-empty then only users or groups listed here are allowed to post.|
|appRoleAssignments|[appRoleAssignment](approleassignment.md) collection|Represents the app roles a group has been granted for an application. |
|calendar|[calendar](calendar.md)|The group's calendar. Read-only.|
|calendarView|[event](event.md) collection|The calendar view for the calendar. Read-only.|
|conversations|[conversation](conversation.md) collection|The group's conversations.|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| The user (or application) that created the group. NOTE: This is not set if the user is an administrator. Read-only.|
|drive|[drive](drive.md)|The group's default drive. Read-only.|
|drives|[drive](drive.md) collection|The group's drives. Read-only.|
|events|[event](event.md) collection|The group's calendar events.|
|extensions|[extension](extension.md) collection|The collection of open extensions defined for the group. Read-only. Nullable.|
|groupLifecyclePolicies|[groupLifecyclePolicy](grouplifecyclepolicy.md) collection|The collection of lifecycle policies for this group. Read-only. Nullable.|
|memberOf|[directoryObject](directoryobject.md) collection|Groups that this group is a member of. HTTP Methods: GET (supported for all groups). Read-only. Nullable.|
|members|[directoryObject](directoryobject.md) collection| Users and groups that are members of this group. HTTP Methods: GET (supported for all groups), POST (supported for Microsoft 365 groups, security groups and mail-enabled security groups), DELETE (supported for Microsoft 365 groups and security groups). Nullable.|
|membersWithLicenseErrors|[User](user.md) collection|A list of group members with license errors from this group-based license assignment. Read-only.|
|onenote|[Onenote](onenote.md)| Read-only.|
|owners|[directoryObject](directoryobject.md) collection|The owners of the group. The owners are a set of non-admin users who are allowed to modify this object. Limited to 100 owners. HTTP Methods: GET (supported for all groups), POST (supported for Microsoft 365 groups, security groups and mail-enabled security groups), DELETE (supported for Microsoft 365 groups and security groups). Nullable.|
|photo|[profilePhoto](profilephoto.md)| The group's profile photo |
|photos|[profilePhoto](profilephoto.md) collection| The profile photos owned by the group. Read-only. Nullable.|
|planner|[plannerGroup](plannergroup.md)| Entry-point to Planner resource that might exist for a Unified Group.|
|rejectedSenders|[directoryObject](directoryobject.md) collection|The list of users or groups that are not allowed to create posts or calendar events in this group. Nullable|
|settings|[groupSetting](groupsetting.md) collection| Read-only. Nullable.|
|sites|[site](site.md) collection|The list of SharePoint sites in this group. Access the default site with /sites/root.|
|threads|[conversationThread](conversationthread.md) collection| The group's conversation threads. Nullable.|

## JSON representation

The following is a JSON representation of the resource.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.directoryObject",
  "openType": true,
  "optionalProperties": [
    "acceptedSenders",
    "appRoleAssignments",
    "calendar",
    "calendarView",
    "conversations",
    "createdOnBehalfOf",
    "drive",
    "drives",
    "events",
    "extensions",
    "groupLifecyclePolicies",
    "memberOf",
    "members",
    "onenote",
    "owners",
    "photo",
    "photos",
    "planner",
    "rejectedSenders",
    "settings",
    "sites",
    "threads",

    "allowExternalSenders",
    "assignedLicenses",
    "autoSubscribeNewMembers",
    "hasMembersWithLicenseErrors",
    "isSubscribedByMail",
    "licenseProcessingState",
    "unseenCount"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.group",
  "@odata.annotations": [
    {
      "capabilities": {
        "changeTracking": true
      }
    },
    {
      "property": "acceptedSenders",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "calendar",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "calendarView",
      "capabilities": {
        "changeTracking": true,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "conversations",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "updatable": false
      }
    },
    {
      "property": "events",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    },
    {
      "property": "photo",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false
      }
    },
    {
      "property": "photos",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "expandable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "rejectedSenders",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false,
        "updatable": false
      }
    },
    {
      "property": "threads",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "allowExternalSenders": false,
  "assignedLicenses": [{"@odata.type": "microsoft.graph.assignedLicense"}],
  "autoSubscribeNewMembers": true,
  "classification": "string",
  "createdDateTime": "String (timestamp)",
  "description": "string",
  "displayName": "string",
  "groupTypes": ["string"],
  "hasMembersWithLicenseErrors": "Boolean",
  "hideFromAddressLists": false,
  "hideFromOutlookClients": false,
  "id": "string (identifier)",
  "isSubscribedByMail": true,
  "licenseProcessingState": "string",
  "mail": "string",
  "mailEnabled": true,
  "mailNickname": "string",
  "onPremisesLastSyncDateTime": "String (timestamp)",
  "onPremisesProvisioningErrors": [{"@odata.type": "microsoft.graph.onPremisesProvisioningError"}],
  "onPremisesSecurityIdentifier": "string",
  "onPremisesSyncEnabled": true,
  "preferredDataLocation": "string",
  "proxyAddresses": ["string"],
  "renewedDateTime": "String (timestamp)",
  "resourceBehaviorOptions": ["String"],
  "resourceProvisioningOptions": ["String"],
  "securityEnabled": true,
  "securityIdentifier": "String",
  "unseenCount": 1024,
  "visibility": "string",
  "acceptedSenders": [ { "@odata.type": "microsoft.graph.directoryObject"} ],
  "calendar": { "@odata.type": "microsoft.graph.calendar" },
  "calendarView": [{ "@odata.type": "microsoft.graph.event" }],
  "conversations": [ { "@odata.type": "microsoft.graph.conversation" }],
  "createdOnBehalfOf": { "@odata.type": "microsoft.graph.directoryObject" },
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "events": [ { "@odata.type": "microsoft.graph.event" }],
  "memberOf": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "members": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "membersWithLicenseErrors": [{"@odata.type": "microsoft.graph.user"}],
  "owners": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "photo": { "@odata.type": "microsoft.graph.profilePhoto" },
  "rejectedSenders": [ { "@odata.type": "microsoft.graph.directoryObject" } ],
  "sites": [ { "@odata.type": "microsoft.graph.site" } ],
  "threads": [ { "@odata.type": "microsoft.graph.conversationThread" }]
}
```

## See also

- [Add custom data to resources using extensions](/graph/extensibility-overview)
- [Add custom data to users using open extensions](/graph/extensibility-open-users)
- [Add custom data to groups using schema extensions](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
