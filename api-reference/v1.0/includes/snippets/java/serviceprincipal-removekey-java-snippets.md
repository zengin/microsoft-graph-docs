---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

UUID keyId = UUID.fromString("f0b0b335-1d71-4883-8f98-567911bfdca6");

String proof = "eyJ0eXAiOiJ...";

graphClient.servicePrincipals("{id}")
	.removeKey(keyId,proof)
	.buildRequest()
	.post();

```