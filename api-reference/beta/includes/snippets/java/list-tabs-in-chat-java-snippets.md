---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

ITeamsTabCollectionPage tabs = graphClient.chats("19:d65713bc498c4a428c71ef9353e6ce20@thread.v2").tabs()
	.buildRequest()
	.expand("teamsApp")
	.get();

```