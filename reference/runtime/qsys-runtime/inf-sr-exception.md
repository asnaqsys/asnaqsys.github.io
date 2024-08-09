---
title: "InfSrException class          | QSYS API Reference Guide"
description: "Exception that can be thrown from InfSr to return or report an error condition. "
last_modified_at: 2024-08-09T16:18:25Z
---

Exception that can be thrown from InfSr to return or report an error condition.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InfSrException](#infsrexceptioninfsrreturnpoint)([InfSrReturnPoint](/reference/runtime/qsys-runtime/inf-sr-return-point.html)) | Initializes an InfSrException object.
| [InfSrException](#infsrexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes an InfSrException object.

### InfSrException([InfSrReturnPoint](/reference/runtime/qsys-runtime/inf-sr-return-point.html))

Initializes an InfSrException object.

```cs
InfSrException(InfSrReturnPoint)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [InfSrReturnPoint](/reference/runtime/qsys-runtime/inf-sr-return-point.html) | returnPoint | The InfSrReturnPoint value describing from where the exception will be thrown.

### InfSrException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes an InfSrException object.

```cs
InfSrException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | returnPointSring | String value with the name of the return point from where the exception will be thrown.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [InfSrReturnPoint](/reference/runtime/qsys-runtime/inf-sr-return-point.html) | ReturnPoint | The InfSrReturnPoint value describing where this exception happened. |
