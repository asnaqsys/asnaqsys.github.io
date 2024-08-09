---
title: "DdsFunctionKeysTagHelper class"
description: "Defines Application Aid Key banner "
last_modified_at: 2024-08-09T17:26:17Z
---

Defines Application Aid Key banner

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

All Display Pages have a `bar` that displays buttons to activate [AidKey](/reference/expo/qsys-expo-model/aid-key.html) codes to submit the Page to the server.

The `DdsFunctionKeys` defines where this `bar` will be rendered, effectively defining the remaining area on the Page where the rest of the `DdsXXX` will render.

Typically, the `DdsFunctionKeys` is defined as the first element inside `DdsFile`

```html
<form id="MonarchForm" method="post">
    <DdsFile DisplayPageModel="Model">

        <DdsFunctionKeys Location="HorizontalBottom" />
        .
        .
        .
    </DdsFile>
<form>
```

>If you prefer not to display the `DdsFunctionKeys` bar (i.e. your Application has other navigation menus), include the `DdsFunctionKeys` instance on your Display Page with the `Location` property set to [Hidden](/reference/expo/qsys-expo-tags/active-key-bar-location.html). 


## Properties

| Type | Name | Description
| --- | --- | --- 
| [ActiveKeyBarLocation](/reference/expo/qsys-expo-tags/active-key-bar-location.html) | Location | Gets or sets the ActiveKeyBarLocation location where keys will be rendered. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ShowKeyMnemonics | Show the Function Key Mnemonics along with the Key Names, for example: (F3 - Exit). |
