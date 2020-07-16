---
title: "Task resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# Task resource type

Namespace: microsoft.graph

**TODO: Add Description**


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List tasks](../api/tasklist-list-tasks.md)|[Task](../resources/task.md) collection|Get the Tasks from the tasks navigation property.|
|[Create tasks](../api/tasklist-post-tasks.md)|[Task](../resources/task.md)|Create a new tasks object.|
|[Update tasks](../api/tasklist-update-tasks.md)|[Task](../resources/task.md)|Update the properties of a tasks object.|
|[Get tasks](../api/tasklist-get-task.md)|[Task](../resources/task.md)|Read the properties and relationships of a [Task](../resources/task.md) object.|
|[Delete tasks](../api/tasklist-delete-tasks.md)|None|Delete a [Task](../resources/task.md) object.|
|[List Tasks](../api/task-list.md)|[Task](../resources/task.md) collection|Get a list of the [Task](../resources/task.md) objects and their properties.|
|[Create Task](../api/task-post-tasks.md)|[Task](../resources/task.md)|Create a new [Task](../resources/task.md) object.|
|[Get Task](../api/task-get.md)|[Task](../resources/task.md)|Read the properties and relationships of a [Task](../resources/task.md) object.|
|[Update Task](../api/task-update.md)|[Task](../resources/task.md)|Update the properties of a [Task](../resources/task.md) object.|
|[Delete Task](../api/task-delete.md)|None|Deletes a [Task](../resources/task.md) object.|
|[List linkedResources](../api/task-list-linkedresources.md)|[linkedResource](../resources/linkedresource.md) collection|Get the linkedResources from the linkedResources navigation property.|
|[Create linkedResources](../api/task-post-linkedresources.md)|[linkedResource](../resources/linkedresource.md)|Create a new linkedResources object.|
|[Get linkedResources](../api/task-get-linkedresource.md)|[linkedResource](../resources/linkedresource.md)|Read the properties and relationships of a [linkedResource](../resources/linkedresource.md) object.|
|[Update linkedResources](../api/task-update-linkedresources.md)|[linkedResource](../resources/linkedresource.md)|Update the properties of a linkedResources object.|
|[Delete linkedResources](../api/task-delete-linkedresources.md)|None|Delete a [linkedResource](../resources/linkedresource.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|body|[itemBody](../resources/itembody.md)|**TODO: Add Description**|
|bodyLastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|completedDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|dueDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|importance|importance|**TODO: Add Description**. Possible values are: `low`, `normal`, `high`.|
|isReminderOn|Boolean|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|recurrence|[patternedRecurrence](../resources/patternedrecurrence.md)|**TODO: Add Description**|
|reminderDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|**TODO: Add Description**|
|status|taskStatus|**TODO: Add Description**. Possible values are: `notStarted`, `inProgress`, `completed`, `waitingOnOthers`, `deferred`.|
|title|String|**TODO: Add Description**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|linkedResources|[linkedResource](../resources/linkedresource.md) collection|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.Task",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.Task",
  "id": "String (identifier)",
  "body": {
    "@odata.type": "microsoft.graph.itemBody"
  },
  "completedDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "dueDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "importance": "String",
  "isReminderOn": "Boolean",
  "recurrence": {
    "@odata.type": "microsoft.graph.patternedRecurrence"
  },
  "reminderDateTime": {
    "@odata.type": "microsoft.graph.dateTimeTimeZone"
  },
  "status": "String",
  "title": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "bodyLastModifiedDateTime": "String (timestamp)"
}
```

