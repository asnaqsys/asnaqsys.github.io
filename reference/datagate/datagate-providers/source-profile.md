---
title: SourceProfile class
---

Represents a source profile with various properties.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [SourceProfile()](#sourceprofile-) | Initializes a new instance of the SourceProfile class.
| [SourceProfile](#sourceprofile-sourceprofile-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the SourceProfile class with the properties of an existing SourceProfile.

### SourceProfile()

Initializes a new instance of the SourceProfile class.

```cs
SourceProfile()
```

### SourceProfile([SourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Initializes a new instance of the SourceProfile class with the properties of an existing SourceProfile.

```cs
SourceProfile(SourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | 

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | AltDecoderProps | Gets or sets the alternative decoder properties. |
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | AltEncoderProps | Gets or sets the alternative encoder properties. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AltEncodingName | Gets or sets the alternative encoding name. |
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | Credential | Gets or sets the credential. |
|  | DGPLATFORM | Constant for DataLink platform. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | InitialLibraryList | Get or Set initial library list |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSqlClientPlatform | Gets a value indicating whether the platform is SQL Client. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSqlPlatform | Gets a value indicating whether the platform is SQL. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Label | Get or Set label name |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PlatformAttribute | Gets or sets the platform attribute. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | PoolingTimeout | Gets or sets the pooling timeout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Port | Gets or sets the port. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Server | Get or Set server name |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ServicePrincipalName | Gets or sets the service principal name. |
|  | SQLCLIENTPLATFORM | Constant for SQL Client platform. |
|  | SQLOLEDBPLATFORM | Constant for SQL OLEDB platform. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SslCertificateName | Gets or sets the SSL certificate name. |
| [SslOptions](/reference/datagate/datagate-common/ssl-options.html) | SslOptions | Gets or sets the SSL options. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets the text. |

## Methods

| Signature | Description |
| --- | --- |
| [ToString()](#tostring-) | Returns a string that represents the current SourceProfile.
| [Clone()](#clone-) | Creates a new object that is a copy of the current instance.
| [IsKnownPlatformAttribute](#isknownplatformattribute-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the provided platform attribute is known.
| [op_Equality](#op_equality-sourceprofile-sourceprofile-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether two SourceProfile instances are equal.
| [op_Inequality](#op_inequality-sourceprofile-sourceprofile-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether two SourceProfile instances are not equal.
| [Equals](#equals-sourceprofile-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether the specified SourceProfile is equal to the current SourceProfile.
| [Equals](#equals-object-)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current SourceProfile.
| [Equals](#equals-object-boolean-)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Determines whether the specified object is equal to the current SourceProfile, with an option to ignore the database name.
| [GetHashCode()](#gethashcode-) | Serves as the default hash function.

### string ToString()

Returns a string that represents the current SourceProfile.

```cs
string ToString()
```

### object Clone()

Creates a new object that is a copy of the current instance.

```cs
object Clone()
```

### bool IsKnownPlatformAttribute([string platformAttr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether the provided platform attribute is known.

```cs
bool IsKnownPlatformAttribute(string platformAttr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | platformAttr | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the platform attribute is known; otherwise, false.

### bool op_Equality([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether two SourceProfile instances are equal.

```cs
bool op_Equality(SourceProfile x, SourceProfile y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | x | 
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | y | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the SourceProfiles are equal; otherwise, false.

### bool op_Inequality([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether two SourceProfile instances are not equal.

```cs
bool op_Inequality(SourceProfile x, SourceProfile y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | x | 
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | y | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the SourceProfiles are not equal; otherwise, false.

### bool Equals([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether the specified SourceProfile is equal to the current SourceProfile.

```cs
bool Equals(SourceProfile x, SourceProfile y)
```

### bool Equals([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether the specified object is equal to the current SourceProfile.

```cs
bool Equals(SourceProfile x, SourceProfile y)
```

### bool Equals([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether the specified object is equal to the current SourceProfile, with an option to ignore the database name.

```cs
bool Equals(SourceProfile x, SourceProfile y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | obj | 
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | bIgnoreDatabaseName | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is equal to the current SourceProfile; otherwise, false.

### int GetHashCode()

Serves as the default hash function.

```cs
int GetHashCode()
```
## Example

```cs 
  /* This creates a brand new database name using the
   * old source profile.*/
  SourceProfile newDbProfile2 = new SourceProfile("Brand New DB Name", sp);
```

