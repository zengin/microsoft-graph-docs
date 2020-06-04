---
title: "Activity Notification to a team"
description: "Create a copy of a team. This operation also creates a copy of the corresponding group."
author: "nkramer"
localization_priority: Normal
ms.prod: "microsoft-teams"
doc_type: apiPageType
---

# Clone a team

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Send an activity feed notification 
to a single [user](../resources/user.md), 
all users in a [chat](../resources/chat.md), 
or all users in a [team](../resources/team.md).

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
|topic|teamworkActivityTopic | Represents what is being referenced in the feed item. Required.|
|activityType | string | Represents the type of activity and must be declared in the [Teams App Manifest](../../resources/schema/manifest-schema.md). Required.|
|recipient | teamworkNotificationRecipient | The intended receiver. A recipient must be a Teams user with the ability to post notifications to everyone in a team, channel, and chat.  Required.|
| from | string |Displays a hint if the sender is different than the caller on the Graph token.|
| chainId | long | Enables the developer to override a previous notification. If not included, a new notifcation will be posted.|
| previewText | itemBody | Preview text displayed to the user as part an activity feed item. |
| templateParameters | collection\<keyvaluepair\>| Parameter values declared in the [Teams App Manifest](../../resources/schema/manifest-schema.md) |

## Response

If successful, this method will return a `202 Accepted` response code with a Location: header pointing to the [operation](../resources/teamsasyncoperation.md) resource.
When the operation is complete, the operation resource will tell you the id of the created team.

## Example

#### Request

The following is an example of the request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "clone_team"
}-->
```http
POST /users/{id}/teamwork/sendActivityNotification
Content-Type: application/json

{  
.....................
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

The following is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 202 Accepted
Location: /teams({id})/operations({opId})
Content-Type: text/plain
Content-Length: 0
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
