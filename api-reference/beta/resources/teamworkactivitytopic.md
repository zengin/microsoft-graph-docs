---
title: "teamworkActivityTopic resource type"
description: "The location field of an activity notification"
author: "nkramer"
localization_priority: Normal
ms.prod: Priority
doc_type: resourcePageType
---

# teamworkActivityTopic resource type

Namespace: microsoft.graph

The location field (a.k.a. second line) of an [activity notification](../api/team-sendactivitynotification.md).

## Properties
|Property|Type|Description|
|:---|:---|:---|
|source|teamworkActivityTopicSource| Describes what the value property represents -- a URL to a Microsoft Graph entity, or the actual text to display in the activity Notification's second line. Possible values are: `entityUrl`, `text`.|
|value|String| Depending on the source property, this is either a URL to a Microsoft Graph entity, or the actual text to display in the activity Notification's second line.|
|webUrl|String|URL Navigate to when the user clicks on an activity notification. Must be a link that navigates within Microsoft Teams.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamworkActivityTopic"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.teamworkActivityTopic",
  "source": "String",
  "value": "String",
  "webUrl": "String"
}
```

