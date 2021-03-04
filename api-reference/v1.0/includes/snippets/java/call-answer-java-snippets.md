---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

String callbackUri = "callbackUri-value";

AppHostedMediaConfig mediaConfig = new AppHostedMediaConfig();
mediaConfig.blob = "<Media Session Configuration Blob>";

LinkedList<Modality> acceptedModalitiesList = new LinkedList<Modality>();
acceptedModalitiesList.add(Modality.AUDIO);

graphClient.communications().calls("{id}")
	.answer(callbackUri,mediaConfig,acceptedModalitiesList)
	.buildRequest()
	.post();

```