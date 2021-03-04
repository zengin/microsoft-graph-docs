---
title: "Update legalHold"
description: "Update the properties of a legalHold object."
localization_priority: Normal
author: "mahage-msft"
ms.prod: "ediscovery"
doc_type: apiPageType
---

# Update legalHold

Namespace: microsoft.graph.ediscovery

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [legalHold](../resources/ediscovery-legalhold.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|eDiscovery.Read.All, eDiscovery.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

``` http
PATCH /compliance/ediscovery/cases/{caseId}/legalHolds/{legalholdId}
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body

In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance, don't include existing values that haven't changed.

|Property|Type|Description|
|:---|:---|:---|
|contentQuery|String|KQL query that specifies content to be held in the specified locations. For more information about KQL in eDiscovery, see [Keyword queries and search conditions for Content Search and eDiscovery](/microsoft-365/compliance/keyword-queries-and-search-conditions). To hold all content in the specified locations, leave **contentQuery** blank. |
|description|String| The legal hold description. |
|displayName|String| The display name of the legal hold. |
|isEnabled|Boolean|Indicates whether the hold is enabled and actively holding content. |

## Response

If successful, this action returns a `204 No Content` response code.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_legalhold"
}
-->

``` http
PATCH https://graph.microsoft.com/beta/compliance/ediscovery/cases/{caseId}/legalHolds/{legalholdId}
Content-Type: application/json
Content-length: 295

{
  "description": "This is a description for a legalHold"
}
```

### Response

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.ediscovery.legalHold"
}
-->

``` http
HTTP/1.1 204 No Content
```
