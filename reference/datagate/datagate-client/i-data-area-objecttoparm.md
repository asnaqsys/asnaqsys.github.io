---
title: "IDataArea interface.ObjectToParm Method"
description: "Converts an object to a ProgParm parameter and assigns it to the data area."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Converts an object to a ProgParm parameter and assigns it to the data area.

## Overloads

| Signature | Description |
| --- | --- |
| [ObjectToParm](#void-objecttoparm-object-value-string-parametername)(void ObjectToParm(object Value, string ParameterName)) | Converts an object to a ProgParm parameter and assigns it to the data area. |
| [ObjectToParm](#void-objecttoparm-progparm-parameter-object-value)(void ObjectToParm(ProgParm Parameter, object Value)) | Converts an object to a ProgParm parameter and assigns it to the data area. |
| [ObjectToParm](#void-objecttoparm-progparm-parameter-object-value-int-element)(void ObjectToParm(ProgParm Parameter, object Value, int Element)) | Converts an object to a ProgParm parameter and assigns it to the data area. |
| [ObjectToParm](#void-objecttoparm-object-value-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)(void ObjectToParm(object Value, string ParameterName, [Int32\[\] ElementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))) | Converts an object to a ProgParm parameter and assigns it to the data area. |

<a id="void-objecttoparm-object-value-string-parametername"></a>
## void ObjectToParm(object Value, string ParameterName)

Converts an object to a ProgParm parameter and assigns it to the data area.

```cs
void ObjectToParm(object Value, string ParameterName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | The object to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParameterName | The name of the ProgParm parameter.

<a id="void-objecttoparm-progparm-parameter-object-value"></a>
## void ObjectToParm(ProgParm Parameter, object Value)

Converts an object to a ProgParm parameter and assigns it to the data area.

```cs
void ObjectToParm(ProgParm Parameter, object Value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Parameter | The ProgParm parameter to assign to.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | The object to convert.

<a id="void-objecttoparm-progparm-parameter-object-value-int-element"></a>
## void ObjectToParm(ProgParm Parameter, object Value, int Element)

Converts an object to a ProgParm parameter and assigns it to the data area.

```cs
void ObjectToParm(ProgParm Parameter, object Value, int Element)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | Parameter | The ProgParm parameter to assign to.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | The object to convert.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Element | The element index in the ProgParm parameter.

<a id="void-objecttoparm-object-value-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32"></a>
## void ObjectToParm(object Value, string ParameterName, [Int32\[\] ElementIndices](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts an object to a ProgParm parameter and assigns it to the data area.

```cs
void ObjectToParm(object Value, string ParameterName, Int32[] ElementIndices)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Value | The object to convert.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | ParameterName | The name of the ProgParm parameter.
| [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ElementIndices | The element indices in the ProgParm parameter.

## See Also
- [IDataArea interface class](i-data-area.html)
