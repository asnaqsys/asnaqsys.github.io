---
title: "InvariantCultureTypeConverter.CanConvertFrom Method"
description: "Returns whether this converter can convert an object of the given type to the type of this converter, using the invariant culture."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns whether this converter can convert an object of the given type to the type of this converter, using the invariant culture.

<a id="bool-canconvertfrom-itypedescriptorcontext-context-type-sourcetype"></a>
## bool CanConvertFrom(ITypeDescriptorContext context, Type sourceType)

Returns whether this converter can convert an object of the given type to the type of this converter, using the invariant culture.

#### Remarks
This method overrides the base implementation to ensure that the conversion check is performed using the invariant culture.This is useful when you need to ensure that type conversion checks are not affected by the current culture settings of the system.

```cs
bool CanConvertFrom(ITypeDescriptorContext context, Type sourceType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | sourceType | A  that represents the type you want to convert from.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the converter can perform the conversion.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
