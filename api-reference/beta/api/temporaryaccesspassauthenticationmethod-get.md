---
title: "Get temporaryAccessPassAuthenticationMethod"
description: "Read the properties and relationships of a temporaryAccessPassAuthenticationMethod object."
author: "inbarckMS"
ms.author: inbarc
localization_priority: Normal
ms.prod: "microsoft-identity-platform"
doc_type: apiPageType
---

# Get temporaryAccessPassAuthenticationMethod
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve a user's single  [temporaryAccessPassAuthenticationMethod](../resources/temporaryaccesspassauthenticationmethod.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

### Permissions acting on self

|Permission type      | Permissions (from least to most privileged)              |
|:---------------------------------------|:-------------------------|
| Delegated (work or school account)     | UserAuthenticationMethod.Read, UserAuthenticationMethod.ReadWrite |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Not supported. |

### Permissions acting on other users

|Permission type      | Permissions (from least to most privileged)              |
|:---------------------------------------|:-------------------------|:-----------------|
| Delegated (work or school account)     | UserAuthenticationMethod.Read.All, UserAuthenticationMethod.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | UserAuthenticationMethod.Read.All, UserAuthenticationMethod.ReadWrite.All |

For delegated scenarios where an admin is acting on another user, the admin needs [one of the following roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):
* Global admin
* Global reader
* Privileged authentication admin
* Authentication admin

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /me/authentication/temporaryAccessPassMethods/{temporaryAccessPassAuthenticationMethodId}
GET /users/{id | userPrincipalName}/authentication/temporaryAccessPassMethods/{temporaryAccessPassAuthenticationMethodId}
```


## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|


## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [temporaryAccessPassAuthenticationMethod](../resources/temporaryaccesspassauthenticationmethod.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_temporaryaccesspassauthenticationmethod"
}
-->
``` http
GET https://graph.microsoft.com/beta/users/kim@contoso.com/authentication/temporaryAccessPassMethods/30fd0dfc-0dfc-30fd-fc0d-fd30fc0dfd30
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.temporaryAccessPassAuthenticationMethod"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.temporaryAccessPassAuthenticationMethod",
    "id": "30fd0dfc-0dfc-30fd-fc0d-fd30fc0dfd30",
    "temporaryAccessPass": null,
    "createdDateTime": "String (timestamp)",
    "startDateTime": "String (timestamp)",
    "lifetimeInMinutes": "Integer",
    "isUsableOnce": "Boolean",
    "isUsable": "Boolean",
    "methodUsabilityReason": "String"
  }
}
```
