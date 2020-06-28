---
title: "Update userScopeTeamsAppInstallation"
description: "Update the properties of a userScopeTeamsAppInstallation object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update userScopeTeamsAppInstallation
Namespace: microsoft.graph

Update the properties of a [userScopeTeamsAppInstallation](../resources/userscopeteamsappinstallation.md) object.

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
PATCH ** Entity URI for microsoft.graph.userScopeTeamsAppInstallation not found
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [userScopeTeamsAppInstallation](../resources/userscopeteamsappinstallation.md) object.

The following table shows the properties that are required when you create the [userScopeTeamsAppInstallation](../resources/userscopeteamsappinstallation.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|



## Response

If successful, this method returns a `200 OK` response code and an updated [userScopeTeamsAppInstallation](../resources/userscopeteamsappinstallation.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_userscopeteamsappinstallation"
}
-->
``` http
PATCH https://graph.microsoft.com/beta** Entity URI for microsoft.graph.userScopeTeamsAppInstallation not found
Content-Type: application/json
Content-length: 71

{
  "@odata.type": "#microsoft.graph.userScopeTeamsAppInstallation"
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
  "@odata.type": "#microsoft.graph.userScopeTeamsAppInstallation",
  "id": "640b5bcc-5bcc-640b-cc5b-0b64cc5b0b64"
}
```

