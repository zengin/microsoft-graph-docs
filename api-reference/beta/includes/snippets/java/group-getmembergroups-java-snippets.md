---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Boolean securityEnabledOnly = false;

graphClient.groups("{id}")
	.getMemberGroups(securityEnabledOnly)
	.buildRequest()
	.post();

```