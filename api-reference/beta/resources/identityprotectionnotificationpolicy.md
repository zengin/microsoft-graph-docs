---
title: "identityProtectionNotificationPolicy resource type"
description: "PROVIDE DESCRIPTION HERE"
localization_priority: Normal
author: "cloudhandler"
ms.prod: "microsoft-identity-platform"
doc_type: "resourcePageType"
---

# identityProtectionNotificationPolicy resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the settings for the Identity Protection  Weekly Digest e-mails and the Users flagged for risk e-mails.

For more information about Identity Protection notification settings, see [Azure Active Directory Identity Protection notifications](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-configure-notifications)

## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get identityProtectionNotificationPolicy](../api/identityprotectionnotificationpolicy-get.md) | [identityProtectionNotificationPolicy](identityprotectionnotificationpolicy.md) | Read properties and relationships of identityProtectionNotificationPolicy object. |

## Properties

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|description|String||
|displayName|String||
|userAlertsSettings|[userAlertsSettings](useralertssettings.md)||
|weeklyDigestSettings|[weeklyDigestSettings](weeklydigestsettings.md)||

## Relationships

None

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.identityProtectionNotificationPolicy",
  "baseType": ""
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "userAlertsSettings": {"@odata.type": "microsoft.graph.userAlertsSettings"},
  "weeklyDigestSettings": {"@odata.type": "microsoft.graph.weeklyDigestSettings"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "identityProtectionNotificationPolicy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->