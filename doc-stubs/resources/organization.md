---
title: "organization resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# organization resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List organizations](../api/organization-list.md)|[organization](../resources/organization.md) collection|Get a list of the [organization](../resources/organization.md) objects and their properties.|
|[Create organization](../api/organization-create.md)|[organization](../resources/organization.md)|Create a new [organization](../resources/organization.md) object.|
|[Get organization](../api/organization-get.md)|[organization](../resources/organization.md)|Read the properties and relationships of an [organization](../resources/organization.md) object.|
|[Update organization](../api/organization-update.md)|[organization](../resources/organization.md)|Update the properties of an [organization](../resources/organization.md) object.|
|[Delete organization](../api/organization-delete.md)|None|Deletes an [organization](../resources/organization.md) object.|
|[List settings](../api/organization-list-settings.md)|[organizationSettings](../resources/organizationsettings.md) collection|Get the organizationSettings from the settings navigation property.|
|[Create settings](../api/organization-post-settings.md)|[organizationSettings](../resources/organizationsettings.md)|Create a new settings object.|
|[Get settings](../api/organization-get-organizationsettings.md)|[organizationSettings](../resources/organizationsettings.md)|Read the properties and relationships of an [organizationSettings](../resources/organizationsettings.md) object.|
|[Update settings](../api/organization-update-settings.md)|[organizationSettings](../resources/organizationsettings.md)|Update the properties of a settings object.|
|[Delete settings](../api/organization-delete-settings.md)|None|Delete an [organizationSettings](../resources/organizationsettings.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|settings|[organizationSettings](../resources/organizationsettings.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.organization",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.organization",
  "id": "String (identifier)"
}
```

