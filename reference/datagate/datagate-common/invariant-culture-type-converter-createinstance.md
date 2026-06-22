---
title: "InvariantCultureTypeConverter.CreateInstance Method"
description: "Creates an instance of the type that this is associated with, using the specified context and the set of property values."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates an instance of the type that this is associated with, using the specified context and the set of property values.

<a id="object-createinstance-itypedescriptorcontext-context-idictionary-propertyvalues"></a>
## object CreateInstance(ITypeDescriptorContext context, IDictionary propertyValues)

Creates an instance of the type that this  is associated with, using the specified context and the set of property values.

#### Remarks
This method overrides the base implementation to ensure that the instance creation is performed using the wrapped converter.This is useful when you need to create an instance of a type using a set of property values, and you want to ensure that the creation process is not affected by the current culture settings of the system.

```cs
object CreateInstance(ITypeDescriptorContext context, IDictionary propertyValues)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2) | propertyValues | An  of new property values.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | An  that represents the created instance.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
