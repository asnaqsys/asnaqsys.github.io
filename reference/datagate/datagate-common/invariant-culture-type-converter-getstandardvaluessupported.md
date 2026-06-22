---
title: "InvariantCultureTypeConverter.GetStandardValuesSupported Method"
description: "Returns whether this object supports a standard set of values that can be picked from a list, using the wrapped converter's method."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns whether this object supports a standard set of values that can be picked from a list, using the wrapped converter's method.

<a id="bool-getstandardvaluessupported-itypedescriptorcontext-context"></a>
## bool GetStandardValuesSupported(ITypeDescriptorContext context)

Returns whether this object supports a standard set of values that can be picked from a list, using the wrapped converter's method.

#### Remarks
This method overrides the base implementation to ensure that the check is performed using the wrapped converter's method.This is useful when you need to determine if an object supports a standard set of values, and you want to ensure that the check is not affected by the current culture settings of the system.

```cs
bool GetStandardValuesSupported(ITypeDescriptorContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether this object supports a standard set of values that can be picked from a list.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
