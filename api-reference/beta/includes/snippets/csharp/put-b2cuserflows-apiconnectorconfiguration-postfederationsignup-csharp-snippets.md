---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Identity.B2cUserFlows["B2C_1_testuserflow"].PostFederationSignup.Reference
	.Request()
	.PutAsync("{id}");

```