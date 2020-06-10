---
title: "Send Activity Notification"
description: "Send an activity feed notification to a single user, to all users in a chat, or to all users in a team."
author: "nkramer"
localization_priority: Normal
ms.prod: "microsoft-teams"
doc_type: apiPageType
---

# Send Activity Notification

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Send an activity feed notification 
to a single [user](../resources/user.md), 
to all users in a [chat](../resources/chat.md), 
or to all users in a [team](../resources/team.md).

> Note: Only Microsoft Graph appids that have been linked with a Teams appid can send notifications, 
see [Teams App Manifest](/microsoftteams/platform/graph-api/activity-feed/feed-notifications#update-your-teams-app-manifest) for more information.

> Note: Currently activity notifications sent via this API will only appear For users running Microsoft Teams Developer Preview on a web or desktop device.
See [How do I enable Developer Preview](/microsoftteams/platform/resources/dev-preview/developer-preview-intro) for more information.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account)     | TeamsActivity.Send |
|Delegated (personal Microsoft account) | Not supported.    |
|Application                            | TeamsActivity.Send |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id}/teamwork/sendActivityNotification
POST /users/{id}/chats/{id}/sendActivityNotification
POST /chats/{id}/sendActivityNotification
POST /teams/{id}/sendActivityNotification
```

## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |
| Content-Type  | application/json  |

## Request body

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|topic|[teamworkActivityTopic](../resources/teamworkactivitytopic.md) | Represents what is being referenced in the feed item. Required.|
|activityType | string | Represents the type of activity and must be declared in the [Teams App Manifest](/microsoftteams/platform/graph-api/activity-feed/feed-notifications#update-your-teams-app-manifest). Required.|
|recipient | [teamworkNotificationRecipient](../resources/teamworknotificationrecipient.md) | The intended receiver. A recipient must be a Teams user with the ability to post notifications to everyone in a team, channel, and chat.  Required.|
| from | string |Displays a hint if the sender is different than the caller on the Graph token.|
| chainId | long | Enables the developer to override a previous notification. If not included, a new notifcation will be posted. Note: currently, when specifying chainId, an unrelated notification from the same app will sometimes be replaced, we are working on a fix. |
| previewText | [itemBody](../resources/itemBody.md) | Preview text displayed to the user as part an activity feed item. |
| templateParameters | [keyValuePair](../resources/keyvaluepair.md) collection | Parameter values declared in the [Teams App Manifest](/microsoftteams/platform/graph-api/activity-feed/feed-notifications#update-your-teams-app-manifest) |

## Response

If successful, this method will return a `202 Accepted` response code with a Location: header pointing to the [operation](../resources/teamsasyncoperation.md) resource.
When the operation is complete, the operation resource will tell you the id of the created team.

If there is more than one Teams app corresponding to a given Graph appid, this method will return a `409 Conflict` response code
with the message `Found multiple applications with the same AAD App ID '{guid}' - a Teams Application ID is required to resolve which application is correct.`
The message is misleading, there is no way to specify a Teams Application ID.
You must disambiguate by uninstalling any conflicting Teams apps.
Note that sideloading (uploading custom maps to a particular team, rather than to the app catalog)
creates a new teams app and a new teams appid.

## Example

#### Request

The following is an example of the request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "Send_activity_notification"
}-->
```http
POST /teams/{teamId}/sendActivityNotification

Content-Type: application/json
  
{
  "topic": {
    "source": "entityUrl",
    "value": "https://graph.microsoft.com/teams/dc0ae126-1046-4c7b-8b56-991f55479a11/channels/19:910b7d76f3564480a0e52e0671e0f116@thread.tacv2/messages/1591749374896"
  },
  "activityType": "questionAnswered",
  "previewText": {
    "content": "Your question has been answered"
  },
  "recipient": {
    "@odata.type": "microsoft.graph.aadUserNotificationRecipient",
    "userId": "598efcd4-e549-402a-9602-0b50201faebe"
  },
  "templateParameters": [
    {
      "@odata.type": "microsoft.graph.keyValuePair"
    }
  ]
}
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/clone-team-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/clone-team-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/clone-team-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### Response

The following is an example of the response. 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Send Activity Notification",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
