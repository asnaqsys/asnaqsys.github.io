---
title: "DSParameter class             | QSYS API Reference Guide"
description: "Describes the datastructure parameters sent into an IBMi program call. "
last_modified_at: 2024-08-09T17:25:29Z
---

Describes the datastructure parameters sent into an IBMi program call.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Parameter](/reference/runtime/qsys-runtime/parameter.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DSParameter](#dsparameterstring-datadirection-idscallparm)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html)) | Create a DSParm object to represent an IBMi datastructure parameter.
| [DSParameter](#dsparameterstring-datadirection-idscallparm)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm\[\]](/reference/runtime/qsys-runtime/ids-call-parm.html)) | /// Create a DSParm object to represent an IBMi datastructure array parameter.

### DSParameter([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html))

Create a DSParm object to represent an IBMi datastructure parameter.

```cs
DSParameter(String, DataDirection, IDSCallParm)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | The DataDirection of the parameter.
| [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html) | dsCallParm | The IDSFlds object containing full descriptions of each ds field.

### DSParameter([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm\[\]](/reference/runtime/qsys-runtime/ids-call-parm.html))

/// Create a DSParm object to represent an IBMi datastructure array parameter.

```cs
DSParameter(String, DataDirection, IDSCallParm[])
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | The DataDirection of the parameter.
| [IDSCallParm\[\]](/reference/runtime/qsys-runtime/ids-call-parm.html) | dsCallParmArray | The IDSFlds object array containing full descriptions of each ds field.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html) | DSCallParm | The IDSFlds object containing full descriptions of each ds field. |
| [IDSCallParm\[\]](/reference/runtime/qsys-runtime/ids-call-parm.html) | DSCallParmArray | The IDSFlds object array containing full descriptions of each ds field. |
