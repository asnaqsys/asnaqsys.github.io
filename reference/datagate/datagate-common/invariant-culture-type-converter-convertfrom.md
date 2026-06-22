---
title: "InvariantCultureTypeConverter.ConvertFrom Method"
description: "Converts the given value object to the type of this converter, using the invariant culture."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Converts the given value object to the type of this converter, using the invariant culture.

<a id="object-convertfrom-itypedescriptorcontext-context-cultureinfo-culture-object-value"></a>
## object ConvertFrom(ITypeDescriptorContext context, CultureInfo culture, object value)

Converts the given value object to the type of this converter, using the invariant culture.

#### Remarks
This method overrides the base implementation to ensure that the conversion is performed using the invariant culture, regardless of the culture parameter provided.This is useful when you need to ensure that type conversions are not affected by the current culture settings of the system.

```cs
object ConvertFrom(ITypeDescriptorContext context, CultureInfo culture, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) | culture | The  to use as the current culture. This is not used in this implementation, as the invariant culture is always used.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The  to convert.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An  that represents the converted value.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
