---
title: "identityProtectionRoot resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# identityProtectionRoot resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List identityProtectionRoots](../api/identityprotectionroot-list.md)|[identityProtectionRoot](../resources/identityprotectionroot.md) collection|Get a list of the [identityProtectionRoot](../resources/identityprotectionroot.md) objects and their properties.|
|[Create identityProtectionRoot](../api/identityprotectionroot-create.md)|[identityProtectionRoot](../resources/identityprotectionroot.md)|Create a new [identityProtectionRoot](../resources/identityprotectionroot.md) object.|
|[Get identityProtectionRoot](../api/identityprotectionroot-get.md)|[identityProtectionRoot](../resources/identityprotectionroot.md)|Read the properties and relationships of an [identityProtectionRoot](../resources/identityprotectionroot.md) object.|
|[Update identityProtectionRoot](../api/identityprotectionroot-update.md)|[identityProtectionRoot](../resources/identityprotectionroot.md)|Update the properties of an [identityProtectionRoot](../resources/identityprotectionroot.md) object.|
|[Delete identityProtectionRoot](../api/identityprotectionroot-delete.md)|None|Deletes an [identityProtectionRoot](../resources/identityprotectionroot.md) object.|
|[List riskDetections](../api/identityprotectionroot-list-riskdetections.md)|[riskDetection](../resources/riskdetection.md) collection|Get the riskDetections from the riskDetections navigation property.|
|[Create riskDetections](../api/identityprotectionroot-post-riskdetections.md)|[riskDetection](../resources/riskdetection.md)|Create a new riskDetections object.|
|[Get riskDetections](../api/identityprotectionroot-get-riskdetection.md)|[riskDetection](../resources/riskdetection.md)|Read the properties and relationships of a [riskDetection](../resources/riskdetection.md) object.|
|[Update riskDetections](../api/identityprotectionroot-update-riskdetections.md)|[riskDetection](../resources/riskdetection.md)|Update the properties of a riskDetections object.|
|[Delete riskDetections](../api/identityprotectionroot-delete-riskdetections.md)|None|Delete a [riskDetection](../resources/riskdetection.md) object.|
|[List riskyUsers](../api/identityprotectionroot-list-riskyusers.md)|[riskyUser](../resources/riskyuser.md) collection|Get the riskyUsers from the riskyUsers navigation property.|
|[Create riskyUsers](../api/identityprotectionroot-post-riskyusers.md)|[riskyUser](../resources/riskyuser.md)|Create a new riskyUsers object.|
|[Get riskyUsers](../api/identityprotectionroot-get-riskyuser.md)|[riskyUser](../resources/riskyuser.md)|Read the properties and relationships of a [riskyUser](../resources/riskyuser.md) object.|
|[Update riskyUsers](../api/identityprotectionroot-update-riskyusers.md)|[riskyUser](../resources/riskyuser.md)|Update the properties of a riskyUsers object.|
|[Delete riskyUsers](../api/identityprotectionroot-delete-riskyusers.md)|None|Delete a [riskyUser](../resources/riskyuser.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|riskDetections|[riskDetection](../resources/riskdetection.md) collection|**TODO: Add Description**|
|riskyUsers|[riskyUser](../resources/riskyuser.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.identityProtectionRoot",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.identityProtectionRoot",
  "id": "String (identifier)"
}
```

