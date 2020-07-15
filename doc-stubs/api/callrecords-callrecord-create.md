---
title: "Create callRecord"
description: "Create a new callRecord object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create callRecord
Namespace: microsoft.graph.callRecords

Create a new [callRecord](../resources/callrecords-callrecord.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /communications/callRecords
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [callRecord](../resources/callrecords-callrecord.md) object.

The following table shows the properties that are required when you create the [callRecord](../resources/callrecords-callrecord.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/callrecords-entity.md)|
|version|Int64|**TODO: Add Description**|
|type|callType|**TODO: Add Description**. Possible values are: `unknown`, `groupCall`, `peerToPeer`, `unknownFutureValue`.|
|modalities|modality collection|**TODO: Add Description**. Possible values are: `audio`, `video`, `videoBasedScreenSharing`, `data`, `screenSharing`, `unknownFutureValue`.|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description**|
|startDateTime|DateTimeOffset|**TODO: Add Description**|
|endDateTime|DateTimeOffset|**TODO: Add Description**|
|organizer|[identitySet](../resources/callrecords-identityset.md)|**TODO: Add Description**|
|participants|[identitySet](../resources/callrecords-identityset.md) collection|**TODO: Add Description**|
|joinWebUrl|String|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [callRecord](../resources/callrecords-callrecord.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_callrecord_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/communications/callRecords
Content-Type: application/json
Content-length: 425

{
  "@odata.type": "#microsoft.graph.callRecords.callRecord",
  "version": "Integer",
  "type": "String",
  "modalities": [
    "String"
  ],
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "organizer": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "participants": [
    {
      "@odata.type": "microsoft.graph.identitySet"
    }
  ],
  "joinWebUrl": "String"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.callRecords.callRecord"
}
-->
``` http
HTTP/1.1 201 Created

Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.callRecords.callRecord",
  "id": "abd12e3d-2e3d-abd1-3d2e-d1ab3d2ed1ab",
  "version": "Integer",
  "type": "String",
  "modalities": [
    "String"
  ],
  "lastModifiedDateTime": "String (timestamp)",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "organizer": {
    "@odata.type": "microsoft.graph.identitySet"
  },
  "participants": [
    {
      "@odata.type": "microsoft.graph.identitySet"
    }
  ],
  "joinWebUrl": "String"
}
```

