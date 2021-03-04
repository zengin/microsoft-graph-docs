---
title: "application resource type"
description: "Represents an application."
localization_priority: Priority
author: "sureshja"
ms.prod: "applications"
doc_type: resourcePageType
---

# application resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents an application. Any application that outsources authentication to Azure Active Directory (Azure AD) must be registered in a directory. Application registration involves telling Azure AD about your application, including the URL where it's located, the URL to send replies after authentication, the URI to identify your application, and more. For more information, see [Basics of Registering an Application in Azure AD](/azure/active-directory/develop/authentication-vs-authorization#basics-of-registering-an-application-in-azure-ad). Inherits from [directoryObject](directoryobject.md).

> [!Note]
> Changes to the application resource type are currently in development. For more information, see [Known issues with Microsoft Graph](/graph/known-issues#application-and-serviceprincipal-api-changes).

This resource supports using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/application-delta.md) function.

## Methods

| Method | Return Type | Description |
|:---------------|:--------|:----------|
|[List applications](../api/application-list.md) | [application](application.md) collection | Retrieve the list of applications in the organization. |
|[Create application](../api/application-post-applications.md) | [application](application.md) | Creates (registers) a new application.|
|[Get application](../api/application-get.md) | [application](application.md) |Read properties and relationships of application object.|
|[Update application](../api/application-update.md) | [application](application.md) |Update application object. |
|[Delete application](../api/application-delete.md) | None |Delete application object. |
|[List deleted applications](../api/directory-deleteditems-list.md) | [directoryObject](directoryobject.md) collection | Retrieve a list of recently deleted applications. |
|[Get deleted application](../api/directory-deleteditems-get.md) | [directoryObject](directoryobject.md) | Retrieve the properties of a recently deleted application. |
|[Permanently delete application](../api/directory-deleteditems-delete.md) | None | Permanently delete an applications. |
|[Restore deleted application](../api/directory-deleteditems-restore.md) | [directoryObject](directoryobject.md) | Restore a recently deleted application. |
|[delta](../api/application-delta.md)|[application](application.md) collection| Get incremental changes for applications. |
|[Create call](../api/application-post-calls.md)|[call](call.md)|Create a new call by posting to the calls collection.|
|[Create online meeting](../api/application-post-onlinemeetings.md)|[onlineMeeting](onlinemeeting.md)|Create a new online meeting by posting to the onlineMeetings collection.|
|**Certificates and secrets**| | |
|[Add password](../api/application-addpassword.md)|[passwordCredential](passwordcredential.md)|Add a strong password to an application.|
|[Remove password](../api/application-removepassword.md)|[passwordCredential](passwordcredential.md)|Remove a password from an application.|
|[Add key](../api/application-addkey.md)|[keyCredential](keycredential.md)|Add a key credential to an application.|
|[Remove key](../api/application-removekey.md)|None|Remove a key credential from an application.|
|**Extensions**| | |
| [List extensions](../api/application-list-extensionproperty.md) | [extensionProperty](extensionProperty.md) collection | List extension properties on an application object. |
| [Create extension](../api/application-post-extensionproperty.md) | [extensionProperty](extensionProperty.md) | Create an extension property on an application object. |
| [Delete extension](../api/application-delete-extensionproperty.md) | None | Delete an extension property from an application object. |
|**Owners**| | |
|[List owners](../api/application-list-owners.md) |[directoryObject](directoryobject.md) collection| Get an owner object collection.|
|[Add owner](../api/application-post-owners.md) |[directoryObject](directoryobject.md)| Add an owner by posting to the owners collection.|
|[Remove owner](../api/application-delete-owners.md) |None| Remove an owner from an application.|
|**Policies**| | |
|[Assign tokenIssuancePolicy](../api/application-post-tokenissuancepolicies.md)| [tokenIssuancePolicy](tokenissuancepolicy.md) collection| Assign a tokenIssuancePolicy to this object.|
|[List tokenIssuancePolicies](../api/application-list-tokenissuancepolicies.md)| [tokenIssuancePolicy](tokenissuancepolicy.md) collection| Get all tokenIssuancePolicies assigned to this object.|
|[Remove tokenIssuancePolicy](../api/application-delete-tokenissuancepolicies.md)| [tokenIssuancePolicy](tokenissuancepolicy.md) collection| Remove a tokenIssuancePolicy from this object.|
|[Assign tokenLifetimePolicy](../api/application-post-tokenlifetimepolicies.md)| [tokenLifetimePolicy](tokenlifetimepolicy.md) collection| Assign a tokenLifetimePolicy to this object.|
|[List tokenLifetimePolicies](../api/application-list-tokenlifetimepolicies.md)| [tokenLifetimePolicy](tokenlifetimepolicy.md) collection| Get all tokenLifetimePolicies assigned to this object.|
|[Remove tokenLifetimePolicy](../api/application-delete-tokenlifetimepolicies.md)| [tokenLifetimePolicy](tokenlifetimepolicy.md) collection| Remove a tokenLifetimePolicy from this object.|
|**Verified publisher**| | |
|[Set verified publisher](../api/application-setverifiedpublisher.md)| None | Set the verified publisher of an application.|
|[Unset verified publisher](../api/application-unsetverifiedpublisher.md)| None | Unset the verified publisher of an application.|

