---
title: "DdsMenuOptionTagHelper class  | QSYS API Reference Guide"
description: "Defines a Context Menu Option. DdsMenuOptions on a DdsContextMenu container define actions identified by AidKeys. "
last_modified_at: 2024-08-09T17:26:17Z
---

Defines a Context Menu Option. DdsMenuOptions on a DdsContextMenu container define actions identified by AidKeys.

**Namespace:** ASNA.QSys.Expo.Tags
**Assembly:** ASNA.QSys.Expo.Tags.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TagHelper](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.razor.taghelpers.taghelper?view=aspnetcore-8.0)
<br>
<br>

## Remarks

Defines a Context Menu Option

Menu Options define *actions* a user may execute. The *action* is labeled with a descriptive `Text`.

An Action may:

1. *Change* the value of an existing field on the page. Optionally setting the *row,col* values for the virtual legacy application cursor-location, to allow the program that executed this DisplayPage to test the *current* cursor-location to conditionally execute logic code.
2. *Push* an [AidKey](/reference/expo/qsys-expo-model/aid-key.html) to submit the page.
3. Combination of *(1)* and *(2)* above to *Change* a field and then *Push* an [AidKey](/reference/expo/qsys-expo-model/aid-key.html) to submit the page.

>To define a menu Option separator, enter `--` (two dashes) as the `Text` property.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | AidKey | Attention or Function key to be posted when Button is clicked (as if the user had pressed than keyboard key). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FieldValue | When used along with FocusField, gets or sets the value to be copied to the field prior to submitting the page. This allows compatibility with logic expecting to detect a particular value of a field at a particular cursor position.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FocusField | Gets or sets the name of the field where the cursor will be set prior to submitting the page. This allows compatibility with logic expecting to detect cursor position on a particular field. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets the Menu Option Display Text. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | VirtualRowCol | Gets or sets the value of the legacy row, col position that the Button will report as being the one where the cursor was 'positioned' when the button was clicked. |
