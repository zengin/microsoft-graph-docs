---
title: "workbookFilterCriteria resource type"
description: "Represents the filtering criteria applied to a column."
localization_priority: Normal
doc_type: resourcePageType
ms.prod: "excel"
author: ""
---

# workbookFilterCriteria resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the filtering criteria applied to a column.

## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilterCriteria"
}-->

```json
{
  "color": "string",
  "criterion1": "string",
  "criterion2": "string",
  "dynamicCriteria": "string",
  "filterOn": "string",
  "values": {"@odata.type":"microsoft.graph.Json"},
  "icon":{"@odata.type": "microsoft.graph.workbookIcon"},
  "operator":"string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "workbookFilterCriteria resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
     "Error: /resources/workbookfiltercriteria.md:\r\n      A required document header is missing from the document: Properties"
  ]
}
-->