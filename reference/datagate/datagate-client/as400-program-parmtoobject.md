---
title: "As400Program.ParmToObject Method"
description: "Converts the specified parameter to an object of the specified type."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Converts the specified parameter to an object of the specified type.

## Overloads

| Signature | Description |
| --- | --- |
| [ParmToObject](#object-parmtoobject-progparm-parameter-type-returntype-int-element)(object ParmToObject(ProgParm parameter, Type returnType, int element)) | Converts the specified parameter to an object of the specified type. |
| [ParmToObject](#object-parmtoobject-progparm-parameter-type-returntype)(object ParmToObject(ProgParm Parameter, Type ReturnType)) | Converts the specified parameter to an object of the specified type. |
| [ParmToObject](#object-parmtoobject-type-returntype-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)(object ParmToObject(Type returnType, string parameterName, [Int32\[\] elementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))) | Converts the specified parameter to an object of the specified type. |
| [ParmToObject](#object-parmtoobject-type-returntype-string-parametername)(object ParmToObject(Type ReturnType, string ParameterName)) | Converts the specified parameter to an object of the specified type. |

<a id="object-parmtoobject-progparm-parameter-type-returntype-int-element"></a>
## object ParmToObject(ProgParm parameter, Type returnType, int element)

Converts the specified parameter to an object of the specified type.

#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then creates a new SubParmName with the specified element index and calls the ToObject method of the parameter with the SubParmName.

```cs
object ParmToObject(ProgParm parameter, Type returnType, int element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | returnType | The type to convert the parameter to.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | element | The index of the element to convert, if the parameter is an array.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

<a id="object-parmtoobject-progparm-parameter-type-returntype"></a>
## object ParmToObject(ProgParm Parameter, Type ReturnType)

Converts the specified parameter to an object of the specified type.

#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then creates a new SubParmName with the specified element index and calls the ToObject method of the parameter with the SubParmName.

```cs
object ParmToObject(ProgParm Parameter, Type ReturnType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Parameter | The parameter to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert the parameter to.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

<a id="object-parmtoobject-type-returntype-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32"></a>
## object ParmToObject(Type returnType, string parameterName, [Int32\[\] elementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts the specified parameter to an object of the specified type.

#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It checks if the provided parameter name is null, and if so, throws an ArgumentNullException. It then creates a new SubParmName with the specified parameter name and element indices, and gets the parameter with the name from the SubParmName. If no such parameter exists, it throws an ArgumentException. It then calls the ToObject method of the parameter with the SubParmName and the type.

```cs
object ParmToObject(Type returnType, string parameterName, Int32[] elementIndices)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | returnType | The type to convert the parameter to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameterName | The name of the parameter to convert.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | elementIndices | The indices of the elements to convert, if the parameter is an array.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

<a id="object-parmtoobject-type-returntype-string-parametername"></a>
## object ParmToObject(Type ReturnType, string ParameterName)

Converts the specified parameter to an object of the specified type.

#### Remarks
This method converts the specified parameter to an object of the specified type in the ASNA DataGate client. It calls the ParmToObject method with the type, parameter name, and an empty array of element indices.

```cs
object ParmToObject(Type ReturnType, string ParameterName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | ReturnType | The type to convert the parameter to.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParameterName | The name of the parameter to convert.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An object of the specified type, representing the specified parameter.

## See Also
- [As400Program class](as400-program.html)
