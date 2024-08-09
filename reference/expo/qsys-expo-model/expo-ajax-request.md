---
title: "ExpoAjaxRequest class         | QSYS API Reference Guide"
description: "Defines the ExpoAjaxRequest class (used for JSON serialization) "
last_modified_at: 2024-08-09T16:18:58Z
---

Defines the ExpoAjaxRequest class (used for JSON serialization)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | action | Gets or sets the action description that defines the interpretation of the rest of properties |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | dupFields | If action == "get5250", gets or sets the collection of user input dup fields |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | encodedRequest | If action == "get5250", gets or sets the encoded user input data |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | from | If action == "getRecords", gets or sets the upper rrn range of records requested |
| [IconShapeRequest\[\]](/reference/expo/qsys-expo-model/icon-shape-request.html) | iconForElement | If action == "getIconCollection", gets or sets the collection of requested icon SVG shapes  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | recordName | If action == "getRecords", gets or sets the name of the record format requested  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | requestorAidKey | Gets or sets the AID key (i.e. PgDn, PgDn) that triggered the AJAX request |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | telnetFlags | If action == "get5250", gets or sets the input telnet flags |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | to | If action == "getRecords", gets or sets the lower rrn range of records requested |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | wantDropped | If action == "getRecords", gets or sets a boolean value indicating to drop fields while populating record |
