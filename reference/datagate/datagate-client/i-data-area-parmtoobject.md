---
title: "IDataArea interface.ParmToObject Method"
description: "Converts a ProgParm parameter to an object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Converts a ProgParm parameter to an object.

## Overloads

| Signature | Description |
| --- | --- |
| [ParmToObject](#object-parmtoobject-type-returntype-string-parametername)(object ParmToObject(Type ReturnType, string ParameterName)) | Converts a ProgParm parameter to an object. |
| [ParmToObject](#object-parmtoobject-progparm-parameter-type-returntype)(object ParmToObject(ProgParm Parameter, Type ReturnType)) | Converts a ProgParm parameter to an object. |
| [ParmToObject](#object-parmtoobject-progparm-parameter-type-returntype-int-element)(object ParmToObject(ProgParm Parameter, Type ReturnType, int Element)) | Converts a ProgParm parameter to an object. |
| [ParmToObject](#object-parmtoobject-type-returntype-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)(object ParmToObject(Type ReturnType, string ParameterName, [Int32\[\] ElementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))) | Converts a ProgParm parameter to an object. |

<a id="object-parmtoobject-type-returntype-string-parametername"></a>
## object ParmToObject(Type ReturnType, string ParameterName)

Converts a ProgParm parameter to an object.

```cs
object ParmToObject(Type ReturnType, string ParameterName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParameterName | The name of the ProgParm parameter.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The converted object.

<a id="object-parmtoobject-progparm-parameter-type-returntype"></a>
## object ParmToObject(ProgParm Parameter, Type ReturnType)

Converts a ProgParm parameter to an object.

```cs
object ParmToObject(ProgParm Parameter, Type ReturnType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Parameter | The ProgParm parameter to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert to.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The converted object.

<a id="object-parmtoobject-progparm-parameter-type-returntype-int-element"></a>
## object ParmToObject(ProgParm Parameter, Type ReturnType, int Element)

Converts a ProgParm parameter to an object.

```cs
object ParmToObject(ProgParm Parameter, Type ReturnType, int Element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Parameter | The ProgParm parameter to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert to.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Element | The element index in the ProgParm parameter.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The converted object.

<a id="object-parmtoobject-type-returntype-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32"></a>
## object ParmToObject(Type ReturnType, string ParameterName, [Int32\[\] ElementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts a ProgParm parameter to an object.

```cs
object ParmToObject(Type ReturnType, string ParameterName, Int32[] ElementIndices)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParameterName | The name of the ProgParm parameter.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ElementIndices | The element indices in the ProgParm parameter.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The converted object.

## See Also
- [IDataArea interface class](i-data-area.html)
