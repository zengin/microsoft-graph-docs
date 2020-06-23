---
title: "synchronizationJob resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# synchronizationJob resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List jobs](../api/synchronization-synchronization-list-jobs.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md) collection|Get the synchronizationJobs from the jobs navigation property.|
|[Create jobs](../api/synchronization-synchronization-post-jobs.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Create a new jobs object.|
|[Update jobs](../api/synchronization-synchronization-update-jobs.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Update the properties of a jobs object.|
|[Get jobs](../api/synchronization-synchronization-get-synchronizationjob.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Read the properties and relationships of a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[Delete jobs](../api/synchronization-synchronization-delete-jobs.md)|None|Delete a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[List synchronizationJobs](../api/synchronization-synchronizationjob-list.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md) collection|Get a list of the [synchronizationJob](../resources/synchronizationjob.md) objects and their properties.|
|[Create synchronizationJob](../api/synchronization-synchronizationjob-create.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Create a new [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[Get synchronizationJob](../api/synchronization-synchronizationjob-get.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Read the properties and relationships of a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[Update synchronizationJob](../api/synchronization-synchronizationjob-update.md)|[synchronizationJob](../resources/synchronization-synchronizationjob.md)|Update the properties of a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[Delete synchronizationJob](../api/synchronization-synchronizationjob-delete.md)|None|Deletes a [synchronizationJob](../resources/synchronization-synchronizationjob.md) object.|
|[pause](../api/synchronization-synchronizationjob-pause.md)|None|**TODO: Add Description**|
|[provisionOnDemand](../api/synchronization-synchronizationjob-provisionondemand.md)|[stringKeyStringValuePair](../resources/synchronization-stringkeystringvaluepair.md)|**TODO: Add Description**|
|[start](../api/synchronization-synchronizationjob-start.md)|None|**TODO: Add Description**|
|[stop](../api/synchronization-synchronizationjob-stop.md)|None|**TODO: Add Description**|
|[restart](../api/synchronization-synchronizationjob-restart.md)|None|**TODO: Add Description**|
|[validateCredentials](../api/synchronization-synchronizationjob-validatecredentials.md)|None|**TODO: Add Description**|
|[validateCredentials](../api/synchronization-synchronizationjob-validatecredentials.md)|None|**TODO: Add Description**|
|[List schema](../api/synchronization-synchronizationjob-list-schema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md) collection|Get the synchronizationSchemas from the schema navigation property.|
|[Create schema](../api/synchronization-synchronizationjob-post-schema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Create a new schema object.|
|[Get schema](../api/synchronization-synchronizationjob-get-synchronizationschema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Read the properties and relationships of a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|
|[Update schema](../api/synchronization-synchronizationjob-update-schema.md)|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|Update the properties of a schema object.|
|[Delete schema](../api/synchronization-synchronizationjob-delete-schema.md)|None|Delete a [synchronizationSchema](../resources/synchronization-synchronizationschema.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|schedule|[synchronizationSchedule](../resources/synchronization-synchronizationschedule.md)|**TODO: Add Description**|
|status|[synchronizationStatus](../resources/synchronization-synchronizationstatus.md)|**TODO: Add Description**|
|synchronizationJobSettings|[keyValuePair](../resources/synchronization-keyvaluepair.md) collection|**TODO: Add Description**|
|templateId|String|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|schema|[synchronizationSchema](../resources/synchronization-synchronizationschema.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.synchronizationJob",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.synchronizationJob",
  "id": "String (identifier)",
  "schedule": {
    "@odata.type": "microsoft.graph.synchronizationSchedule"
  },
  "status": {
    "@odata.type": "microsoft.graph.synchronizationStatus"
  },
  "templateId": "String",
  "synchronizationJobSettings": [
    {
      "@odata.type": "microsoft.graph.keyValuePair"
    }
  ]
}
```

