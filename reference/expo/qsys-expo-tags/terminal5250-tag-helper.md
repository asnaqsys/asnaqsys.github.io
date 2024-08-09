---
title: "Terminal5250TagHelper class   | QSYS API Reference Guide"
description: "Defines the element where the 5250 Terminal will be rendered "
last_modified_at: 2024-08-09T16:19:09Z
---

Defines the element where the 5250 Terminal will be rendered

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

The `Terminal5250` Tag Helper renders a [5250 Terminal](https://en.wikipedia.org/wiki/IBM_5250) Emulator.

Legacy Applications migrated to [ASNA Monarch Base](/concepts/concepts-overview.html) runtime environment, may contain Display Pages that can directly display screens where the Application Logic still runs as [IBM i Program Objects](https://www.ibm.com/docs/en/i/7.1?topic=concepts-i-objects#).

There are two reasons why an Application may use this technique:

1. The Application Migration is a *continuos process*, where the **most used interactive programs** are Migrated first. Hybrid environments (application logic code split: some migrated to .Net other remaining on IBM i systems). Sections of the Application are put into production, while the rest is being migrated.
2. The Application Migration is complete but the IBM i system will not be retired. Some **rarely used programs** are kept as legacy - indefinitely - on IBM i systems.

   Possible scenarios:

      a) The source code may be missing.

      b) `IBM i Program objects` too expensive to remediate (programs written on different languages and development resources no longer available).

      c) `IBM i Program objects` that have not changed for a long time and are not expected to change.

      d) `IBM i Program objects` Program restricted to system operators - who do not need a new User Interface -.



[ASNA Browser Terminal](https://asna.com/us/products/bterm) is a product that exposes a Display Page that uses an instance of `Terminal5250` Tag Helper, and provides very simple end-user connectivity to the IBM i.

The following markup shows how [ASNA Browser Terminal](https://asna.com/us/products/bterm) defines the Display Page:

```html
@page
@addTagHelper *, ASNA.QSys.Expo.Tags
@model ASNA.Pages.TerminalPage.Terminal
@{
    ViewData["Title"] = "ASNA BTerm";
}

<html>
<body>
    <div id="close-icon" onclick="asnaExpo.terminal.executeMacro(['Exit', 'REDIRECT:/Monarch/Eoj'])" >
        <svg style="height: 100%" viewBox="0 0 1792 1792" xmlns="http://www.w3.org/2000/svg">
            <path fill="currentColor" d="M1490 1322q0 40-28 68l-136 136q-28 28-68 28t-68-28l-294-294-294 294q-28 28-68 28t-68-28l-136-136q-28-28-28-68t28-68l294-294-294-294q-28-28-28-68t28-68l136-136q28-28 68-28t68 28l294 294 294-294q28-28 68-28t68 28l136 136q28 28 28 68t-28 68l-294 294 294 294q28 28 28 68z" />
        </svg>
    </div>

    <form method="post">
        <Terminal5250 For=@Model />
    </form>
</body>
</html>
```

>In addition to the [form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form) element, where the `Terminal5250` will render, a *clickable* icon on the top is displayed to allow the User to **close** the Application (re-direct to **E**nd **O**f **J**ob Page).

The Model code is very simple:

```cs
using Microsoft.AspNetCore.Mvc;
using ASNA.QSys.Expo.Model;

namespace ASNA.Pages.TerminalPage
{
    public class Terminal : Terminal5250_PageModel
    {

    }
}
```

>The [Terminal5250_PageModel](/reference/expo/qsys-expo-model/terminal5250-page-model.html) implements the 5250 protocol to connect to the IBM i.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ModelExpression](https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.viewfeatures.modelexpression) | For | Gets or sets the Model reference to the Record class. Mostly to simplify markup syntax.  |
| [Terminal5250_PageModel](/reference/expo/qsys-expo-model/terminal5250-page-model.html) | The5250RecordModel | Gets the Terminal5250_PageModel Model reference |
