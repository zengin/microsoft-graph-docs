---
title: "aadUserNotificationRecipient resource type"
description: "Who to send an activity notification to."
author: "nkramer"
localization_priority: Normal
ms.prod: Priority
doc_type: resourcePageType
---

# aadUserNotificationRecipient resource type

Namespace: microsoft.graph

Represents something an [activity notification](../api/team-sendactivitynotification.md)
to a user via their user id (guid).

Inherits from [teamworkNotificationRecipient](../resources/teamworknotificationrecipient.md).

## Properties
|Property|Type|Description|
|:---|:---|:---|
|userId|String|The guid of the user.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.aadUserNotificationRecipient"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.aadUserNotificationRecipient",
  "userId": "String"
}
```

