---
title: "patternedRecurrence resource type"
description: "The recurrence pattern and range."
localization_priority: Normal
doc_type: resourcePageType
ms.prod: "governance"
author: "harini84"
---

# patternedRecurrence resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The recurrence pattern and range.

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|pattern|[recurrencePattern](recurrencepattern.md)|The frequency of an event.|
|range|[recurrenceRange](recurrencerange.md)|The duration of an event.|

## JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.patternedRecurrence"
}-->

```json
{
  "pattern": {"@odata.type": "microsoft.graph.recurrencePattern"},
  "range": {"@odata.type": "microsoft.graph.recurrenceRange"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "patternedRecurrence resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


