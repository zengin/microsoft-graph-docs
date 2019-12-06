---
title: "API Documentation"
description: Update the existing doc 
localization_priority: Normal
author: "ROhini-MSFT"
ms.prod: "outlook"
doc_type: apiPageType
---

# Update Calendar

Update the properties of a [Calendar](../resources/calendar.md)object. The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md)

## Permissions

| Calendar | Delegated (work or school account) |  Delegated (personal Microsoft account) | Application |
|:-----|:-----|:-----|:-----|
| user calendar | Calendars.ReadWrite | Calendars.ReadWrite | Calendars.ReadWrite |
| group calendar | Group.ReadWrite.All | Not supported. | Not supported. |

## HTTP request

A user's or group's default [calendar](../resources/calendar.md).
```http
PATCH /me/calendar
PATCH /users/{id | userPrincipalName}/calendar
PATCH /groups/{id}/calendar
```
A users's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md)

### Request Headers
| Header      | Value |
|:------|:-------|
|Authorization | Bearer {token}. Required. |
|Content-Type |application/json. Required.| 


*italic*

**Bold**

_italic_

__underscores__

You _**can**_ combine them

~~Scratch this~~

1. First ordered list item
2. Second item
   * SubItem1
   * SubItem2
        1. Item1
        1. Item2
        1. Item3

http://github.com

[Github](http://github.com)

As he said:
> We are living the future so 


> the present 
> is our past. 



![Github Logo](../images/../../../concepts/images/OneNoteLogoIcon.png)

I think you should use an `address element` instead


- [ ]  Rohini
- [ ] Shalini
- [x] Vijay

```
function fancyAlert(arg){
        if(arg){
        $.facebox({div:'#foo'})
    }
}
```



# Emoji

:smile:


