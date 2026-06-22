---
title: "InvariantCultureTypeConverter.GetCreateInstanceSupported Method"
description: "Returns whether changing a value on this object requires a call to the method to create a new value."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns whether changing a value on this object requires a call to the method to create a new value.

<a id="bool-getcreateinstancesupported-itypedescriptorcontext-context"></a>
## bool GetCreateInstanceSupported(ITypeDescriptorContext context)

Returns whether changing a value on this object requires a call to the  method to create a new value.

#### Remarks
This method overrides the base implementation to ensure that the check is performed using the wrapped converter's method.This is useful when you need to determine if an instance of a type can be created from a set of property values, and you want to ensure that the check is not affected by the current culture settings of the system.

```cs
bool GetCreateInstanceSupported(ITypeDescriptorContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether changing a value on this object requires a call to  to create a new value.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
