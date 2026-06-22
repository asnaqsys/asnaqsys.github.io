---
title: "InvariantCultureTypeConverter.GetProperties Method"
description: "Returns a collection of properties for the type of array specified by the value parameter, using the specified context and attributes."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Returns a collection of properties for the type of array specified by the value parameter, using the specified context and attributes.

<a id="propertydescriptorcollection-getproperties-itypedescriptorcontext-context-object-value-attribute-attributes-https-docs-microsoft-com-en-us-dotnet-api-system-attribute"></a>
## PropertyDescriptorCollection GetProperties(ITypeDescriptorContext context, object value, [Attribute\[\] attributes](https://docs.microsoft.com/en-us/dotnet/api/system.attribute))

Returns a collection of properties for the type of array specified by the value parameter, using the specified context and attributes.

#### Remarks
This method overrides the base implementation to ensure that the properties are retrieved using the wrapped converter's method.This is useful when you need to retrieve the properties of a type, and you want to ensure that the retrieval process is not affected by the current culture settings of the system.

```cs
PropertyDescriptorCollection GetProperties(ITypeDescriptorContext context, object value, Attribute[] attributes)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | An  that specifies the type of array for which to get properties.
| [Attribute\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) | attributes | An array of type  that is used as a filter.

#### Returns

| Type | Description
| --- | ---
| [PropertyDescriptorCollection](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.propertydescriptorcollection?view=net-8.0) | A  with the properties that are exposed for this data type, or null if there are no properties.

## See Also
- [InvariantCultureTypeConverter class](invariant-culture-type-converter.html)
