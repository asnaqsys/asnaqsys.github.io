---
title: "InvariantCultureTypeConverter.ConvertTo Method"
description: "Converts the given value object to the specified type, using the invariant culture."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Converts the given value object to the specified type, using the invariant culture.

<a id="object-convertto-itypedescriptorcontext-context-cultureinfo-culture-object-value-type-destinationtype"></a>
## object ConvertTo(ITypeDescriptorContext context, CultureInfo culture, object value, Type destinationType)

Converts the given value object to the specified type, using the invariant culture.

#### Remarks
This method overrides the base implementation to ensure that the conversion is performed using the invariant culture, regardless of the culture parameter provided.This is useful when you need to ensure that type conversions are not affected by the current culture settings of the system.

```cs
object ConvertTo(ITypeDescriptorContext context, CultureInfo culture, object value, Type destinationType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) | culture | The  to use as the current culture. This is not used in this implementation, as the invariant culture is always used.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The  to convert.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | destinationType | The  that represents the type you want to convert to.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An  that represents the converted value.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
