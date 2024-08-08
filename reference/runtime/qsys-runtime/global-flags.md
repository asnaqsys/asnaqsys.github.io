---
title: "GlobalFlags class             | QSYS API Reference Guide"
description: "Holds the application flags that correspond to RPG&#39;s %ERROR, not %FOUND, %EOF, and %EQUAL. These flags are local per thread. "
last_modified_at: 2024-08-08T21:41:46Z
---

Holds the application flags that correspond to RPG's %ERROR, not %FOUND, %EOF, and %EQUAL. These flags are local per thread.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | EOF | Thread local EOF flag (RPG's %EOF) |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Equal | Thread local equal flag (RPG's %EQUAL) |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Error | Thread local error flag (RPG's %ERROR) |
| [GlobalFlagProperty](/reference/runtime/qsys-runtime/global-flag-property.html) | GlobalFlag | Property to access global flags using case-insensitive names. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | NotFound | Thread local not found flag (RPG's *not %FOUND) |
