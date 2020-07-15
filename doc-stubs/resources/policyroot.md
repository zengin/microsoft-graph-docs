---
title: "policyRoot resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# policyRoot resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List policyRoots](../api/policyroot-list.md)|[policyRoot](../resources/policyroot.md) collection|Get a list of the [policyRoot](../resources/policyroot.md) objects and their properties.|
|[Create policyRoot](../api/policyroot-create.md)|[policyRoot](../resources/policyroot.md)|Create a new [policyRoot](../resources/policyroot.md) object.|
|[Get policyRoot](../api/policyroot-get.md)|[policyRoot](../resources/policyroot.md)|Read the properties and relationships of a [policyRoot](../resources/policyroot.md) object.|
|[Update policyRoot](../api/policyroot-update.md)|[policyRoot](../resources/policyroot.md)|Update the properties of a [policyRoot](../resources/policyroot.md) object.|
|[Delete policyRoot](../api/policyroot-delete.md)|None|Deletes a [policyRoot](../resources/policyroot.md) object.|
|[List authorizationPolicy](../api/policyroot-list-authorizationpolicy.md)|[authorizationPolicy](../resources/authorizationpolicy.md) collection|Get the authorizationPolicies from the authorizationPolicy navigation property.|
|[Create authorizationPolicy](../api/policyroot-post-authorizationpolicy.md)|[authorizationPolicy](../resources/authorizationpolicy.md)|Create a new authorizationPolicy object.|
|[Get authorizationPolicy](../api/policyroot-get-authorizationpolicy.md)|[authorizationPolicy](../resources/authorizationpolicy.md)|Read the properties and relationships of an [authorizationPolicy](../resources/authorizationpolicy.md) object.|
|[Update authorizationPolicy](../api/policyroot-update-authorizationpolicy.md)|[authorizationPolicy](../resources/authorizationpolicy.md)|Update the properties of an authorizationPolicy object.|
|[Delete authorizationPolicy](../api/policyroot-delete-authorizationpolicy.md)|None|Delete an [authorizationPolicy](../resources/authorizationpolicy.md) object.|
|[List permissionGrantPolicies](../api/policyroot-list-permissiongrantpolicies.md)|[permissionGrantPolicy](../resources/permissiongrantpolicy.md) collection|Get the permissionGrantPolicies from the permissionGrantPolicies navigation property.|
|[Create permissionGrantPolicies](../api/policyroot-post-permissiongrantpolicies.md)|[permissionGrantPolicy](../resources/permissiongrantpolicy.md)|Create a new permissionGrantPolicies object.|
|[Get permissionGrantPolicies](../api/policyroot-get-permissiongrantpolicy.md)|[permissionGrantPolicy](../resources/permissiongrantpolicy.md)|Read the properties and relationships of a [permissionGrantPolicy](../resources/permissiongrantpolicy.md) object.|
|[Update permissionGrantPolicies](../api/policyroot-update-permissiongrantpolicies.md)|[permissionGrantPolicy](../resources/permissiongrantpolicy.md)|Update the properties of a permissionGrantPolicies object.|
|[Delete permissionGrantPolicies](../api/policyroot-delete-permissiongrantpolicies.md)|None|Delete a [permissionGrantPolicy](../resources/permissiongrantpolicy.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|activityBasedTimeoutPolicies|[activityBasedTimeoutPolicy](../resources/activitybasedtimeoutpolicy.md) collection|**TODO: Add Description**|
|authorizationPolicy|[authorizationPolicy](../resources/authorizationpolicy.md) collection|**TODO: Add Description**|
|claimsMappingPolicies|[claimsMappingPolicy](../resources/claimsmappingpolicy.md) collection|**TODO: Add Description**|
|homeRealmDiscoveryPolicies|[homeRealmDiscoveryPolicy](../resources/homerealmdiscoverypolicy.md) collection|**TODO: Add Description**|
|permissionGrantPolicies|[permissionGrantPolicy](../resources/permissiongrantpolicy.md) collection|**TODO: Add Description**|
|tokenIssuancePolicies|[tokenIssuancePolicy](../resources/tokenissuancepolicy.md) collection|**TODO: Add Description**|
|tokenLifetimePolicies|[tokenLifetimePolicy](../resources/tokenlifetimepolicy.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.policyRoot",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.policyRoot",
  "id": "String (identifier)"
}
```

