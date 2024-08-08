---
title: "DatabaseLabel class           | QSYS API Reference Guide"
description: "The `DatabaseLabel` class provides static methods for managing and interacting with database labels in a DataGate environment. "
last_modified_at: 2024-08-08T21:41:32Z
---

The `DatabaseLabel` class provides static methods for managing and interacting with database labels in a DataGate environment.

**Namespace:** ASNA.DataGate.Client.DatabaseLabel
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks
This class includes methods for creating, changing, and removing databases, as well as retrieving and manipulating labels.
Labels are used to identify and manage databases in the DataGate environment. They can be retrieved either individually, by name, or as a collection.
The class also provides methods for labeling and unlabeling databases, and for creating new label objects.

<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [ChangeDatabase](#void-changedatabasesourceprofile-serverandcredentials-ilabel-label)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [ILabel](/reference/datagate/datagate-client/i-label.html)) | Modifies database label
| [CreateDatabase](#void-createdatabasesourceprofile-serverandcredentials-bool-bissecured-ilabel-label)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ILabel](/reference/datagate/datagate-client/i-label.html)) | Creates a database
| [CreateDatabase](#void-createdatabasesourceprofile-serverandcredentials-bool-bissecured-ilabel-plabel-int-tcpport)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ILabel](/reference/datagate/datagate-client/i-label.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Creates a database
| [CreateLabelObject()](#ilabel-createlabelobject) | Creates an ILabel object with default values
| [GetLabel](#ilabel-getlabelsourceprofile-sp-string-lblname)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Retrieves a specific label from a given server.
| [GetLabels](#ilabel--getlabelssourceprofile-sp)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Creates a list of all labels in a given server
| [RemoveDatabase](#void-removedatabasesourceprofile-sourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Completely erases a database and its label.
| [UnlabelDatabase](#void-unlabeldatabasesourceprofile-source)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Remove a label on a database

### void ChangeDatabase([SourceProfile serverAndCredentials](/reference/datagate/datagate-providers/source-profile.html), [ILabel label](/reference/datagate/datagate-client/i-label.html))

Modifies database label

```cs
void ChangeDatabase(SourceProfile serverAndCredentials, ILabel label)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | serverAndCredentials | Object identifying the server,            user and password, or kerberos SPN.
| [ILabel](/reference/datagate/datagate-client/i-label.html) | label | Label details

### void CreateDatabase([SourceProfile serverAndCredentials](/reference/datagate/datagate-providers/source-profile.html), [bool bIsSecured](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ILabel label](/reference/datagate/datagate-client/i-label.html))

Creates a database

```cs
void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel label)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | serverAndCredentials | Object identifying the server            and client credentials.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bIsSecured | Whether the database is secure
| [ILabel](/reference/datagate/datagate-client/i-label.html) | label | Label details for the database

### void CreateDatabase([SourceProfile serverAndCredentials](/reference/datagate/datagate-providers/source-profile.html), [bool bIsSecured](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ILabel pLabel](/reference/datagate/datagate-client/i-label.html), [int tcpPort](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Creates a database

```cs
void CreateDatabase(SourceProfile serverAndCredentials, bool bIsSecured, ILabel pLabel, int tcpPort)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | serverAndCredentials | Object identifying the server            and client credentials.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bIsSecured | Whether the database is secure
| [ILabel](/reference/datagate/datagate-client/i-label.html) | pLabel | Label details for the database
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | tcpPort | The TCP port number the server listens to.            

### ILabel CreateLabelObject()

Creates an ILabel object with default values

```cs
ILabel CreateLabelObject()
```

### ILabel GetLabel([SourceProfile sp](/reference/datagate/datagate-providers/source-profile.html), [string lblName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Retrieves a specific label from a given server.


#### Remarks
This method uses the  method to retrieve all labels from the server specified in the source profile.It then uses LINQ to filter the labels based on the provided name, using a case-insensitive comparison.If a label with the provided name is found, it is returned; otherwise, the method returns null.

```cs
ILabel GetLabel(SourceProfile sp, string lblName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The source profile containing server and user credentials.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | lblName | The name of the label to retrieve.

#### Returns

| Type | Description
| --- | ---
| [ILabel](/reference/datagate/datagate-client/i-label.html) | The label matching the provided name, or null if no match is found.

### ILabel\[\] GetLabels([SourceProfile sp](/reference/datagate/datagate-providers/source-profile.html))

Creates a list of all labels in a given server

```cs
ILabel[] GetLabels(SourceProfile sp)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | Connection parameters defining the machine to            to search, server TCP port, user credentials, and Krb5 SPN.            

#### Returns

| Type | Description
| --- | ---
| [ILabel\[\]](/reference/datagate/datagate-client/i-label.html) | Array of labels

### void RemoveDatabase([SourceProfile sourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Completely erases a database and its label.

```cs
void RemoveDatabase(SourceProfile sourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sourceProfile | Provides server host name, port,            database label to delete, and user credentials.

### void UnlabelDatabase([SourceProfile source](/reference/datagate/datagate-providers/source-profile.html))

Remove a label on a database

```cs
void UnlabelDatabase(SourceProfile source)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | source | Provides Label name, server, port, and access            credentials.
