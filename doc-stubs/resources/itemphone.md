---
title: "itemPhone resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# itemPhone resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [itemFacet](../resources/itemfacet.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List phones](../api/profile-list-phones.md)|[itemPhone](../resources/itemphone.md) collection|Get the itemPhones from the phones navigation property.|
|[Create phones](../api/profile-post-phones.md)|[itemPhone](../resources/itemphone.md)|Create a new phones object.|
|[Update phones](../api/profile-update-phones.md)|[itemPhone](../resources/itemphone.md)|Update the properties of a phones object.|
|[Get phones](../api/profile-get-itemphone.md)|[itemPhone](../resources/itemphone.md)|Read the properties and relationships of an [itemPhone](../resources/itemphone.md) object.|
|[Delete phones](../api/profile-delete-phones.md)|None|Delete an [itemPhone](../resources/itemphone.md) object.|
|[List itemPhones](../api/itemphone-list.md)|[itemPhone](../resources/itemphone.md) collection|Get a list of the [itemPhone](../resources/itemphone.md) objects and their properties.|
|[Create itemPhone](../api/itemphone-create.md)|[itemPhone](../resources/itemphone.md)|Create a new [itemPhone](../resources/itemphone.md) object.|
|[Get itemPhone](../api/itemphone-get.md)|[itemPhone](../resources/itemphone.md)|Read the properties and relationships of an [itemPhone](../resources/itemphone.md) object.|
|[Update itemPhone](../api/itemphone-update.md)|[itemPhone](../resources/itemphone.md)|Update the properties of an [itemPhone](../resources/itemphone.md) object.|
|[Delete itemPhone](../api/itemphone-delete.md)|None|Deletes an [itemPhone](../resources/itemphone.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|allowedAudiences|allowedAudiences|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md). Possible values are: `me`, `family`, `contacts`, `groupMembers`, `organization`, `federatedOrganizations`, `everyone`, `unknownFutureValue`.|
|createdBy|[identitySet](../resources/identityset.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|createdDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|displayName|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|inference|[inferenceData](../resources/inferencedata.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|lastModifiedBy|[identitySet](../resources/identityset.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|number|String|**TODO: Add Description**|
|source|[personDataSource](../resources/persondatasource.md)|**TODO: Add Description** Inherited from [itemFacet](../resources/itemfacet.md)|
|type|phoneType|**TODO: Add Description**. Possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.itemPhone",
  "baseType": "microsoft.graph.itemFacet",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.itemPhone",
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
  "displayName": "String",
  "type": "String",
  "number": "String"
}
```

