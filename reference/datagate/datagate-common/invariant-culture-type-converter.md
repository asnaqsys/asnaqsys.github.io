---
title: "InvariantCultureTypeConverter class"
description: "Provides a type converter to convert object types to and from string representations, using the invariant culture. "
last_modified_at: 2024-08-08T21:41:32Z
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
| [InvariantCultureTypeConverter](#invariantculturetypeconvertertypeconverter)([TypeConverter](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter?view=net-8.0)) | Initializes a new instance of the  class.

### InvariantCultureTypeConverter([TypeConverter](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter?view=net-8.0))

Initializes a new instance of the  class.

```cs
InvariantCultureTypeConverter(TypeConverter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TypeConverter](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter?view=net-8.0) | inner | The  instance that this converter wraps.

## Methods

| Signature | Description |
| --- | --- |
| [CanConvertFrom](#bool-canconvertfromitypedescriptorcontext-context-type-sourcetype)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Returns whether this converter can convert an object of the given type to the type of this converter, using the invariant culture.
| [CanConvertTo](#bool-canconverttoitypedescriptorcontext-context-type-destinationtype)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Returns whether this converter can convert an object of this converter's type to the specified type, using the invariant culture.
| [ConvertFrom](#object-convertfromitypedescriptorcontext-context-cultureinfo-culture-object-value)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Converts the given value object to the type of this converter, using the invariant culture.
| [ConvertTo](#object-converttoitypedescriptorcontext-context-cultureinfo-culture-object-value-type-destinationtype)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Converts the given value object to the specified type, using the invariant culture.
| [CreateInstance](#object-createinstanceitypedescriptorcontext-context-idictionary-propertyvalues)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [IDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2)) | Creates an instance of the type that this  is associated with, using the specified context and the set of property values.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object, using the wrapped converter's Equals method.
| [GetCreateInstanceSupported](#bool-getcreateinstancesupporteditypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether changing a value on this object requires a call to the  method to create a new value.
| [GetHashCode()](#int-gethashcode) | Serves as the default hash function, using the wrapped converter's GetHashCode method.
| [GetProperties](#propertydescriptorcollection-getpropertiesitypedescriptorcontext-context-object-value-attribute--attributes)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Attribute\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.attribute)) | Returns a collection of properties for the type of array specified by the value parameter, using the specified context and attributes.
| [GetPropertiesSupported](#bool-getpropertiessupporteditypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether this object supports properties, using the wrapped converter's method.
| [GetStandardValues](#standardvaluescollection-getstandardvaluesitypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns a collection of standard values for the data type this type converter is designed for when provided with a format context.
| [GetStandardValuesExclusive](#bool-getstandardvaluesexclusiveitypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether the collection of standard values returned from  is an exclusive list of possible values, using the wrapped converter's method.
| [GetStandardValuesSupported](#bool-getstandardvaluessupporteditypedescriptorcontext-context)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0)) | Returns whether this object supports a standard set of values that can be picked from a list, using the wrapped converter's method.
| [IsValid](#bool-isvaliditypedescriptorcontext-context-object-value)([ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Returns whether the given value object is valid for this type and for the specified context, using the wrapped converter's method.
| [ToString()](#string-tostring) | Returns a string that represents the current object, using the wrapped converter's ToString method.

### bool CanConvertFrom([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Type sourceType](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Returns whether this converter can convert an object of the given type to the type of this converter, using the invariant culture.


#### Remarks
This method overrides the base implementation to ensure that the conversion check is performed using the invariant culture.This is useful when you need to ensure that type conversion checks are not affected by the current culture settings of the system.

```cs
bool CanConvertFrom(ITypeDescriptorContext context, Type sourceType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | sourceType | A  that represents the type you want to convert from.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the converter can perform the conversion.

### bool CanConvertTo([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [Type destinationType](https://docs.microsoft.com/en-us/dotnet/api/system.type))

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

### object ConvertFrom([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [CultureInfo culture](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

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

### object ConvertTo([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [CultureInfo culture](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Type destinationType](https://docs.microsoft.com/en-us/dotnet/api/system.type))

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

### object CreateInstance([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [IDictionary propertyValues](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.idictionary-2))

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

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the specified object is equal to the current object, using the wrapped converter's Equals method.


#### Remarks
This method overrides the base implementation to ensure that the equality check is performed using the wrapped converter's Equals method.This is useful when you need to ensure that equality checks are not affected by the current culture settings of the system.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The  to compare with the current object.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether the specified object is equal to the current object.

### bool GetCreateInstanceSupported([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0))

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

### int GetHashCode()

Serves as the default hash function, using the wrapped converter's GetHashCode method.


#### Remarks
This method overrides the base implementation to ensure that the hash code is generated using the wrapped converter's GetHashCode method.This is useful when you need to ensure that hash code generation is not affected by the current culture settings of the system.

```cs
int GetHashCode()
```

### PropertyDescriptorCollection GetProperties([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Attribute\[\] attributes](https://docs.microsoft.com/en-us/dotnet/api/system.attribute))

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

### bool GetPropertiesSupported([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0))

Returns whether this object supports properties, using the wrapped converter's method.


#### Remarks
This method overrides the base implementation to ensure that the check is performed using the wrapped converter's method.This is useful when you need to determine if an object supports properties, and you want to ensure that the check is not affected by the current culture settings of the system.

```cs
bool GetPropertiesSupported(ITypeDescriptorContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents whether this object supports properties.

### StandardValuesCollection GetStandardValues([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0))

Returns a collection of standard values for the data type this type converter is designed for when provided with a format context.


#### Remarks
This method overrides the base implementation to ensure that the standard values are retrieved using the wrapped converter's method.This is useful when you need to retrieve the standard values of a type, and you want to ensure that the retrieval process is not affected by the current culture settings of the system.

```cs
StandardValuesCollection GetStandardValues(ITypeDescriptorContext context)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ITypeDescriptorContext](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0) | context | An  that provides a format context.

#### Returns

| Type | Description
| --- | ---
| [StandardValuesCollection](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.typeconverter.standardvaluescollection.item?view=net-8.0) | A  that holds a standard set of valid values, or null if the data type does not support a standard set of values.

### bool GetStandardValuesExclusive([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0))

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

### bool GetStandardValuesSupported([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0))

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

### bool IsValid([ITypeDescriptorContext context](https://learn.microsoft.com/en-us/dotnet/api/system.componentmodel.itypedescriptorcontext?view=net-8.0), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

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

### string ToString()

Returns a string that represents the current object, using the wrapped converter's ToString method.


#### Remarks
This method overrides the base implementation to ensure that the string representation is generated using the wrapped converter's ToString method.This is useful when you need to ensure that the string representation of the object is not affected by the current culture settings of the system.

```cs
string ToString()
```
