---
title: "Delete subscription"
description: "Delete a subscription."
localization_priority: Normal
author: "davidmu1"
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# Delete subscription

Namespace: microsoft.graph

Delete a subscription.

See the table in the [Permissions](#permissions) section for the list of resources that support subscribing to change notifications.

## Permissions

Depending on the resource and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API. To learn more, including [taking caution](/graph/auth/auth-concepts#best-practices-for-requesting-permissions) before choosing more privileged permissions, search for the following permissions in [Permissions](/graph/permissions-reference).

| Supported resource | Delegated (work or school account) | Delegated (personal Microsoft account) | Application |
|:-----|:-----|:-----|:-----|
|[callRecord](../resources/callrecords-callrecord.md) | Not supported | Not supported | CallRecords.Read.All |
|[chatMessage](../resources/chatmessage.md) (/teams/{id}/channels/{id}/messages) | Not supported | Not supported |  ChannelMessage.Read.Group*, ChannelMessage.Read.All  |
|[chatMessage](../resources/chatmessage.md) (/teams/getAllMessages -- all channel messages in organization) | Not supported | Not supported | ChannelMessage.Read.All  |
|[chatMessage](../resources/chatmessage.md) (/chats/{id}/messages) | Not supported | Not supported | Chat.Read.All  |
|[chatMessage](../resources/chatmessage.md) (/chats/getAllMessages -- all chat messages in organization) | Not supported | Not supported | Chat.Read.All  |
|[contact](../resources/contact.md) | Contacts.Read | Contacts.Read | Contacts.Read |
|[driveItem](../resources/driveitem.md) (user's personal OneDrive) | Not supported | Files.ReadWrite | Not supported |
|[driveItem](../resources/driveitem.md) (OneDrive for Business) | Files.ReadWrite.All | Not supported | Files.ReadWrite.All |
|[event](../resources/event.md) | Calendars.Read | Calendars.Read | Calendars.Read |
|[group](../resources/group.md) | Group.Read.All | Not supported | Group.Read.All |
|[group conversation](../resources/conversation.md) | Group.Read.All | Not supported | Not supported |
|[list](../resources/list.md) | Sites.ReadWrite.All | Not supported | Sites.ReadWrite.All |
|[message](../resources/message.md) | Mail.ReadBasic, Mail.Read | Mail.ReadBasic, Mail.Read | Mail.ReadBasic, Mail.Read |
|[security alert](../resources/alert.md) | SecurityEvents.ReadWrite.All | Not supported | SecurityEvents.ReadWrite.All |
|[user](../resources/user.md) | User.Read.All | User.Read.All | User.Read.All |

> **Note**: Permissions marked with * use [resource-specific consent]( https://aka.ms/teams-rsc).

[!INCLUDE [teams-subscription-notes](../../includes/teams-subscription-notes.md)]

### driveItem

Additional limitations apply for subscriptions on OneDrive items. The limitations apply to creating as well as managing (getting, updating, and deleting) subscriptions.

On a personal OneDrive, you can subscribe to the root folder or any subfolder in that drive. On OneDrive for Business, you can subscribe to only the root folder. Change notifications are sent for the requested types of changes on the subscribed folder, or any file, folder, or other **driveItem** instances in its hierarchy. You cannot subscribe to **drive** or **driveItem** instances that are not folders, such as individual files.

### contact, event, and message

Additional limitations apply for subscriptions on Outlook items. The limitations apply to creating as well as managing (getting, updating, and deleting) subscriptions.

- Delegated permission supports subscribing to items in folders in only the signed-in user's mailbox. For example, you cannot use the delegated permission Calendars.Read to subscribe to events in another user’s mailbox.
- To subscribe to change notifications of Outlook contacts, events, or messages in _shared or delegated_ folders:

  - Use the corresponding application permission to subscribe to changes of items in a folder or mailbox of _any_ user in the tenant.
  - Do not use the Outlook sharing permissions (Contacts.Read.Shared, Calendars.Read.Shared, Mail.Read.Shared, and their read/write counterparts), as they do **not** support subscribing to change notifications on items in shared or delegated folders.


## HTTP request

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{subscription-id}
```

## Request headers

| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.
For details about how errors are returned, see [Error responses][error-response].

## Example

##### Request

Here is an example of the request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/7f105c7d-2dc5-4530-97cd-4e7ae6534c07
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/delete-subscription-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/delete-subscription-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/delete-subscription-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/delete-subscription-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### Response

Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 204 No Content
```

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Delete subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

