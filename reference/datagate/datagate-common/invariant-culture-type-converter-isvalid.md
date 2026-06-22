---
title: "InvariantCultureTypeConverter.IsValid Method"
description: "Returns whether the given value object is valid for this type and for the specified context, using the wrapped converter's method."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns whether the given value object is valid for this type and for the specified context, using the wrapped converter's method.

<a id="bool-isvalid-itypedescriptorcontext-context-object-value"></a>
## bool IsValid(ITypeDescriptorContext context, object value)

Returns whether the given value object is valid for this type and for the specified context, using the wrapped converter's method.

#### Remarks
This method overrides the base implementation to ensure that the validity check is performed using the wrapped converter's method.This is useful when you need to ensure that validity checks are not affected by the current culture settings of the system.

```cs
bool IsValid(ITypeDescriptorContext context, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The  to evaluate for validity.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the specified object value is valid for this type and for the specified context.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
