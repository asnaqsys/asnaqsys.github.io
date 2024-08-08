---
title: "SourceProfile class           | QSYS API Reference Guide"
description: "The SourceProfile class represents a profile in the source system. "
last_modified_at: 2024-08-08T21:41:32Z
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
| [SourceProfile()](#sourceprofile) | Initializes a new instance of the  class with default values.
| [SourceProfile](#sourceprofilesourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the  class with the specified source profile.

### SourceProfile()

Initializes a new instance of the  class with default values.

```cs
SourceProfile()
```

### SourceProfile([SourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Initializes a new instance of the  class with the specified source profile.

```cs
SourceProfile(SourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The source profile to initialize the new instance with.

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
| [Clone()](#object-clone) | Creates a new object that is a copy of the current instance.
| [Equals](#bool-equalssourceprofile-other)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether the current instance of  is equal to the specified instance.
| [Equals](#bool-equalsobject-other)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the current instance of  is equal to the specified instance.
| [Equals](#bool-equalsobject-obj-bool-bignoredatabasename)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Determines whether the current instance of  is equal to the specified object.
| [GetHashCode()](#int-gethashcode) | Serves as the default hash function.
| [IsKnownPlatformAttribute](#bool-isknownplatformattributestring-platformattr)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the provided platform attribute is a known platform attribute.
| [op_Equality](#bool-op-equalitysourceprofile-x-sourceprofile-y)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether two instances of  are equal.
| [op_Inequality](#bool-op-inequalitysourceprofile-x-sourceprofile-y)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Determines whether two instances of  are not equal.
| [ToString()](#string-tostring) | Returns a string that represents the current SourceProfile.

### object Clone()

Creates a new object that is a copy of the current instance.


#### Remarks
This method is used to create a copy of the current instance of the SourceProfile class. The copy is made by calling the Copy method with a new instance of the SourceProfile class and the current instance as parameters.

```cs
object Clone()
```

### bool Equals([SourceProfile other](/reference/datagate/datagate-providers/source-profile.html))

Determines whether the current instance of  is equal to the specified instance.


#### Remarks
This method is used to compare the current instance with another instance of the SourceProfile class. The comparison is based on the properties of the instances.

```cs
bool Equals(SourceProfile other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | other | The instance to compare with the current instance.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the current instance is equal to the specified instance; otherwise, false.

### bool Equals([object other](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the current instance of  is equal to the specified instance.

```cs
bool Equals(object other)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | other | The instance to compare with the current instance.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the current instance is equal to the specified instance; otherwise, false.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object), [bool bIgnoreDatabaseName](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Determines whether the current instance of  is equal to the specified object.


#### Remarks
This method is used to compare the current instance with another object of the same type. If the `bIgnoreDatabaseName` parameter is set to true, the comparison will ignore the database name.

```cs
bool Equals(object obj, bool bIgnoreDatabaseName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current instance.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bIgnoreDatabaseName | A boolean value that indicates whether to ignore the database name in the comparison.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the current instance is equal to the specified object; otherwise, false.

### int GetHashCode()

Serves as the default hash function.


#### Remarks
This method is used to generate a hash code for the current instance of the SourceProfile class. It takes into account all the properties of the class to generate a unique hash code.

```cs
int GetHashCode()
```

### bool IsKnownPlatformAttribute([string platformAttr](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether the provided platform attribute is a known platform attribute.


#### Remarks
This method is used to validate that the platform attribute provided is one that the system recognizes and can handle.

```cs
bool IsKnownPlatformAttribute(string platformAttr)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | platformAttr | The platform attribute to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the provided platform attribute is a known platform attribute; otherwise, false.

### bool op_Equality([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether two instances of  are equal.

```cs
bool op_Equality(SourceProfile x, SourceProfile y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | x | The first instance to compare.
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | y | The second instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the instances are equal; otherwise, false.

### bool op_Inequality([SourceProfile x](/reference/datagate/datagate-providers/source-profile.html), [SourceProfile y](/reference/datagate/datagate-providers/source-profile.html))

Determines whether two instances of  are not equal.

```cs
bool op_Inequality(SourceProfile x, SourceProfile y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | x | The first instance to compare.
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | y | The second instance to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the instances are not equal; otherwise, false.

### string ToString()

Returns a string that represents the current SourceProfile.


#### Remarks
This method overrides the base ToString method and provides a string representation of the SourceProfile, typically including key properties of the SourceProfile for debugging or logging purposes.

```cs
string ToString()
```

## Example 1. Most simple constructor.

```cs 
  /* Opens the database "*PUBLIC/DG NET iSeries" and changes the user
   * name and password. */
  SourceProfile sp = new SourceProfile("*PUBLIC/DG NET iSeries");
  sp.User = "NewUser";
  sp.Password = "NewPassword";
  sp.Register(); /* Updates the information. */

```

## Example 2. Using Constructor using an existing Source Profile.

```cs 
  /* This creates a brand new database name using the
   * old source profile.*/
  SourceProfile newDbProfile2 = new SourceProfile("Brand New DB Name", sp);
```

## Example 3. Using Constructor bypassing Registry.


```cs 
  /* When we specify false with this constructor, we're
   * telling Datagate not to get information from the
   * registry. Thus we can use it to create an entirely
   * new database name. */
  SourceProfile newDbProfile = new SourceProfile("New database", false);
  newDbProfile.Server = "valid ip address";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Port = 5047;
  newDbProfile.PoolingTimeout = 0;
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();

```


## Example 4. Unregistering a Database Profile

```cs 
  /* Open up and unregistered the database profile "Worthless Db". */
  try
  {
      SourceProfile.Unregister("Worthless Db");
  }
  catch(dgException)
  {
      MessageBox.Show("\"Worthless DB\" is not a 
            registered database profile.",
          "Could not unregister.");
      return;
  }
```

## Example 5. Getting a List of Database Names

```cs 
  /* This code displays all of the *PUBLIC database
   * names, along with their descriptive text, to the list view
   * "lvDbNames" whose view is set to "View.Details". */
  ListViewItem newItem;
  SourceProfile currentProfile;
  foreach(string name in SourceProfile.GetNames(true))
  {
      currentProfile = new SourceProfile(name);
      newItem = new ListViewItem(currentProfile.DatabaseName);
      newItem.SubItems.Add(currentProfile.Text);
      lvDbNames.Items.Add(newItem);
  }
```

## Example 6. Use of Server property.

```cs 
  /* The code below updates a database profile to use a different IP address. */
  SourceProfile sp = new SourceProfile("CustomerDB");
  sp.Server = "555.93.279.303";
  sp.Register(); /* Save changes. */

```

## Example 7. Updating User and password, and then saves the changes by calling Register. 

```cs 
  /* When we specify false with this constructor, we're
   * telling Datagate not to get information from the
   * registry. Thus we can use it to create an entirely
   * new database name. */
  SourceProfile newDbProfile = new SourceProfile("New database", false);
  newDbProfile.Server = "valid ip address";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Port = 5047;
  newDbProfile.PoolingTimeout = 0;
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();
```

## Example 8. Using the PoolingTimeout property.

```cs 
  /* Connect using the already established database name 
   * "*PUBLIC/DG NET iSeries" but use a different idle
   * timeout time. */
  SourceProfile sp = new SourceProfile("*PUBLIC/DG NET iSeries");
  sp.PoolingTimeout = 10;
  AdgConnection database = new AdgConnection(sp);

```

## Example 9. Using the Platform property.

```cs 
  /* Register the database name "My Local" to specify the local database. */
  SourceProfile newDbProfile = new SourceProfile("My Local", false);
  newDbProfile.Server = "*LOCAL";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Label = "DG 7 Database";
  newDbProfile.PoolingTimeout = 0;
  /* Specify *DATALINK since we're connecting to the datagate engine. */
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();
```

## Example 10. Using the PasswordType property.

```cs 
  /* Connect using the already established database name 
   * "*PUBLIC/DG NET iSeries" but use a different
   * username and password. */
  SourceProfile sp = new SourceProfile("*PUBLIC/DG NET iSeries");
  sp.User = "NewUser";
  sp.Password = "NewPassword";
  sp.PasswordType = "Legacy";
  AdgConnection database = new AdgConnection(sp);

```

## Example 11. Using the Label property.

```cs 
  /* Register the database name "My Local" to specify the local database.
   * Because the local database is a Windows DataGate server, 
   * you need to include a valid label as well. */
  SourceProfile newDbProfile = new SourceProfile("My Local", false);
  newDbProfile.Server = "*LOCAL";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Label = "DG 7 Database";
  newDbProfile.PoolingTimeout = 0;
  /* Specify *DATALINK since we're connecting to the datagate engine. */
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();
```

## Example 12. Changing the Initial Library List.

```cs 
  /* This code will update the database name "SalesDB" to include
   * "IMPORTS" in its library list. */
  SourceProfile sp = new SourceProfile("SalesDB");
  string[] newList = new string[sp.InitialLibl.Length + 1];
  int i;
  for (i = 0; i< sp.InitialLibl.Length; i ++)
  {
      newList[i] = sp.InitialLibl[i];
  }
  newList[i] = "IMPORTS";
  sp.InitialLibl = newList;
  sp.Register();
```

## Example 13. Loading a ComboBox with Database Names.

```cs 
  /* This code will fill a combo box with all of the available database
   * names. */
  foreach(string name in SourceProfile.GetNames(true)) /* Get *PUBLIC databases. */
      cbDbName.Items.Add(name); /* NOTE: The names appear without the "*PUBLIC/" prefix. */
  foreach(string name in SourceProfile.GetNames(false)) /* Get non public databases. */
      cbDbName.Items.Add(name);
```

