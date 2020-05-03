---
title: "educationSynchronizationDataProvider resource type"
description: "Represents the source SIS schema. This allows the system to know how to map the incoming data to the Azure Active Directory (Azure AD) schema. "
author: "mmast-msft"
localization_priority: Normal
ms.prod: "education"
doc_type: resourcePageType
---

# educationSynchronizationDataProvider resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the source SIS schema. This allows the system to know how to map the incoming data to the Azure Active Directory (Azure AD) schema.

> **Note:** This complex type is abstract. Refer to the specific types of data providers listed.

## Derived types
| Type | Description |
|:-|:-|:-|
| [educationcsvdataprovider](educationcsvdataprovider.md) | Used with CSV files as the input source. |
| [educationpowerschooldataprovider](educationpowerschooldataprovider.md) | Used with PowerSchool as the input source. |
| [educationonerosterapidataprovider](educationonerosterapidataprovider.md) | Used with OneRoster API as the input source. |

## Properties

No properties are exposed by this type.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationSynchronizationDataProvider resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /resources/educationsynchronizationdataprovider.md:\r\n      A required document header is missing from the document: JSON representation"
  ]
}
-->