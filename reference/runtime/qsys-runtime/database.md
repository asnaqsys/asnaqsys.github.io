---
title: "Database class                | QSYS API Reference Guide"
description: "Handles connections to a Database. "
last_modified_at: 2024-08-09T16:18:25Z
---

Handles connections to a Database.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Database](#databasestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructs a Database object using a database name. 
| [Database](#databasestring-virtualterminal-openaccessdspf)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [VirtualTerminal](/reference/runtime/qsys-runtime/virtual-terminal.html), [OpenAccessDspF](/reference/runtime/qsys-runtime/open-access-dsp-f.html)) | Constructs a Database object using a database name, VirtualTerminal value, and OpenAccessDspF value.

### Database([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Constructs a Database object using a database name. 

```cs
Database(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | databaseName | Database name.

### Database([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [VirtualTerminal](/reference/runtime/qsys-runtime/virtual-terminal.html), [OpenAccessDspF](/reference/runtime/qsys-runtime/open-access-dsp-f.html))

Constructs a Database object using a database name, VirtualTerminal value, and OpenAccessDspF value.

```cs
Database(String, VirtualTerminal, OpenAccessDspF)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | databaseName | Database name.
| [VirtualTerminal](/reference/runtime/qsys-runtime/virtual-terminal.html) | virtualTerminal | Value that specifies whether this connection will be used for an interactive virtual terminal connection.
| [OpenAccessDspF](/reference/runtime/qsys-runtime/open-access-dsp-f.html) | openAccessDspF | Value that specifies whether this connection is for use with Open Access RPG programs.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | Connection | Gets the DataGate Connection instance. |
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CurrentUserLibl | Sets the current library list for the current connection.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DBName | Gets the Database Name. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | DefaultJobCodePageID | Gets or sets the Job's default Code Page ID. |
| [dgException](/reference/datagate/datagate-common/dg-exception.html) | InitialException | Gets the initial DataGate exception. |
| [IEnumerable\<String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | InitialLibl | Gets or sets the current database initial library list. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsInteractive | Gets a boolean value indicating that the Database is associated with an Interactive Job. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsOpen | Returns a True or False indicating if the database is open. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Label | Gets or sets a string containing the label of the database to connect to. |
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NameStoreConfigFiles | Gets the list of the database name store configuration files. |
| [NameStoreOptions](/reference/runtime/qsys-runtime/name-store-options.html) | NameStoreOptions | Gets the database name store options. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | NameStorePrepared | Gets whether the database name store has already been set for the process. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Password | Sets the password to be used in conjunction with User for connection authentication. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PlatformAttribute | Gets or sets a platform-specific attribute of the database engine. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PoolingTimeout | Gets or sets the database PoolingTimeOut (in minutes).  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Port | Gets or sets the TCP port number used by the database server for TCP/IP-based transport (default 5042). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Server | The database server host machine name.  |
| [ServerSupport](/reference/runtime/qsys-runtime/server-support.html) | ServerSupport | For interactive connections, determines if program can issue server requests like open file or call program. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SslCertificateName | Gets or sets the SSL Certificate name for the database connection. |
| [SslOptions](/reference/datagate/datagate-common/ssl-options.html) | SslOptions | Gets or sets the SLL Options for the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | TerminalDeviceName | For interactive connections, determines the name of the device. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | Gets or sets a description of the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | User | Gets or sets the user name that used to authorize thecurrent database connection.  |
| [VirtualTerminal](/reference/runtime/qsys-runtime/virtual-terminal.html) | VirtualTerminal | VirtualTerminal summary. |

## Methods

| Signature | Description |
| --- | --- |
| [AddMember](#void-addmemberstring-filepath-string-membername)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Add a member to a file.
| [ClearMember](#void-clearmemberstring-filepath-string-membername)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Clear a file member.
| [Close()](#void-close) | Closes a connection to a Database.
| [Commit](#void-commitstring-boundary)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Commits an open transaction.
| [Connect()](#void-connect) | Open a connection to a Database.
| [CopyFileToDb](#void-copyfiletodbstring-filepath-database-todb-string-todirectory-bool-copydata)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a file with all its members and data, if they exist, from the current Database to another Database.
| [CopyLogicalFileToDb](#void-copylogicalfiletodbstring-filepath-database-todb-string-todirectory-bool-replacebasefiles-bool-copydata)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/runtime/qsys-runtime/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a logical file and its base physical files from the current Database to another Database.
| [CreateDirectory](#void-createdirectorystring-directoryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new directory (library) in the Database.
| [DeleteFile](#void-deletefilestring-filepath)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Deletes a file from the Database.
| [Dispose](#void-disposebool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases resources.
| [Dispose()](#void-dispose) | Releases resources.
| [EndTpm()](#void-endtpm) | Ends a Database transaction operation.
| [GetNames](#string--getnamesbool-publicdbs)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Returns an array of strings with all of the database names found. 
| [GetSourceProfile](#sourceprofile-getsourceprofilestring-dbname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a SourceProfile from the Database name store.
| [InitializeMember](#void-initializememberstring-filepath-string-membername-int-recordcount)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a file member with the specified number of deleted records.
| [Open()](#void-open) | Open a connection to a Database.
| [PrepareNameStore\<T\>](#void-preparenamestore-t-namestoreoptions-options-string--configfiles)([NameStoreOptions](/reference/runtime/qsys-runtime/name-store-options.html), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Prepares the Database name store. Should be called only once and before any attempt to use a DataGated database by name.
| [RemoveDirectory](#void-removedirectorystring-directoryname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a directory (library) in the Database.
| [RemoveMember](#void-removememberstring-filepath-string-membername)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a member from the specified file.
| [RenameFile](#void-renamefilestring-filepath-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the name of a file in the Database.
| [RenameMember](#void-renamememberstring-filepath-string-membername-string-newname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the name of a member in a file.
| [Rollback()](#void-rollback) | Rollbacks, i.e. cancels, a transaction. 
| [SetDatabaseName](#void-setdatabasenamestring-databasename)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the Database name.
| [SetSourceProfile](#void-setsourceprofilesourceprofile-sourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Sets the Database name.
| [StartTpm](#void-starttpmint-level-string-name-string-options)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Starts transaction processing.

### void AddMember([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string memberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Add a member to a file.

```cs
void AddMember(string filePath, string memberName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to be added.

### void ClearMember([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string memberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Clear a file member.

```cs
void ClearMember(string filePath, string memberName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to clear.

### void Close()

Closes a connection to a Database.

```cs
void Close()
```

### void Commit([string boundary](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Commits an open transaction.

```cs
void Commit(string boundary)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | boundary | Transaction name to commit.

### void Connect()

Open a connection to a Database.

```cs
void Connect()
```

### void CopyFileToDb([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database toDb](/reference/runtime/qsys-runtime/database.html), [string toDirectory](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool copyData](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a file with all its members and data, if they exist, from the current Database to another Database.

```cs
void CopyFileToDb(string filePath, Database toDb, string toDirectory, bool copyData)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path of the file to be copied, as "library/fileName".
| [Database](/reference/runtime/qsys-runtime/database.html) | toDb | Database onto which the file will be copied.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDirectory | Destination directory.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | copyData | True to copy also the file data.

### void CopyLogicalFileToDb([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Database toDb](/reference/runtime/qsys-runtime/database.html), [string toDirectory](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool replaceBaseFiles](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool copyData](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a logical file and its base physical files from the current Database to another Database.

```cs
void CopyLogicalFileToDb(string filePath, Database toDb, string toDirectory, bool replaceBaseFiles, bool copyData)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path of the file to be copied, as "library/fileName".
| [Database](/reference/runtime/qsys-runtime/database.html) | toDb | Database onto which the file will be copied.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDirectory | Destination directory.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | replaceBaseFiles | If true, if a base file already exists in the target DB it will be replaced.            If false, if a base file already exists it will not be replaced.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | copyData | True to copy also the physical file data.

### void CreateDirectory([string directoryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Creates a new directory (library) in the Database.

```cs
void CreateDirectory(string directoryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directoryName | Name of the directory to be created.

### void DeleteFile([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Deletes a file from the Database.

```cs
void DeleteFile(string filePath)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".

### void Dispose([bool disposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases resources.

```cs
void Dispose(bool disposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | If True, it is safe to dispose of class members.

### void Dispose()

Releases resources.

```cs
void Dispose()
```

### void EndTpm()

Ends a Database transaction operation.

```cs
void EndTpm()
```

### String\[\] GetNames([bool publicDBs](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Returns an array of strings with all of the database names found. 

```cs
String[] GetNames(bool publicDBs)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | publicDBs |             A boolean parameter indicating whether to get Public Databases (true)             or those private to the current user (false).            

#### Returns

| Type | Description
| --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | 

### SourceProfile GetSourceProfile([string dbName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a SourceProfile from the Database name store.

```cs
SourceProfile GetSourceProfile(string dbName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dbName | Database name to search.

#### Returns

| Type | Description
| --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | The SourceProfile corresponding to the given dbName parameter.

### void InitializeMember([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string memberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int recordCount](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Initializes a file member with the specified number of deleted records.

```cs
void InitializeMember(string filePath, string memberName, int recordCount)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to initialize.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | recordCount | Number of deleted records to add to the member.

### void Open()

Open a connection to a Database.

```cs
void Open()
```

### void PrepareNameStore\<T\>([NameStoreOptions options](/reference/runtime/qsys-runtime/name-store-options.html), [String\[\] configFiles](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Prepares the Database name store. Should be called only once and before any attempt to use a DataGated database by name.

```cs
void PrepareNameStore<T>(NameStoreOptions options, String[] configFiles)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [NameStoreOptions](/reference/runtime/qsys-runtime/name-store-options.html) | options | Tells the name store where to look for database connection information, e.g. config files, user secrets, and others.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | configFiles | Optional collection of configuration files containing database connection information.

### void RemoveDirectory([string directoryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes a directory (library) in the Database.

```cs
void RemoveDirectory(string directoryName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directoryName | Name of the directory to remove.

### void RemoveMember([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string memberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes a member from the specified file.

```cs
void RemoveMember(string filePath, string memberName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to remove.

### void RenameFile([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Changes the name of a file in the Database.

```cs
void RenameFile(string filePath, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New file name.

### void RenameMember([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string memberName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string newName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Changes the name of a member in a file.

```cs
void RenameMember(string filePath, string memberName, string newName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Current member name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New member name.

### void Rollback()

Rollbacks, i.e. cancels, a transaction. 

```cs
void Rollback()
```

### void SetDatabaseName([string databaseName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Sets the Database name.

```cs
void SetDatabaseName(string databaseName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | databaseName | Database name. Use null for a blank source profile.

### void SetSourceProfile([SourceProfile sourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Sets the Database name.

```cs
void SetSourceProfile(SourceProfile sourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sourceProfile | The new source profile.

### void StartTpm([int level](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Starts transaction processing.

```cs
void StartTpm(int level, string name, string options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | level | Transaction level.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | Transaction name.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | options | Transaction options.
