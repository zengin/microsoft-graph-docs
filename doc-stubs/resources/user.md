---
title: "user resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# user resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List invitedUser](../api/invitation-list-inviteduser.md)|[user](../resources/user.md) collection|Get the users from the invitedUser navigation property.|
|[Add invitedUser](../api/invitation-post-inviteduser.md)|[user](../resources/user.md)|Add invitedUser by posting to the invitedUser collection.|
|[Remove invitedUser](../api/invitation-delete-inviteduser.md)|None|Remove a [user](../resources/user.md) object.|
|[List users](../api/user-list.md)|[user](../resources/user.md) collection|Get a list of the [user](../resources/user.md) objects and their properties.|
|[Create user](../api/user-post-user.md)|[user](../resources/user.md)|Create a new [user](../resources/user.md) object.|
|[Get user](../api/user-get.md)|[user](../resources/user.md)|Read the properties and relationships of a [user](../resources/user.md) object.|
|[Update user](../api/user-update.md)|[user](../resources/user.md)|Update the properties of a [user](../resources/user.md) object.|
|[Delete user](../api/user-delete.md)|None|Deletes a [user](../resources/user.md) object.|
|[List profile](../api/user-list-profile.md)|[profile](../resources/profile.md) collection|Get the profiles from the profile navigation property.|
|[Create profile](../api/user-post-profile.md)|[profile](../resources/profile.md)|Create a new profile object.|
|[Get profile](../api/user-get-profile.md)|[profile](../resources/profile.md)|Read the properties and relationships of a [profile](../resources/profile.md) object.|
|[Update profile](../api/user-update-profile.md)|[profile](../resources/profile.md)|Update the properties of a profile object.|
|[Delete profile](../api/user-delete-profile.md)|None|Delete a [profile](../resources/profile.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|profile|[profile](../resources/profile.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.user",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.user",
  "id": "String (identifier)"
}
```

