---
title: "Create servicePrincipal"
description: "Create a new servicePrincipal object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create servicePrincipal
Namespace: microsoft.graph

Create a new [servicePrincipal](../resources/serviceprincipal.md) object.

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
POST /servicePrincipals
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [servicePrincipal](../resources/serviceprincipal.md) object.

The following table shows the properties that are required when you create the [servicePrincipal](../resources/serviceprincipal.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|



## Response

If successful, this method returns a `201 Created` response code and a [servicePrincipal](../resources/serviceprincipal.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_serviceprincipal_from_serviceprincipals"
}
-->
``` http
POST https://graph.microsoft.com/beta/servicePrincipals
Content-Type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.servicePrincipal"
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.serviceprincipal"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.servicePrincipal",
  "id": "a99981b7-81b7-a999-b781-99a9b78199a9"
}
```

