---
title: "Update identityProtectionRoot"
description: "Update the properties of an identityProtectionRoot object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update identityProtectionRoot
Namespace: microsoft.graph

Update the properties of an [identityProtectionRoot](../resources/identityprotectionroot.md) object.

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
PATCH /identityProtection
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [identityProtectionRoot](../resources/identityprotectionroot.md) object.

The following table shows the properties that are required when you create the [identityProtectionRoot](../resources/identityprotectionroot.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|



## Response

If successful, this method returns a `200 OK` response code and an updated [identityProtectionRoot](../resources/identityprotectionroot.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_identityprotectionroot"
}
-->
``` http
PATCH https://graph.microsoft.com/v1.0/identityProtection
Content-Type: application/json
Content-length: 64

{
  "@odata.type": "#microsoft.graph.identityProtectionRoot"
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
  "@odata.type": "#microsoft.graph.identityProtectionRoot",
  "id": "f27ca582-a582-f27c-82a5-7cf282a57cf2"
}
```

