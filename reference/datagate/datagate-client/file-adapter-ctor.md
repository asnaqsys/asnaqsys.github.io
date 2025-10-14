---
title: "FileAdapter Constructor"
description: "Initializes a new instance of the FileAdapter class. "
---

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the FileAdapter class.

## Overloads

| Name | Description |
| --- | --- |
| [FileAdapter()](#fileadapter) | Initializes a new instance of the FileAdapter class without a connection.
| [FileAdapter](#fileadapteradgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the FileAdapter class with a connection.
| [FileAdapter](#fileadapteradgconnection-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a connection and a file name.
| [FileAdapter](#fileadapteradgconnection-string-string)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a connection, a file name, and a member name.
| [FileAdapter](#fileadapterifileobject-string)([IFileObject](/reference/datagate/datagate-client/i-file-object.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the FileAdapter class with a FileObject and a member name.
| [FileAdapter](#fileadapterifileobject)([IFileObject](/reference/datagate/datagate-client/i-file-object.html)) | Initializes a new instance of the FileAdapter class with a FileObject.

## FileAdapter()

Initializes a new instance of the FileAdapter class without a connection.

```cs
FileAdapter()
```

### Remarks

This constructor creates an instance of **FileAdapter** without a database connection, file path, or member name. The `Open` method of such an instance cannot be used until its `FileName` and `Connection`properties are set (the constructor initializes these values to null). The `MemberName` property is initialized to null.  If **MemberName** is not explicitly set prior to a call to the **Open** method, DG assigns the value "*FIRST" to this property.

The `AccessMode` property is initialized with the value `Read`.

## FileAdapter(AdgConnection)

Initializes a new instance of the FileAdapter class with a connection.

```cs
FileAdapter(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The connection to use for the FileAdapter.

### Remarks

This constructor creates an instance of **FileAdapter** with the given database connection but without a file path or member name.  The `Open` method of such an instance cannot be used until its `FileName` property is set (the constructor initializes its value to null).  The `MemberName` property is initialized to null.  If **MemberName** is not explicitly set prior to a call to the **Open** method, DG assigns the value "*FIRST" to this property.

The `AccessMode` property is initialized with the value `Read`.

## FileAdapter(AdgConnection, String)

Initializes a new instance of the FileAdapter class with a connection and a file name.

```cs
FileAdapter(AdgConnection cn, String FileName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The connection to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | The name of the file to work with.

### Remarks

This constructor creates an instance of **FileAdapter** with the given database connection and file path but without a member name.  The `MemberName` property is initialized to null.  If **MemberName** is not explicitly set prior a call to the `Open` method, DG assigns the value "*FIRST" to this property.

The `AccessMode` property is initialized with the value Read.

## FileAdapter(AdgConnection, String, String)

Initializes a new instance of the FileAdapter class with a connection, a file name, and a member name.

```cs
FileAdapter(AdgConnection cn, String FileName, String MemberName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The connection to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | FileName | The name of the file to work with.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MemberName | The name of the member to work with.

### Example

```cs
    AdgConnection dataBase = createAdgConnection("MyDatabaseName");
    FileAdapter dbFile = new FileAdapter(dataBase, "SALESMAST", "WESTCOAST");  // Prepare Sales file with West Coast member
```

### Remarks

This constructor creates an instance of **FileAdapter** with the given database connection, file path, and member name (which are used to initialize the **Connection**, **FileName**, and **MemberName** properties respectively).  If the value of the given member name is null or an empty string, and the **MemberName** property is not otherwise set prior to a call to the `Open` method, DG assigns this property the value "*FIRST".

The `AccessMode` property is initialized with the value Read.

## FileAdapter(IFileObject, String)

Initializes a new instance of the FileAdapter class with a FileObject and a member name.

```cs
FileAdapter(IFileObject fileObject, String memberName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | fileObject | The FileObject to use for the FileAdapter.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | The name of the member to work with.

## FileAdapter([IFileObject](/reference/datagate/datagate-client/i-file-object.html))

Initializes a new instance of the FileAdapter class with a FileObject.

```cs
FileAdapter(IFileObject fileObject)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFileObject](/reference/datagate/datagate-client/i-file-object.html) | fileObject | The FileObject to use for the FileAdapter.
