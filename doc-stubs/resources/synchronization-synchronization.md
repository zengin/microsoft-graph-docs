---
title: "synchronization resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# synchronization resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List synchronizations](../api/synchronization-synchronization-list.md)|[synchronization](../resources/synchronization-synchronization.md) collection|Get a list of the [synchronization](../resources/synchronization.md) objects and their properties.|
|[Create synchronization](../api/synchronization-synchronization-create.md)|[synchronization](../resources/synchronization-synchronization.md)|Create a new [synchronization](../resources/synchronization-synchronization.md) object.|
|[Get synchronization](../api/synchronization-synchronization-get.md)|[synchronization](../resources/synchronization-synchronization.md)|Read the properties and relationships of a [synchronization](../resources/synchronization-synchronization.md) object.|
|[Update synchronization](../api/synchronization-synchronization-update.md)|[synchronization](../resources/synchronization-synchronization.md)|Update the properties of a [synchronization](../resources/synchronization-synchronization.md) object.|
|[Delete synchronization](../api/synchronization-synchronization-delete.md)|None|Deletes a [synchronization](../resources/synchronization-synchronization.md) object.|
|[Ping](../api/synchronization-synchronization-ping.md)|String|**TODO: Add Description**|
|[List jobs](../api/synchronization-synchronization-list-jobs.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md) collection|Get the synchronizationJobs from the jobs navigation property.|
|[Create jobs](../api/synchronization-synchronization-post-jobs.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Create a new jobs object.|
|[Get jobs](../api/synchronization-synchronization-get-synchronizationjob.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Read the properties and relationships of a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[Update jobs](../api/synchronization-synchronization-update-jobs.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Update the properties of a jobs object.|
|[Delete jobs](../api/synchronization-synchronization-delete-jobs.md)|None|Delete a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[List templates](../api/synchronization-synchronization-list-templates.md)|[synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) collection|Get the synchronizationTemplates from the templates navigation property.|
|[Create templates](../api/synchronization-synchronization-post-templates.md)|[synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md)|Create a new templates object.|
|[Get templates](../api/synchronization-synchronization-get-synchronizationtemplate.md)|[synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md)|Read the properties and relationships of a [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object.|
|[Update templates](../api/synchronization-synchronization-update-templates.md)|[synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md)|Update the properties of a templates object.|
|[Delete templates](../api/synchronization-synchronization-delete-templates.md)|None|Delete a [synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|secrets|[synchronizationSecretKeyStringValuePair](../resources/synchronization-synchronizationsecretkeystringvaluepair.md) collection|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|jobs|[synchronizationJob](../resources/synchronization-synchronizationjob.md) collection|**TODO: Add Description**|
|templates|[synchronizationTemplate](../resources/synchronization-synchronizationtemplate.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.synchronization",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.synchronization",
  "id": "String (identifier)",
  "secrets": [
    {
      "@odata.type": "microsoft.graph.synchronizationSecretKeyStringValuePair"
    }
  ]
}
```

