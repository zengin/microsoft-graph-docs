---
title: Update printJob configuration
description: Update the configuration of a print job
author: tomsato-ms
localization_priority: Normal
ms.prod: cloud-printing
doc_type: apiPageType
---

# Update printJob configuration

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the [configuration](../resources/printjobconfiguration.md) property of a [print job](../resources/printjob.md).

Updating a print job configuration will only succeed if there is a [printTask](../resources/printTask.md) in `processing` state on the associated print job, started by a trigger that requesting app created. For details about how to register a task trigger, see [Extending Universal Print to support pull printing](/graph/universal-print-concept-overview#extending-universal-print-to-support-pull-printing).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

To use the Universal Print service, the user or app's tenant must have an active Universal Print subscription, either the Printer.Read.All or Printer.ReadWrite.All application permission, and one of the permissions listed in the following table.

|Permission type | Permissions (from least to most privileged) |
|:---------------|:--------------------------------------------|
|Delegated (work or school account)| Not supported. |
|Delegated (personal Microsoft account)|Not Supported.|
|Application| PrintJob.ReadWriteBasic.All, PrintJob.ReadWrite.All |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /print/printers/{id}/jobs/{id}/configuration
```
## Request headers
| Name          | Description   |
|:--------------|:--------------|
| Authorization | Bearer {token}. Required. |

## Request body
In the request body, supply the values of the relevant [printJobConfiguration](../resources/printjobconfiguration.md) fields. Existing properties that are not included in the request body will maintain their previous values.

## Response
If successful, this method returns a `204 No Content` response code.

## Example
The following example shows how to call this API.
### Request
The following is an example of the request.


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "printjob-update-configuration"
}-->
```http
PATCH https://graph.microsoft.com/beta/print/printers/d5ef6ec4-07ca-4212-baf9-d45be126bfbb/jobs/44353/configuration

{
  "feedOrientation": "longEdgeFirst",
  "pageRanges": [
    {
      "start": 1,
      "end": 1
    }
  ],
  "quality": "medium",
  "dpi": 600,
  "orientation": "landscape",
  "copies": 1,
  "duplexMode": "oneSided",
  "colorMode": "blackAndWhite",
  "inputBin": "by-pass-tray",
  "outputBin": "output-tray",
  "mediaSize": "A4",
  "margin": {
    "top": 0,
    "bottom": 0,
    "left": 0,
    "right": 0
  },
  "mediaType": "stationery",
  "finishings": null,
  "pagesPerSheet": 1,
  "multipageLayout": "clockwiseFromBottomLeft",
  "collate": false,
  "scaling": "shrinkToFit",
  "fitPdfToPage": false
}
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/printjob-update-configuration-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/printjob-update-configuration-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/printjob-update-configuration-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/printjob-update-configuration-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


---


### Response
The following is an example of the response. 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update print job configuration",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->