## Properties

| Property | Type | Description |
|:---------------|:--------|:----------|
| addIns | [addIn](addin.md) collection | Defines custom behavior that a consuming service can use to call an app in specific contexts. For example, applications that can render file streams [may set the addIns property](/onedrive/developer/file-handlers/?view=odsp-graph-online) for its "FileHandler" functionality. This will let services like Office 365 call the application in the context of a document the user is working on. |
| api | [apiApplication](apiapplication.md) | Specifies settings for an application that implements a web API. |
| appId | String | The unique identifier for the application that is assigned by Azure AD. Not nullable. Read-only. |
| appRoles | [appRole](approle.md) collection | The collection of roles assigned to the application. With [app role assignments](approleassignment.md), these roles can be assigned to users, groups, or service principals associated with other applications. Not nullable. |
| createdDateTime | DateTimeOffset | The date and time the application was registered. Read-only. |
| deletedDateTime | DateTimeOffset | The date and time the application was deleted. Read-only. |
| displayName | String | The display name for the application. |
| groupMembershipClaims | String | Configures the `groups` claim issued in a user or OAuth 2.0 access token that the application expects. To set this attribute, use one of the following string values:<ul><li>`None`</li><li>`SecurityGroup`: For security groups and Azure AD roles</li><li>`All`: This gets all of the security groups, distribution groups, and Azure AD directory roles that the signed-in user is a member of.</li></ul> |
| id | String | The unique identifier for the application. Inherited from [directoryObject](directoryobject.md). Key. Not nullable. Read-only. |
| identifierUris | String collection | The URIs that identify the application within its Azure AD tenant, or within a verified custom domain if the application is multi-tenant. For more information, see [Application Objects and Service Principal Objects](/azure/active-directory/develop/app-objects-and-service-principals). The `any` operator is required for filter expressions on multi-valued properties. Not nullable. |
| info | [informationalUrl](informationalurl.md) | Basic profile information of the application, such as it's marketing, support, terms of service, and privacy statement URLs. The terms of service and privacy statement are surfaced to users through the user consent experience. For more information, see [How to: Add Terms of service and privacy statement for registered Azure AD apps](/azure/active-directory/develop/howto-add-terms-of-service-privacy-statement). |
| isFallbackPublicClient | Boolean | Specifies the fallback application type as public client, such as an installed application running on a mobile device. The default value is `false` which means the fallback application type is confidential client such as a web app. There are certain scenarios where Azure AD cannot determine the client application type. For example, the [ROPC](https://tools.ietf.org/html/rfc6749#section-4.3) flow where the application is configured without specifying a redirect URI. In those cases Azure AD interprets the application type based on the value of this property.|
| keyCredentials | [keyCredential](keycredential.md) collection | The collection of key credentials associated with the application. Not nullable. |
| logo | Stream | The main logo for the application. Not nullable. |
| oauth2RequiredPostResponse | Boolean | Specifies whether, as part of OAuth 2.0 token requests, Azure AD allows POST requests, as opposed to GET requests. The default is `false`, which specifies that only GET requests are allowed. |
| onPremisesPublishing |[onPremisesPublishing](onpremisespublishing.md)| Represents the set of properties required for [configuring Application Proxy](/graph/application-proxy-configure-api) for this application. Configuring these properties allows you to publish your on-premises application for secure remote access. |
| optionalClaims | [optionalClaims](optionalclaims.md) | Application developers can configure optional claims in their Azure AD applications to specify the claims that are sent to their application by the Microsoft security token service. For more information, see [How to: Provide optional claims to your app](/azure/active-directory/develop/active-directory-optional-claims).|
| parentalControlSettings | [parentalControlSettings](parentalcontrolsettings.md) |Specifies parental control settings for an application. |
| passwordCredentials | [passwordCredential](passwordcredential.md) collection|The collection of password credentials associated with the application. Not nullable.|
| publicClient | [publicClientApplication](publicclientapplication.md) | Specifies settings for installed clients such as desktop or mobile devices. |
| publisherDomain | String | The verified publisher domain for the application. Read-only.|
| requiredResourceAccess |[requiredResourceAccess](requiredresourceaccess.md) collection| Specifies the resources that the application needs to access. This property also specifies the set of OAuth permission scopes and application roles that it needs for each of those resources. This configuration of access to the required resources drives the consent experience. Not nullable.|
| signInAudience | String | Specifies the Microsoft accounts that are supported for the current application. Supported values are:<ul><li>`AzureADMyOrg`: Users with a Microsoft work or school account in my organization’s Azure AD tenant (single-tenant).</li><li>`AzureADMultipleOrgs`: Users with a Microsoft work or school account in any organization’s Azure AD tenant (multi-tenant).</li><li>`AzureADandPersonalMicrosoftAccount`: Users with a personal Microsoft account, or a work or school account in any organization’s Azure AD tenant.</li><li>`PersonalMicrosoftAccount`: Users with a personal Microsoft account only.</li></ul> |
| spa                     | [spaApplication](../resources/spaapplication.md)                            | Specifies settings for a single-page application, including sign out URLs and redirect URIs for authorization codes and access tokens. |
| tags |String collection| Custom strings that can be used to categorize and identify the application. Not nullable.|
| tokenEncryptionKeyId |String|Specifies the keyId of a public key from the keyCredentials collection. When configured, Azure AD encrypts all the tokens it emits by using the key this property points to. The application code that receives the encrypted token must use the matching private key to decrypt the token before it can be used for the signed-in user.|
| verifiedPublisher          | [verifiedPublisher](verifiedPublisher.md)                            | Specifies the verified publisher of the application.|
| web |[webApplication](webapplication.md)| Specifies settings for a web application. |

## Relationships

| Relationship | Type | Description |
|:---------------|:--------|:----------|
|calls           |[call](call.md) collection                  |Read-only. Nullable.|
|connectorGroup|[connectorGroup](connectorgroup.md)| The connectorGroup the application is using with Azure AD Application Proxy. Nullable.|
|createdOnBehalfOf|[directoryObject](directoryobject.md)| Read-only.|
|extensionProperties|[extensionProperty](extensionproperty.md) collection| Read-only. Nullable.|
|onlineMeetings  |[onlineMeeting](onlinemeeting.md) collection|Read-only. Nullable.|
|owners|[directoryObject](directoryobject.md) collection|Directory objects that are owners of the application. Read-only. Nullable.|
|tokenLifetimePolicies|[tokenLifetimePolicy](tokenLifetimePolicy.md) collection|The tokenLifetimePolicies assigned to this application.|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty":"id",
  "optionalProperties": [
    "createdOnBehalfOf",
    "owners"
  ],
  "@odata.type": "microsoft.graph.application"
}-->

