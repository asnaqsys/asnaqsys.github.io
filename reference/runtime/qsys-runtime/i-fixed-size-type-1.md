---
title: "IFixedSizeType<T> interface   | QSYS API Reference Guide"
description: "Declares the basic functionality of a fixed-size generic type. "
last_modified_at: 2024-08-09T17:25:29Z
---

Declares the basic functionality of a fixed-size generic type.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** [IFixedSizeType](/reference/runtime/qsys-runtime/i-fixed-size-type.html), [IComparable](https://learn.microsoft.com/en-us/dotnet/api/system.icomparable-1?view=net-8.0)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | Value | Returns the value of type T. |

## Methods

| Signature | Description |
| --- | --- |
| [Convert](#ifixedsizetype-t-convertt-value)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Convert the value to FixedSize of a particular type.

### IFixedSizeType\<T\> Convert([T value](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Convert the value to FixedSize of a particular type.

```cs
IFixedSizeType<T> Convert(T value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | value | Input value.

#### Returns

| Type | Description
| --- | ---
| [IFixedSizeType`1](/reference/runtime/qsys-runtime/i-fixed-size-type-1.html) | The new FixedSize of type, converted value.
