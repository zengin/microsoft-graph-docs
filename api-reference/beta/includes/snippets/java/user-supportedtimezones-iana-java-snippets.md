---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IOutlookUserSupportedTimeZonesCollectionPage supportedTimeZones = graphClient.me().outlook()
	.supportedTimeZones(microsoft.graph.timeZoneStandard'Iana')
	.buildRequest()
	.get();

```