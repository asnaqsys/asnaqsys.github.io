---
title: "Call class                    | QSYS API Reference Guide"
description: "Provides functionality to handle calling a program residing in an IBMi server. "
last_modified_at: 2024-08-08T21:41:46Z
---

Provides functionality to handle calling a program residing in an IBMi server.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [AddDSParm](#void-adddsparmstring-name-datadirection-direction-idscallparm-dscallparm)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html)) | Adds a datastructure parameter to the program call.
| [AddDSParm](#void-adddsparmstring-name-datadirection-direction-idscallparm--dscallparmarray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm\[\]](/reference/runtime/qsys-runtime/ids-call-parm.html)) | Adds a datastructure array parameter to the program call.
| [AddParm](#void-addparmstring-name-fieldtype-type-datadirection-direction-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](/reference/datagate/datagate-common/field-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds a parameter to the program call with an initial value (use for input and input/output parameters).
| [AddParm](#void-addparmstring-name-fieldtype-type-datadirection-direction-object--valuearray)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](/reference/datagate/datagate-common/field-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds a parameter array to the program call with an initial value (use for input and input/output parameters).
| [AddParm](#void-addparmstring-name-fieldtype-type)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](/reference/datagate/datagate-common/field-type.html)) | Adds a parameter to the program call with no initial value (use only for output parameters).
| [AddParm](#void-addparmstring-name-fieldtype-type-int-arraylength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [FieldType](/reference/datagate/datagate-common/field-type.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Adds a parameter or parameter array to the program call with no initial value (use only for output parameters).
| [CallProgram](#void-callprogramstring-name-database-database)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html)) | Calls an IBMi Program with the parameters added to the call object.
| [GetParm](#object-getparmstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves the value of an output or update parameter based on its name.

### void AddDSParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DataDirection direction](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm dsCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html))

Adds a datastructure parameter to the program call.

```cs
void AddDSParm(string name, DataDirection direction, IDSCallParm dsCallParm)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | Specifies if the parameter is input, output, or input/output.
| [IDSCallParm](/reference/runtime/qsys-runtime/ids-call-parm.html) | dsCallParm | The IDSCallParm object representing the datastructure to add to the program call.

### void AddDSParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DataDirection direction](/reference/datagate/datagate-common/data-direction.html), [IDSCallParm\[\] dsCallParmArray](/reference/runtime/qsys-runtime/ids-call-parm.html))

Adds a datastructure array parameter to the program call.

```cs
void AddDSParm(string name, DataDirection direction, IDSCallParm[] dsCallParmArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | Specifies if the parameter is input, output, or input/output.
| [IDSCallParm\[\]](/reference/runtime/qsys-runtime/ids-call-parm.html) | dsCallParmArray | The IDSCallParm[] object representing the datastructure array to add to the program call.

### void AddParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [FieldType type](/reference/datagate/datagate-common/field-type.html), [DataDirection direction](/reference/datagate/datagate-common/data-direction.html), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Adds a parameter to the program call with an initial value (use for input and input/output parameters).

```cs
void AddParm(string name, FieldType type, DataDirection direction, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [FieldType](/reference/datagate/datagate-common/field-type.html) | type | The FieldType object that describes the parameter's type and size.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | Specifies if the parameter is input, output, or update.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | Initial value for the parameter to be sent to the program being called.

### void AddParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [FieldType type](/reference/datagate/datagate-common/field-type.html), [DataDirection direction](/reference/datagate/datagate-common/data-direction.html), [Object\[\] valueArray](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Adds a parameter array to the program call with an initial value (use for input and input/output parameters).

```cs
void AddParm(string name, FieldType type, DataDirection direction, Object[] valueArray)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [FieldType](/reference/datagate/datagate-common/field-type.html) | type | The FieldType object that describes the parameter's type and size.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | direction | Specifies if the parameter is input, output, or update.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | valueArray | Initial value for the parameter array to be sent to the program being called.

### void AddParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [FieldType type](/reference/datagate/datagate-common/field-type.html))

Adds a parameter to the program call with no initial value (use only for output parameters).

```cs
void AddParm(string name, FieldType type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [FieldType](/reference/datagate/datagate-common/field-type.html) | type | The FieldType object that describes the parameter's type and size.

### void AddParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [FieldType type](/reference/datagate/datagate-common/field-type.html), [int arrayLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Adds a parameter or parameter array to the program call with no initial value (use only for output parameters).

```cs
void AddParm(string name, FieldType type, int arrayLength)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.
| [FieldType](/reference/datagate/datagate-common/field-type.html) | type | The FieldType object that describes the parameter's type and size.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | arrayLength | The parameter's length if it is an array (pass in 0 if it is not an array).

### void CallProgram([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database database](/reference/runtime/qsys-runtime/database.html))

Calls an IBMi Program with the parameters added to the call object.

```cs
void CallProgram(string name, Database database)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the IBMi program to call.
| [Database](/reference/runtime/qsys-runtime/database.html) | database | The database to connect with in order to call the program.

### object GetParm([string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Retrieves the value of an output or update parameter based on its name.

```cs
object GetParm(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter to retrieve.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The value of the parameter requested.
