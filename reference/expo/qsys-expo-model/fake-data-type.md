---
title: "FakeDataType enum             | QSYS API Reference Guide"
description: "Specifies the type of fake data to use for the display pages. "
last_modified_at: 2024-08-08T21:42:10Z
---

Specifies the type of fake data to use for the display pages.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll
<br>
<br>

Expo provides a mechanism to test the Razor Pages views by utilizing fake data stored in text files in lieu of invoking the application programs. This enumeration is part of that mechanism.

See the [DisplayPagesOptions](/reference/expo/qsys-expo-model/display-pages-options.html) used with the extension method [ConfigureDisplayPagesOptions](/reference/expo/qsys-expo-model/display-options-service-collection-extensions.html)().

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| Input | Allows user to save display page data rendered on the browser as fake data. | 2 |
| None | No fake data is to be used. | 0 |
| Output | Use fake data when rendering the display pages. Logic project is not used at all. | 1 |
