---
title: "SourceProfile class           | QSYS API Reference Guide"
description: "The SourceProfile class represents a profile in the source system. "
last_modified_at: 2024-08-09T17:25:07Z
---

The SourceProfile class represents a profile in the source system.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
This class is used to map the profile data from the source system to the target system.

<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [SourceProfile()](source-profile-ctor.html#sourceprofile) | Initializes a new instance of the  class with default values.
| [SourceProfile](source-profile-ctor.html#sourceprofilesourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the  class with the specified source profile.

For detailed constructor documentation, see [SourceProfile Constructors](source-profile-ctor.html).

## Properties

| Type | Name | Description
| --- | --- | --- 
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | AltDecoderProps | Gets or sets the alternative decoder properties for the source profile. |
| [ITransformProperties](/reference/datagate/datagate-providers/i-transform-properties.html) | AltEncoderProps | Gets or sets the alternative encoder properties for the source profile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AltEncodingName | Alternative character encoding string identifiers must becase-insensitive in the invariant culture. |
| [IDataGateCredential](/reference/datagate/datagate-providers/i-datagate-credential.html) | Credential | Gets or sets the credentials for the source profile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DGPLATFORM | Constant for the DataLink platform attribute. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | InitialLibraryList | Get or Set initial library list |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSqlClientPlatform | Gets a value indicating whether the platform attribute of the source profile is SQL Client-based. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSqlPlatform | Gets a value indicating whether the platform attribute of the source profile is SQL-based. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Label | Get or Set label name |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PlatformAttribute | Gets or sets the platform attribute for the source profile. |
| [Byte](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | PoolingTimeout | Gets or sets the pooling timeout for the source profile. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Port | Gets or sets the port for the source profile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Server | Get or Set server name |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ServicePrincipalName | Gets or sets the Service Principal Name (SPN) for the source profile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SQLCLIENTPLATFORM | Constant for the SQL Client platform attribute. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SQLOLEDBPLATFORM | Constant for the SQL OLE DB platform attribute. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SslCertificateName | Gets or sets the SSL certificate name for the source profile. |
| [SslOptions](/reference/datagate/datagate-common/ssl-options.html) | SslOptions | Gets or sets the SSL options for the source profile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets the text associated with the source profile. |

## Methods

| Signature | Description |
| --- | --- |
| [Clone()](source-profile-clone.html) | Creates a new object that is a copy of the current instance.
| [Equals](source-profile-equals.html)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether the current instance of  is equal to the specified instance.
| [Equals](source-profile-equals.html)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the current instance of  is equal to the specified instance.
| [Equals](source-profile-equals.html)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Determines whether the current instance of  is equal to the specified object.
| [GetHashCode()](source-profile-gethashcode.html) | Serves as the default hash function.
| [IsKnownPlatformAttribute](source-profile-isknownplatformattribute.html)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the provided platform attribute is a known platform attribute.
| [op_Equality](source-profile-op-equality.html)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether two instances of  are equal.
| [op_Inequality](source-profile-op-inequality.html)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether two instances of  are not equal.
| [ToString()](source-profile-tostring.html) | Returns a string that represents the current SourceProfile.

<!-- Inline method details removed; see individual method pages linked in the Methods table above. -->

## Examples

### Example: Using a Constructor

```cs 
  SourceProfile newDbProfile = new SourceProfile();
  newDbProfile.Server = "valid ip address";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Port = 5047;
  newDbProfile.PoolingTimeout = 0;
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";

```

### Example : Using a Constructor with an existing Source Profile.

```cs 
  /* This creates a brand new database name using the
   * old source profile.*/
  SourceProfile newDbProfile2 = new SourceProfile(sp);
```
