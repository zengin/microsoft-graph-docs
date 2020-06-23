---
title: "synchronizationSchema resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# synchronizationSchema resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List schema](../api/synchronization-synchronizationjob-list-schema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md) collection|Get the synchronizationSchemas from the schema navigation property.|
|[Create schema](../api/synchronization-synchronizationjob-post-schema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Create a new schema object.|
|[Update schema](../api/synchronization-synchronizationjob-update-schema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Update the properties of a schema object.|
|[Get schema](../api/synchronization-synchronizationjob-get-synchronizationschema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Read the properties and relationships of a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[Delete schema](../api/synchronization-synchronizationjob-delete-schema.md)|None|Delete a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[List synchronizationSchemas](../api/synchronization-synchronizationschema-list.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md) collection|Get a list of the [synchronizationSchema](../resources/synchronizationschema.md) objects and their properties.|
|[Create synchronizationSchema](../api/synchronization-synchronizationschema-create.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Create a new [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[Get synchronizationSchema](../api/synchronization-synchronizationschema-get.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Read the properties and relationships of a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[Update synchronizationSchema](../api/synchronization-synchronizationschema-update.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Update the properties of a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[Delete synchronizationSchema](../api/synchronization-synchronizationschema-delete.md)|None|Deletes a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[functions](../api/synchronization-synchronizationschema-functions.md)|[attributeMappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md) collection|**TODO: Add Description**|
|[filterOperators](../api/synchronization-synchronizationschema-filteroperators.md)|[filterOperatorSchema](../resources/synchronization-filteroperatorschema.md) collection|**TODO: Add Description**|
|[parseExpression](../api/synchronization-synchronizationschema-parseexpression.md)|[parseExpressionResponse](../resources/synchronization-parseexpressionresponse.md)|**TODO: Add Description**|
|[List directories](../api/synchronization-synchronizationschema-list-directories.md)|[directoryDefinition](../resources/synchronization-directorydefinition.md) collection|Get the directoryDefinitions from the directories navigation property.|
|[Create directories](../api/synchronization-synchronizationschema-post-directories.md)|[directoryDefinition](../resources/synchronization-directorydefinition.md)|Create a new directories object.|
|[Get directories](../api/synchronization-synchronizationschema-get-directorydefinition.md)|[directoryDefinition](../resources/synchronization-directorydefinition.md)|Read the properties and relationships of a [directoryDefinition](../resources/synchronization-directorydefinition.md) object.|
|[Update directories](../api/synchronization-synchronizationschema-update-directories.md)|[directoryDefinition](../resources/synchronization-directorydefinition.md)|Update the properties of a directories object.|
|[Delete directories](../api/synchronization-synchronizationschema-delete-directories.md)|None|Delete a [directoryDefinition](../resources/synchronization-directorydefinition.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|synchronizationRules|[synchronizationRule](../resources/synchronization-synchronizationrule.md) collection|**TODO: Add Description**|
|version|String|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|directories|[directoryDefinition](../resources/synchronization-directorydefinition.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.synchronizationSchema",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.synchronizationSchema",
  "id": "String (identifier)",
  "synchronizationRules": [
    {
      "@odata.type": "microsoft.graph.synchronizationRule"
    }
  ],
  "version": "String"
}
```

