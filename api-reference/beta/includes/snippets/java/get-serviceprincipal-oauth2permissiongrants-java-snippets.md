---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOAuth2PermissionGrantCollectionWithReferencesPage oauth2PermissionGrants = graphClient.servicePrincipals("{id}").oauth2PermissionGrants()
	.buildRequest()
	.get();

```