---
title: "InvariantCultureTypeConverter.CanConvertTo Method"
description: "Returns whether this converter can convert an object of this converter's type to the specified type, using the invariant culture."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns whether this converter can convert an object of this converter's type to the specified type, using the invariant culture.

<a id="bool-canconvertto-itypedescriptorcontext-context-type-destinationtype"></a>
## bool CanConvertTo(ITypeDescriptorContext context, Type destinationType)

Returns whether this converter can convert an object of this converter's type to the specified type, using the invariant culture.

#### Remarks
This method overrides the base implementation to ensure that the conversion check is performed using the invariant culture.This is useful when you need to ensure that type conversion checks are not affected by the current culture settings of the system.

```cs
bool CanConvertTo(ITypeDescriptorContext context, Type destinationType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | destinationType | A  that represents the type you want to convert to.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the converter can perform the conversion.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
