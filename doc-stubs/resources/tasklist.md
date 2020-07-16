---
title: "TaskList resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# TaskList resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List TaskLists](../api/tasklist-list.md)|[TaskList](../resources/tasklist.md) collection|Get a list of the [TaskList](../resources/tasklist.md) objects and their properties.|
|[Create TaskList](../api/tasklist-post-lists.md)|[TaskList](../resources/tasklist.md)|Create a new [TaskList](../resources/tasklist.md) object.|
|[Get TaskList](../api/tasklist-get.md)|[TaskList](../resources/tasklist.md)|Read the properties and relationships of a [TaskList](../resources/tasklist.md) object.|
|[Update TaskList](../api/tasklist-update.md)|[TaskList](../resources/tasklist.md)|Update the properties of a [TaskList](../resources/tasklist.md) object.|
|[Delete TaskList](../api/tasklist-delete.md)|None|Deletes a [TaskList](../resources/tasklist.md) object.|
|[List tasks](../api/tasklist-list-tasks.md)|[Task](../resources/task.md) collection|Get the Tasks from the tasks navigation property.|
|[Create tasks](../api/tasklist-post-tasks.md)|[Task](../resources/task.md)|Create a new tasks object.|
|[Get tasks](../api/tasklist-get-task.md)|[Task](../resources/task.md)|Read the properties and relationships of a [Task](../resources/task.md) object.|
|[Update tasks](../api/tasklist-update-tasks.md)|[Task](../resources/task.md)|Update the properties of a tasks object.|
|[Delete tasks](../api/tasklist-delete-tasks.md)|None|Delete a [Task](../resources/task.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|displayName|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|isOwner|Boolean|**TODO: Add Description**|
|isShared|Boolean|**TODO: Add Description**|
|wellknownListName|wellknownListName|**TODO: Add Description**. Possible values are: `none`, `defaultList`, `flaggedEmails`, `unknownFutureValue`.|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|tasks|[Task](../resources/task.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.TaskList",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.TaskList",
  "id": "String (identifier)",
  "displayName": "String",
  "isOwner": "Boolean",
  "isShared": "Boolean",
  "wellknownListName": "String"
}
```

