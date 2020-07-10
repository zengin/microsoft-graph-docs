---
title: "application resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# application resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List applications](../api/application-list.md)|[application](../resources/application.md) collection|Get a list of the [application](../resources/application.md) objects and their properties.|
|[Create application](../api/application-post-applications.md)|[application](../resources/application.md)|Create a new [application](../resources/application.md) object.|
|[Get application](../api/application-get.md)|[application](../resources/application.md)|Read the properties and relationships of an [application](../resources/application.md) object.|
|[Update application](../api/application-update.md)|[application](../resources/application.md)|Update the properties of an [application](../resources/application.md) object.|
|[Delete application](../api/application-delete.md)|None|Deletes an [application](../resources/application.md) object.|
|[List synchronization](../api/application-list-synchronization.md)|[synchronization](../resources/synchronization-synchronization.md) collection|Get the synchronizations from the synchronization navigation property.|
|[Create synchronization](../api/application-post-synchronization.md)|[synchronization](../resources/synchronization-synchronization.md)|Create a new synchronization object.|
|[Get synchronization](../api/application-get-synchronization.md)|[synchronization](../resources/synchronization-synchronization.md)|Read the properties and relationships of a [synchronization](../resources/synchronization-synchronization.md) object.|
|[Update synchronization](../api/application-update-synchronization.md)|[synchronization](../resources/synchronization-synchronization.md)|Update the properties of a synchronization object.|
|[Delete synchronization](../api/application-delete-synchronization.md)|None|Delete a [synchronization](../resources/synchronization-synchronization.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|synchronization|[synchronization](../resources/synchronization-synchronization.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.application",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.application",
  "id": "String (identifier)"
}
```

