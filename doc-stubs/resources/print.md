---
title: "print resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# print resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List prints](../api/print-list.md)|[print](../resources/print.md) collection|Get a list of the [print](../resources/print.md) objects and their properties.|
|[Create print](../api/print-create.md)|[print](../resources/print.md)|Create a new [print](../resources/print.md) object.|
|[Get print](../api/print-get.md)|[print](../resources/print.md)|Read the properties and relationships of a [print](../resources/print.md) object.|
|[Update print](../api/print-update.md)|[print](../resources/print.md)|Update the properties of a [print](../resources/print.md) object.|
|[Delete print](../api/print-delete.md)|None|Deletes a [print](../resources/print.md) object.|
|[List taskDefinitions](../api/print-list-taskdefinitions.md)|[printTaskDefinition](../resources/printtaskdefinition.md) collection|Get the printTaskDefinitions from the taskDefinitions navigation property.|
|[Create taskDefinitions](../api/print-post-taskdefinitions.md)|[printTaskDefinition](../resources/printtaskdefinition.md)|Create a new taskDefinitions object.|
|[Get taskDefinitions](../api/print-get-printtaskdefinition.md)|[printTaskDefinition](../resources/printtaskdefinition.md)|Read the properties and relationships of a [printTaskDefinition](../resources/printtaskdefinition.md) object.|
|[Update taskDefinitions](../api/print-update-taskdefinitions.md)|[printTaskDefinition](../resources/printtaskdefinition.md)|Update the properties of a taskDefinitions object.|
|[Delete taskDefinitions](../api/print-delete-taskdefinitions.md)|None|Delete a [printTaskDefinition](../resources/printtaskdefinition.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|settings|[printSettings](../resources/printsettings.md)|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|connectors|[printConnector](../resources/printconnector.md) collection|**TODO: Add Description**|
|operations|[printOperation](../resources/printoperation.md) collection|**TODO: Add Description**|
|printers|[printer](../resources/printer.md) collection|**TODO: Add Description**|
|printerShares|[printerShare](../resources/printershare.md) collection|**TODO: Add Description**|
|reports|[reportRoot](../resources/reportroot.md) collection|**TODO: Add Description**|
|services|[printService](../resources/printservice.md) collection|**TODO: Add Description**|
|shares|[printerShare](../resources/printershare.md) collection|**TODO: Add Description**|
|taskDefinitions|[printTaskDefinition](../resources/printtaskdefinition.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.print",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.print",
  "id": "String (identifier)",
  "settings": {
    "@odata.type": "microsoft.graph.printSettings"
  }
}
```

