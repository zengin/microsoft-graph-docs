---
title: "HTML Chat message in Microsoft Teams"
description: "HTML chat message verification in the Microsoft Teams."
author: "nkramer"
localization_priority: Priority
ms.prod: "microsoft-teams"
---

# HTML Chat message  in Microsoft Teams

Here's some HTML you may encounter in the Teams messages.


## HTML chat message

|Message Type|Content Property|Microsoft Teams Supported|
|--------|-----------|---------|
|Strikethrough|`<div><div><s>Strikethrough</s></div></div>`|Yes|
|Table|`<div><div>\n\n<table style=\"border-width:1px; border-style:solid; width:100%\">\n<colgroup><col style=\"width:50%\"><col style=\"width:50%\"></colgroup>\n<tbody>\n<tr style=\"border-width:1px; border-style:solid\">\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem 0.6rem\"><strong>Name</strong></td>\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem0.6rem\"><strong>Description</strong></td>\n</tr>\n<tr style=\"border-width:1px; border-style:solid\">\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem 0.6rem\">&nbsp;</td>\n<td style=\"border-width:1px; border-style:solid; padding:0.3rem0.6rem\">&nbsp;</td>\n</tr>\n</tbody>\n</table>\n\n</div>\n</div>`|Yes|
|Sticker|`<div><div><img alt=\"Meme image, Hey !!\" src=\"https://graph.microsoft.com/beta/teams/32e3b156-66b2-4135-9aeb-73295a35a55b/channels/19:f253e46c035b42308e9a4a22a87037af@thread.skype/messages/1591170271279/hostedContents/aWQ9eF8wLWV1cy1kNi1mMzk4YmU3ZmE5ZmUxODc0NWUxYzcwMGU1ZjM2ZWFjZSx0eXBlPTEsdXJsPWh0dHBzOi8vdXMtYXBpLmFzbS5za3lwZS5jb20vdjEvb2JqZWN0cy8wLWV1cy1kNi1mMzk4YmU3ZmE5ZmUxODc0NWUxYzcwMGU1ZjM2ZWFjZS92aWV3cy9pbWdv/$value\" style=\"width:250px; height:166px\"></div>\n</div>`|Yes|
|Hyphen|`High-tech 1990-2002`|Yes|
|Bold, Italics, Underline, :, ;, [], {}, ALLCAPS, allsmalls, < (), !, /, \, ?, blue|`<div><div><strong>Bold</strong> <em>Italics</em> <u>Underline</u>&nbsp;ALLCAPS allsmalls < ; : @ --&gt; {} [] () '' | \\ / ? <span style=\"color:#6888c9\">Blue</span></div>\n</div>`|\ and > not supported|
|Heading|`<div>\n<h1>Heading 1</h1>\n\n\n\n<h2>Heading 2</h2>\n\n\n\n<h3>Heading 3</h3>\n\n</div>`|Yes|
|Ordered and Unordered lists|`<div>\n<ul>\n\n\t\n<li>First point\n\t</li><li>Second point\n\t</li><li>Third&nbsp;point\n</li></ul>\n\n\n\n<ol>\n\n\t\n<li>First step\n\t</li><li>Second step\n\t</li><li>Third step\n</li></ol>\n\n</div>`|Yes|
|Quote|`<div>\n<blockquote>\n<div>Honesty is the best policy!</div>\n</blockquote>\n\n</div>`|Yes|
|Insert a link|`<div><div><a href=\"https://github.com/microsoftgraph/microsoft-graph-docs/blob/master/concepts/changelog.md\" rel=\"noreferrer noopener\" target=\"_blank\" title=\"https://github.com/microsoftgraph/microsoft-graph-docs/blob/master/concepts/changelog.md\">Changelog</a></div>\n</div>`|Yes|
|IMPORTANT!|`Let's do it!`|Yes|
|Asterisk|`Channel*`|Yes|
|Messaging extension - Event ride|`<attachment id=\"74f3776dc19f4025a1aaa677eb4167f6\"></attachment>`|Yes|
|Attach checklist|`<attachment id=\"5875ae97469a4b85b65f04ac1da4f040\"></attachment>`|Yes|
|Send a praise card|`<div><div><attachment id=\"deea5ef098394989a6db5ec55f77ee1a\"></attachment></div></div> <div><at id=\"0\">Meenakshi Yeswanth (Ushta Te Consultancy Services) </at> </div>`|Yes|
|Attach a picture|`UY<attachment id=\"dd5685ef-e4b4-4a69-93e1-10c97ce9e2a4\"></attachment>`|Yes|
|Highlight|`<div><div><span style=\"background-color:#6888c9\">Highlighting</span></div></div>`|Yes|
|Announcement|`error`|No|
|Code Snippet|`error`|No|

