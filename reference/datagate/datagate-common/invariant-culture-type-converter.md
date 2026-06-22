---
title: "InvariantCultureTypeConverter class"
description: "Provides a type converter to convert object types to and from string representations, using the invariant culture. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides a type converter to convert object types to and from string representations, using the invariant culture.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [TypeConverter](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter?view=net-8.0)
<br>
<br>

## Remarks
This class is a wrapper around a  instance, and overrides its methods to ensure that all conversions are performed using the invariant culture.
This is useful when you need to ensure that type conversions are not affected by the current culture settings of the system.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [InvariantCultureTypeConverter](invariant-culture-type-converter-ctor.html#invariantculturetypeconverter-typeconverter)([TypeConverter](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter?view=net-8.0)) | Initializes a new instance of the  class.

## Methods

| Signature | Description |
| --- | --- |
| [CanConvertFrom](invariant-culture-type-converter-canconvertfrom.html#bool-canconvertfrom-itypedescriptorcontext-context-type-sourcetype)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Returns whether this converter can convert an object of the given type to the type of this converter, using the invariant culture.
| [CanConvertTo](invariant-culture-type-converter-canconvertto.html#bool-canconvertto-itypedescriptorcontext-context-type-destinationtype)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Returns whether this converter can convert an object of this converter's type to the specified type, using the invariant culture.
| [ConvertFrom](invariant-culture-type-converter-convertfrom.html#object-convertfrom-itypedescriptorcontext-context-cultureinfo-culture-object-value)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Converts the given value object to the type of this converter, using the invariant culture.
| [ConvertTo](invariant-culture-type-converter-convertto.html#object-convertto-itypedescriptorcontext-context-cultureinfo-culture-object-value-type-destinationtype)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Converts the given value object to the specified type, using the invariant culture.
| [CreateInstance](invariant-culture-type-converter-createinstance.html#object-createinstance-itypedescriptorcontext-context-idictionary-propertyvalues)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2)) | Creates an instance of the type that this  is associated with, using the specified context and the set of property values.
| [Equals](invariant-culture-type-converter-equals.html#bool-equals-object-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object, using the wrapped converter's Equals method.
| [GetCreateInstanceSupported](invariant-culture-type-converter-getcreateinstancesupported.html#bool-getcreateinstancesupported-itypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether changing a value on this object requires a call to the  method to create a new value.
| [GetHashCode()](invariant-culture-type-converter-gethashcode.html#int-gethashcode) | Serves as the default hash function, using the wrapped converter's GetHashCode method.
| [GetProperties](invariant-culture-type-converter-getproperties.html#propertydescriptorcollection-getproperties-itypedescriptorcontext-context-object-value-attribute-attributes-https-docs-microsoft-com-en-us-dotnet-api-system-attribute)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Attribute\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | Returns a collection of properties for the type of array specified by the value parameter, using the specified context and attributes.
| [GetPropertiesSupported](invariant-culture-type-converter-getpropertiessupported.html#bool-getpropertiessupported-itypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether this object supports properties, using the wrapped converter's method.
| [GetStandardValues](invariant-culture-type-converter-getstandardvalues.html#standardvaluescollection-getstandardvalues-itypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns a collection of standard values for the data type this type converter is designed for when provided with a format context.
| [GetStandardValuesExclusive](invariant-culture-type-converter-getstandardvaluesexclusive.html#bool-getstandardvaluesexclusive-itypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether the collection of standard values returned from  is an exclusive list of possible values, using the wrapped converter's method.
| [GetStandardValuesSupported](invariant-culture-type-converter-getstandardvaluessupported.html#bool-getstandardvaluessupported-itypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether this object supports a standard set of values that can be picked from a list, using the wrapped converter's method.
| [IsValid](invariant-culture-type-converter-isvalid.html#bool-isvalid-itypedescriptorcontext-context-object-value)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Returns whether the given value object is valid for this type and for the specified context, using the wrapped converter's method.
| [ToString()](invariant-culture-type-converter-tostring.html#string-tostring) | Returns a string that represents the current object, using the wrapped converter's ToString method.

