---
title: "educationSynchronizationConnectionSettings resource type"
description: "Represents the provider connection settings. This allows the system to know how to connect to the provider APIs. "
author: "mmast-msft"
localization_priority: Normal
ms.prod: "education"
doc_type: resourcePageType
---

# educationSynchronizationConnectionSettings resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the provider connection settings. This allows the system to know how to connect to the provider APIs. 

> **Note:** This complex type is abstract. Refer to the specific types of connection settings listed.

## Derived types
| Type | Description | 
|:-|:-|
| [**educationSynchronizationOAuth1ConnectionSettings**](educationsynchronizationoauth1connectionsettings.md) | Use this type to provide OAuth1 connection settings. |
| [**educationSynchronizationOAuth2ClientCredentialsConnectionSettings**](educationsynchronizationoauth2clientcredentialsconnectionsettings.md) | Use this type to provide OAuth2 Client Credentials Grant connection settings. |

## Properties

| Property | Type | Description |
|:-|:-|:-|
| **clientId** | String |  Client ID used to connect to the provider. |
| **clientSecret** | String |  Client secret to authenticate the connection to the provider. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationSynchronizationConnectionSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /resources/educationsynchronizationconnectionsettings.md:\r\n      A required document header is missing from the document: JSON representation"
  ]
}
-->