---
title: "InvariantCultureTypeConverter.GetStandardValuesExclusive Method"
description: "Returns whether the collection of standard values returned from is an exclusive list of possible values, using the wrapped converter's method."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns whether the collection of standard values returned from is an exclusive list of possible values, using the wrapped converter's method.

<a id="bool-getstandardvaluesexclusive-itypedescriptorcontext-context"></a>
## bool GetStandardValuesExclusive(ITypeDescriptorContext context)

Returns whether the collection of standard values returned from  is an exclusive list of possible values, using the wrapped converter's method.

#### Remarks
This method overrides the base implementation to ensure that the check is performed using the wrapped converter's method.This is useful when you need to determine if the standard values of a type form an exclusive list, and you want to ensure that the check is not affected by the current culture settings of the system.

```cs
bool GetStandardValuesExclusive(ITypeDescriptorContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the collection of standard values is an exclusive list.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
