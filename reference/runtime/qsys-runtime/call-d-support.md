---
title: "CallDSupport class            | QSYS API Reference Guide"
description: "Provides methods to construct Omissible and Optional parameters for CALLD "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides methods to construct Omissible and Optional parameters for CALLD

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [NewEmptyNoPassOmit<T>()](#nopassomit-t-newemptynopassomit-t) | Creates a new NoPassOmit parameter without value.
| [NewEmptyOmissible<T>()](#omissible-t-newemptyomissible-t) | Creates a new Omissible parameter without value.
| [NewEmptyOptional<T>()](#optional-t-newemptyoptional-t) | Creates a new Optional parameter without value.
| [NewNoPassOmit\<T\>](#nopassomit-t-newnopassomit-t-t-value)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Creates a new NoPassOmit parameter.
| [NewOmissible\<T\>](#omissible-t-newomissible-t-t-value)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Creates a new Omissible parameter.
| [NewOptional\<T\>](#optional-t-newoptional-t-t-value)([T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0)) | Creates a new Optional parameter.

### NoPassOmit<T> NewEmptyNoPassOmit<T>()

Creates a new NoPassOmit parameter without value.

```cs
NoPassOmit<T> NewEmptyNoPassOmit<T>()
```

### Omissible<T> NewEmptyOmissible<T>()

Creates a new Omissible parameter without value.

```cs
Omissible<T> NewEmptyOmissible<T>()
```

### Optional<T> NewEmptyOptional<T>()

Creates a new Optional parameter without value.

```cs
Optional<T> NewEmptyOptional<T>()
```

### NoPassOmit\<T\> NewNoPassOmit\<T\>([T value](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Creates a new NoPassOmit parameter.

```cs
NoPassOmit<T> NewNoPassOmit<T>(T value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | value | The value to store in the NoPassOmit object.

#### Returns

| Type | Description
| --- | ---
| [NoPassOmit`1](/reference/runtime/qsys-runtime/no-pass-omit-1.html) | A NoPassOmit object with a value.

### Omissible\<T\> NewOmissible\<T\>([T value](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Creates a new Omissible parameter.

```cs
Omissible<T> NewOmissible<T>(T value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | value | The value to store in the Omissible object.

#### Returns

| Type | Description
| --- | ---
| [Omissible`1](/reference/runtime/qsys-runtime/omissible-1.html) | An Omissible object with a value.

### Optional\<T\> NewOptional\<T\>([T value](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0))

Creates a new Optional parameter.

```cs
Optional<T> NewOptional<T>(T value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [T](https://learn.microsoft.com/en-us/dotnet/api/system.type?view=net-8.0) | value | The value to store in the Optional object.

#### Returns

| Type | Description
| --- | ---
| [Optional`1](/reference/runtime/qsys-runtime/optional-1.html) | An Optional object with a value.
