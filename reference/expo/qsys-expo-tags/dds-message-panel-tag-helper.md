---
title: "DdsMessagePanelTagHelper class"
description: "Provides a placeholder for Page messages. "
last_modified_at: 2024-08-09T16:19:09Z
---

Provides a placeholder for Page messages.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

IBM i Display files typically used an area on the Page to display messages. This is known as the [Message Subfile](https://www.ibm.com/docs/en/i/7.1?topic=type-example-message-subfile-using-dds)

The `DdsMessagePanel` Tag Helper defines the location in the Page for the  [Message Subfile](https://www.ibm.com/docs/en/i/7.1?topic=type-example-message-subfile-using-dds).

As Display Pages are submitted, input is validated according to errors produced during the Model Binding process. Any [Binding Model Errors](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.modelerrorcollection) are presented inside `DdsMessagePanel` as a list of text lines with [Line Breaks](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br) after each line.

There is no particular [CSS style](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class) associated with this element. It is assumed that a `class` will be *added later* during the *Modernization* process (i.e. styles such as scrolling, colors etc.)

>If [Binding Model Errors](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.modelbinding.modelerrorcollection) are going to be processed in a different way, omit this Tag Helper and the Application continues normally.

The typical placement of the `DdsMessagePanel` Tag Helper is as the last element on the [main](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main) as indicated below: 

```html
<form method="post">>
    <DdsFile DisplayPageModel="Model">

        <DdsFunctionKeys />

        <main role="main" >
            <DdsSubfileControl For="Record_1">...</DdsSubfileControl>
            <DdsRecord For="Record_2">...</DdsRecord>
            <DdsRecord For="Record_3">...</DdsRecord>
            <DdsRecord For="Record_n">...</DdsRecord>

            <DdsMessagePanel class="my-messages-style"/>
        </main>
    </DdsFile>
</form>
```