```json
{
  "addIns": [{"@odata.type": "microsoft.graph.addIn"}],
  "api": {"@odata.type": "microsoft.graph.apiApplication"},
  "appId": "String",
  "appRoles": [{"@odata.type": "microsoft.graph.appRole"}],
  "createdDateTime": "String (timestamp)",
  "deletedDateTime": "String (timestamp)",
  "displayName": "String",
  "groupMembershipClaims": "String",
  "id": "String (identifier)",
  "identifierUris": ["String"],
  "info": {"@odata.type": "microsoft.graph.informationalUrl"},
  "isFallbackPublicClient": false,
  "keyCredentials": [{"@odata.type": "microsoft.graph.keyCredential"}],
  "logo": "Stream",
  "oauth2RequiredPostResponse": false,
  "optionalClaims": {"@odata.type": "microsoft.graph.optionalClaims"},
  "parentalControlSettings": {"@odata.type": "microsoft.graph.parentalControlSettings"},
  "passwordCredentials": [{"@odata.type": "microsoft.graph.passwordCredential"}],
  "publicClient": {"@odata.type": "microsoft.graph.publicClientApplication"},
  "publisherDomain": "String",
  "requiredResourceAccess": [{"@odata.type": "microsoft.graph.requiredResourceAccess"}],
  "signInAudience": "String",
  "tags": ["String"],
  "tokenEncryptionKeyId": "String",
  "verifiedPublisher": {"@odata.type": "microsoft.graph.verifiedPublisher"},
  "web": {"@odata.type": "microsoft.graph.webApplication"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "application resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

