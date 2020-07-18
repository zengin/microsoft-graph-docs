---
title: "List accessReviews"
description: "Retrieve a list of access review definitions."
localization_priority: Normal
author: "raprakasMSFT"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# List accessReviews

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Retrieve a list of [accessReviewScheduleDefinition](../resources/accesspackage.md) objects.  The resulting list includes all the access reviews that the caller has access to read.

## Permissions

The following permissions and/or roles are required for a calling user to list access reviews.

| Target resource | Operation | Application permissions | Required directory role of the calling user |
|:----------------|:------------------|:------------|:--------------------------------------------|
|[accessReviewScheduleDefinition](accessreviewscheduledefinition.md) of a group or app | Read | AccessReview.Read.All, AccessReview.ReadWrite.Membership or AccessReview.ReadWrite.All | Global Administrator, Security Administrator, Security Reader or User Administrator |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
GET /identityGovernance/accessReviews/definitions
```

## Optional query parameters

This method supports some of the OData query parameters to help customize the response. For example, to retrieve the access package policies for each access package, add `$expand=accessPackageAssignmentPolicies`. To search for access packages with a particular name, include a filter such as `$filter=contains(tolower(displayName),'team')` in the query. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization | Bearer \{token\}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [accessReviewScheduleDefition](../resources/accesspackage.md) objects in the response body.

## Examples

### Request

The following is an example of the request.

# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_accesspackages"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/identityGovernance/accessReviews/definitions
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-accesspackages-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-accesspackages-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-accesspackages-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessPackage",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
      "value": [
        {
            "id": "4cd7a57f-07a9-4e89-83d8-f2fc1fd764ef",
            "displayName": "Access Reviews Display Name",
            "createdDateTime": "2020-07-15T18:42:33.2275259Z",
            "lastModifiedDateTime": "2020-07-15T18:43:05Z",
            "status": "InProgress",
            "descriptionForAdmins": "This is an internal description for administrators",
            "descriptionForReviewers": "This is a description that is sent to reviewers",
            "createdBy": {
                "id": "0cb75d4c-b81b-4e82-bd8c-0f2afc174cf8",
                "displayName": "Meghan Bowen",
                "userPrincipalName": "admin@M365x998010.onmicrosoft.com"
            },
            "scope": {
                "query": "/groups/273f86d7-d0e5-4429-8eaf-06fadf3a5d61/transitiveMembers/microsoft.graph.user/?$count=true&$filter=(userType eq 'Guest')",
                "queryType": "MicrosoftGraph"
            },
            "reviewers": [
                {
                    "query": "/users/0cb75d4c-b81b-4e82-bd8c-0f2afc174cf8",
                    "queryType": "MicrosoftGraph"
                }
            ],
            "settings": {
                "mailNotificationsEnabled": true,
                "reminderNotificationsEnabled": true,
                "justificationRequiredOnApproval": true,
                "defaultDecisionEnabled": false,
                "defaultDecision": "None",
                "instanceDurationInDays": 0,
                "autoApplyDecisionsEnabled": true,
                "recommendationsEnabled": true,
                "recurrence": {
                    "pattern": null,
                    "range": {
                        "type": "numbered",
                        "numberOfOccurrences": 0,
                        "recurrenceTimeZone": null,
                        "startDate": "2020-07-16",
                        "endDate": "9999-12-31"
                    }
                },
                "applyActions": [
                    {
                        "@odata.type": "#microsoft.graph.removeAccessApplyAction"
                    }
                ]
            }
        }
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List accessPackages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
