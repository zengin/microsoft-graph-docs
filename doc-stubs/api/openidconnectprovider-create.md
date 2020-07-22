---
title: "Create openIdConnectProvider"
description: "Create a new openIdConnectProvider object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create openIdConnectProvider
Namespace: microsoft.graph

Create a new [openIdConnectProvider](../resources/openidconnectprovider.md) object.

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
POST ** Collection URI for microsoft.graph.openIdConnectProvider not found
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [openIdConnectProvider](../resources/openidconnectprovider.md) object.

The following table shows the properties that are required when you create the [openIdConnectProvider](../resources/openidconnectprovider.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|type|String|**TODO: Add Description** Inherited from [identityProvider](../resources/identityprovider.md)|
|name|String|**TODO: Add Description** Inherited from [identityProvider](../resources/identityprovider.md)|
|clientId|String|**TODO: Add Description** Inherited from [identityProvider](../resources/identityprovider.md)|
|clientSecret|String|**TODO: Add Description** Inherited from [identityProvider](../resources/identityprovider.md)|
|scope|String|**TODO: Add Description**|
|metadataUrl|String|**TODO: Add Description**|
|domainHint|String|**TODO: Add Description**|
|responseType|openIdConnectResponseTypes|**TODO: Add Description**. Possible values are: `code`, `id_token`, `token`.|
|responseMode|openIdConnectResponseMode|**TODO: Add Description**. Possible values are: `form_post`, `query`, `unknownFutureValue`.|
|claimsMapping|[claimsMapping](../resources/claimsmapping.md)|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and an [openIdConnectProvider](../resources/openidconnectprovider.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_openidconnectprovider_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta** Collection URI for microsoft.graph.openIdConnectProvider not found
Content-Type: application/json
Content-length: 374

{
  "@odata.type": "#microsoft.graph.openIdConnectProvider",
  "type": "String",
  "name": "String",
  "clientId": "String",
  "clientSecret": "String",
  "scope": "String",
  "metadataUrl": "String",
  "domainHint": "String",
  "responseType": "String",
  "responseMode": "String",
  "claimsMapping": {
    "@odata.type": "microsoft.graph.claimsMapping"
  }
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.openIdConnectProvider"
}
-->
``` http
HTTP/1.1 201 Created

Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.openIdConnectProvider",
  "id": "721f00e0-00e0-721f-e000-1f72e0001f72",
  "type": "String",
  "name": "String",
  "clientId": "String",
  "clientSecret": "String",
  "scope": "String",
  "metadataUrl": "String",
  "domainHint": "String",
  "responseType": "String",
  "responseMode": "String",
  "claimsMapping": {
    "@odata.type": "microsoft.graph.claimsMapping"
  }
}
```

