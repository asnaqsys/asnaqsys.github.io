---
title: "QSysRoute class               | QSYS API Reference Guide"
description: "Defines Route values for redirecting pages when switching display files "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines Route values for redirecting pages when switching display files

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [QSysRoute](#qsysroutestring-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes the QSysRoute class

### QSysRoute([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes the QSysRoute class

```cs
QSysRoute(String, Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | area | The name of the area where the page is found. Set to null for pages living outside an area.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | jobHandle | The jobHandle associated with the job requesting the redirect.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | area | Gets and sets the Page's Area. |
| [Nullable\<Int32\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | JobHandle | Gets and sets the JobHandle associated with this route which will be used as a route's QueryString value. |
