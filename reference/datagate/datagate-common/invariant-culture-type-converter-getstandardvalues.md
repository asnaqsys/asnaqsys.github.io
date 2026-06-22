---
title: "InvariantCultureTypeConverter.GetStandardValues Method"
description: "Returns a collection of standard values for the data type this type converter is designed for when provided with a format context."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns a collection of standard values for the data type this type converter is designed for when provided with a format context.

<a id="standardvaluescollection-getstandardvalues-itypedescriptorcontext-context"></a>
## StandardValuesCollection GetStandardValues(ITypeDescriptorContext context)

Returns a collection of standard values for the data type this type converter is designed for when provided with a format context.

#### Remarks
This method overrides the base implementation to ensure that the standard values are retrieved using the wrapped converter's method.This is useful when you need to retrieve the standard values of a type, and you want to ensure that the retrieval process is not affected by the current culture settings of the system.

```cs
StandardValuesCollection GetStandardValues(ITypeDescriptorContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.

#### Returns

| Type | Description
| --- | ---
| [StandardValuesCollection](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter.standardvaluescollection.item?view=net-8.0) | A  that holds a standard set of valid values, or null if the data type does not support a standard set of values.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
