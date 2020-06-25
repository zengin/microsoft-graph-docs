---
title: "Update recoveryKeys"
description: "Update the properties of a recoveryKeys object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update recoveryKeys
Namespace: microsoft.graph

Update the properties of a recoveryKeys object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/concepts/permissions-reference.md).

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
PATCH /bitlocker/recoveryKeys
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [bitlockerRecoveryKey](../resources/bitlockerrecoverykey.md) object.

The following table shows the properties that are required when you create the [bitlockerRecoveryKey](../resources/bitlockerrecoverykey.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description**|
|createdDateTime|DateTimeOffset|**TODO: Add Description**|
|volumeType|volumeType|**TODO: Add Description**. Possible values are: `operatingSystemVolume`, `fixedDataVolume`, `removableDataVolume`, `unknownFutureValue`.|
|deviceId|String|**TODO: Add Description**|
|key|String|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [bitlockerRecoveryKey](../resources/bitlockerrecoverykey.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_recoverykeys"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/bitlocker/recoveryKeys
Content-Type: application/json
Content-length: 134

{
  "@odata.type": "#microsoft.graph.bitlockerRecoveryKey",
  "volumeType": "String",
  "deviceId": "String",
  "key": "String"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.bitlockerRecoveryKey",
  "id": "7edb30ed-30ed-7edb-ed30-db7eed30db7e",
  "createdDateTime": "String (timestamp)",
  "volumeType": "String",
  "deviceId": "String",
  "key": "String"
}
```

