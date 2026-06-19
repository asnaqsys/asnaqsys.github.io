---
title: "As400Program.ObjectToParm Method"
description: "Converts the specified object to a parameter of the specified type."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Converts the specified object to a parameter of the specified type.

## Overloads

| Signature | Description |
| --- | --- |
| [ObjectToParm](#void-objecttoparm-progparm-parameter-object-value-int-element)(void ObjectToParm(ProgParm parameter, object value, int element)) | Converts the specified object to a parameter of the specified type. |
| [ObjectToParm](#void-objecttoparm-progparm-parameter-object-value)(void ObjectToParm(ProgParm parameter, object value)) | Converts the specified object to a parameter. |
| [ObjectToParm](#void-objecttoparm-object-value-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)(void ObjectToParm(object value, string parameterName, [Int32\[\] elementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))) | Converts the specified object to a parameter of the specified name and element indices. |
| [ObjectToParm](#void-objecttoparm-object-value-string-parametername)(void ObjectToParm(object value, string parameterName)) | Converts the specified object to a parameter of the specified name. |

<a id="void-objecttoparm-progparm-parameter-object-value-int-element"></a>
## void ObjectToParm(ProgParm parameter, object value, int element)

Converts the specified object to a parameter of the specified type.

#### Remarks
This method converts the specified object to a parameter of the specified type in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then creates a new SubParmName with the specified element index and calls the FromObject method of the parameter with the SubParmName and the object.

```cs
void ObjectToParm(ProgParm parameter, object value, int element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to convert the object to.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | element | The index of the element to convert, if the parameter is an array.

<a id="void-objecttoparm-progparm-parameter-object-value"></a>
## void ObjectToParm(ProgParm parameter, object value)

Converts the specified object to a parameter.

#### Remarks
This method converts the specified object to a parameter in the ASNA DataGate client. It checks if the provided parameter is null or has no metadata, and if so, throws an exception. It also checks if the parameter is structured, and if so, throws an exception. It then calls the ObjectToParm method with the parameter, object, and an element index of 0.

```cs
void ObjectToParm(ProgParm parameter, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to convert the object to.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.

<a id="void-objecttoparm-object-value-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32"></a>
## void ObjectToParm(object value, string parameterName, [Int32\[\] elementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts the specified object to a parameter of the specified name and element indices.

#### Remarks
This method converts the specified object to a parameter of the specified name and element indices in the ASNA DataGate client. It checks if the provided parameter name is null, and if so, throws an ArgumentNullException. It then creates a new SubParmName with the specified parameter name and element indices, and gets the parameter with the name from the SubParmName. If no such parameter exists, it throws an ArgumentException. It then calls the FromObject method of the parameter with the SubParmName and the object.

```cs
void ObjectToParm(object value, string parameterName, Int32[] elementIndices)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameterName | The name of the parameter to convert the object to.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | elementIndices | The indices of the elements to convert, if the parameter is an array.

<a id="void-objecttoparm-object-value-string-parametername"></a>
## void ObjectToParm(object value, string parameterName)

Converts the specified object to a parameter of the specified name.

#### Remarks
This method converts the specified object to a parameter of the specified name in the ASNA DataGate client. It calls the ObjectToParm method with the object, parameter name, and an empty array of element indices.

```cs
void ObjectToParm(object value, string parameterName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | parameterName | The name of the parameter to convert the object to.

## See Also
- [As400Program class](as400-program.html)
