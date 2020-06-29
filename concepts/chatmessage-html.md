---
title: "HTML Chat message"
description: "HTML chat message verification in the Microsoft Teams."
author: "nkramer"
localization_priority: Priority
ms.prod: "microsoft-teams"
---

# HTML Chat message  in Microsoft Teams

Here's some HTML you may encounter in the Teams messages.

|Construct|Example|
|--------|-----------|
|Strikethrough|`<s>Strikethrough</s>`|
|Table|`<table style=\"border-width:1px; border-style:solid; width:100%\">\n<colgroup><col style=\"width:50%\"><col style=\"width:50%\"></colgroup>\n<tbody>\n<tr style=\"border-width:1px; border-style:solid\">\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem 0.6rem\"><strong>Name</strong></td>\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem0.6rem\"><strong>Description</strong></td>\n</tr>\n<tr style=\"border-width:1px; border-style:solid\">\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem 0.6rem\">&nbsp;</td>\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem0.6rem\">&nbsp;</td>\n</tr>\n</tbody>\n</table>`|
|Sticker|`<img alt=\"Meme image, Hey !!\" src=\"https://graph.microsoft.com/beta/teams/32e3b156-66b2-4135-9aeb-73295a35a55b/channels/19:f253e46c035b42308e9a4a22a87037af@thread.skype/messages/1591170271279/hostedContents/aWQ9eF8wLWV1cy1kNi1mMzk4YmU3ZmE5ZmUxODc0NWUxYzcwMGU1ZjM2ZWFjZSx0eXBlPTEsdXJsPWh0dHBzOi8vdXMtYXBpLmFzbS5za3lwZS5jb20vdjEvb2JqZWN0cy8wLWV1cy1kNi1mMzk4YmU3ZmE5ZmUxODc0NWUxYzcwMGU1ZjM2ZWFjZS92aWV3cy9pbWdv/$value\" style=\"width:250px; height:166px\">`|
|Bold, Italics, Underline, :, ;, [], {}, ALLCAPS, allsmalls, < (), !, /, \, ?, blue|`<strong>Bold</strong> <em>Italics</em> <u>Underline</u>&nbsp;ALLCAPS allsmalls < ; : @ --&gt; {} [] () '' | \\ / ? <span style=\"color:#6888c9\">Blue</span>`|
|Heading|`<h1>Heading 1</h1>`|
|Ordered and Unordered lists|`<ul><li>First point</li></ul><ol><li>First step</li></ol>`|
|Quote|`<blockquote>\n<div>Honesty is the best policy!</div>\n</blockquote>`|
|Insert a link|`<a href=\"https://github.com/microsoftgraph/microsoft-graph-docs/blob/master/concepts/changelog.md\" rel=\"noreferrer noopener\" target=\"_blank\" title=\"https://github.com/microsoftgraph/microsoft-graph-docs/blob/master/concepts/changelog.md\">Changelog</a>`|
|Messaging extension - Event ride|`<attachment id=\"74f3776dc19f4025a1aaa677eb4167f6\"></attachment>`|
|Attach checklist|`<attachment id=\"5875ae97469a4b85b65f04ac1da4f040\"></attachment>`|
|Send a praise card|`<attachment id=\"deea5ef098394989a6db5ec55f77ee1a\"></attachment></div></div> <div><at id=\"0\">Meenakshi Yeswanth (Ushta Te Consultancy Services) </at>`|
|Attach a picture|`UY<attachment id=\"dd5685ef-e4b4-4a69-93e1-10c97ce9e2a4\"></attachment>`|
|Highlight|`<span style=\"background-color:#6888c9\">Highlighting</span>`|
