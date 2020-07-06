---
title: "webAccount resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# webAccount resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [itemFacet](../resources/itemfacet.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List webAccounts](../api/profile-list-webaccounts.md)|[webAccount](../resources/webaccount.md) collection|Get the webAccounts from the webAccounts navigation property.|
|[Create webAccounts](../api/profile-post-webaccounts.md)|[webAccount](../resources/webaccount.md)|Create a new webAccounts object.|
|[Update webAccounts](../api/profile-update-webaccounts.md)|[webAccount](../resources/webaccount.md)|Update the properties of a webAccounts object.|
|[Get webAccounts](../api/profile-get-webaccount.md)|[webAccount](../resources/webaccount.md)|Read the properties and relationships of a [webAccount](../resources/webaccount.md) object.|
|[Delete webAccounts](../api/profile-delete-webaccounts.md)|None|Delete a [webAccount](../resources/webaccount.md) object.|
|[List webAccounts](../api/webaccount-list.md)|[webAccount](../resources/webaccount.md) collection|Get a list of the [webAccount](../resources/webaccount.md) objects and their properties.|
|[Create webAccount](../api/webaccount-create.md)|[webAccount](../resources/webaccount.md)|Create a new [webAccount](../resources/webaccount.md) object.|
|[Get webAccount](../api/webaccount-get.md)|[webAccount](../resources/webaccount.md)|Read the properties and relationships of a [webAccount](../resources/webaccount.md) object.|
|[Update webAccount](../api/webaccount-update.md)|[webAccount](../resources/webaccount.md)|Update the properties of a [webAccount](../resources/webaccount.md) object.|
|[Delete webAccount](../api/webaccount-delete.md)|None|Deletes a [webAccount](../resources/webaccount.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|allowedAudiences|allowedAudiences|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md). Possible values are: `me`, `family`, `contacts`, `groupMembers`, `organization`, `federatedOrganizations`, `everyone`, `unknownFutureValue`.|
|createdBy|[identitySet](../resources/identityset.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|createdDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|description|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|inference|[inferenceData](../resources/inferencedata.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|lastModifiedBy|[identitySet](../resources/identityset.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|service|[serviceInformation](../resources/serviceinformation.md)|**TODO: Add Description**|
|source|[personDataSource](../resources/persondatasource.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|statusMessage|String|**TODO: Add Description**|
|userId|String|**TODO: Add Description**|
|webUrl|String|**TODO: Add Description**|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.webAccount",
  "baseType": "microsoft.graph.itemFacet",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.webAccount",
  "id": "String (identifier)",
  "allowedAudiences": "String",
  "inference": {
    "@odata.type": "microsoft.graph.inferenceData"
  },
  "createdDateTime": "String (timestamp)",
  "createdBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "lastModifiedDateTime": "String (timestamp)",
  "lastModifiedBy": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "source": {
    "@odata.type": "microsoft.graph.personDataSource"
  },
  "description": "String",
  "userId": "String",
  "service": {
    "@odata.type": "microsoft.graph.serviceInformation"
  },
  "statusMessage": "String",
  "webUrl": "String"
}
```

