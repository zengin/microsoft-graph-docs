---
title: "Update bookingNamedEntity"
description: "Update the properties of a bookingNamedEntity object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update bookingNamedEntity
Namespace: microsoft.graph

Update the properties of a [bookingNamedEntity](../resources/bookingnamedentity.md) object.

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
PATCH /bookingNamedEntity
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [bookingNamedEntity](../resources/bookingnamedentity.md) object.

The following table shows the properties that are required when you create the [bookingNamedEntity](../resources/bookingnamedentity.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|displayName|String|**TODO: Add Description**|



## Response

If successful, this method returns a `200 OK` response code and an updated [bookingNamedEntity](../resources/bookingnamedentity.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_bookingnamedentity"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/bookingNamedEntity
Content-Type: application/json
Content-length: 88

{
  "@odata.type": "#microsoft.graph.bookingNamedEntity",
  "displayName": "String"
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
  "@odata.type": "#microsoft.graph.bookingNamedEntity",
  "id": "3fb8cd5b-cd5b-3fb8-5bcd-b83f5bcdb83f",
  "displayName": "String"
}
```

