---
title: Database Class
---

Handles connections to a Database.

**Namespace:** ASNA.QSys.Runtime <br/>
**Assembly:** ASNA.QSys.Runtime

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> Database

<br>
<br>

## Remarks

Handles connections to a Database.

[//]: # ($$TODO: Complete the Remarks section.)

<br>
<br>

## Constructors

| Name |  Description 
| --- | --- 
| [Database](#databasestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Constructs a Database object using a database name. 
| [Database](#databasestring-virtualterminal-openaccessdspf)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [VirtualTerminal](/reference/asna-qsys-runtime/virtual-terminal.html), [OpenAccessDspF](/reference/asna-qsys-runtime/open-access-dsp-f.html)) | Constructs a Database object using a database name, VirtualTerminal value, and OpenAccessDspF value. 

<br>

### Database( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) )

Constructs a Database object using a database name.

```cs
Database( String databaseName );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | databaseName | Database name. 

<br>

### Database( [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [VirtualTerminal](/reference/asna-qsys-runtime/virtual-terminal.html), [OpenAccessDspF](/reference/asna-qsys-runtime/open-access-dsp-f.html) )

Constructs a Database object using a database name, VirtualTerminal value, and OpenAccessDspF value.

```cs
Database( String databaseName, ASNA.QSys.Runtime.VirtualTerminal virtualTerminal, ASNA.QSys.Runtime.OpenAccessDspF openAccessDspF );
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | databaseName | Database name. 
| [VirtualTerminal](/reference/asna-qsys-runtime/virtual-terminal.html) | virtualTerminal | Value that specifies whether this connection will be used for an interactive virtual terminal connection. 
| [OpenAccessDspF](/reference/asna-qsys-runtime/open-access-dsp-f.html) | openAccessDspF | Value that specifies whether this connection is for use with Open Access RPG programs. 

<br>


<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [AdgConnection]($$TODO-ASNA.DataGate.Client.AdgConnection.html) | Connection | Gets the DataGate Connection instance. | 
| [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CurrentUserLibl | Sets the current library list for the current connection. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | DBName | Gets the Database Name. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | DefaultJobCodePageID | Gets or sets the Job's default Code Page ID. | 
| [dgException]($$TODO-ASNA.DataGate.Common.dgException.html) | InitialException | Gets the initial DataGate exception. | 
| [IEnumerable]($$TODO-Collections.Generic.IEnumerable.html) | InitialLibl | Gets or sets the current database initial library list. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsInteractive | Gets a boolean value indicating that the Database is associated with an Interactive Job. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsOpen | Returns a True or False indicating if the database is open. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Label | Gets or sets a string containing the label of the database to connect to. | 
| [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NameStoreConfigFiles | Gets the list of the database name store configuration files. | 
| [NameStoreOptions](/reference/asna-qsys-runtime/name-store-options.html) | NameStoreOptions | Gets the database name store options. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | NameStorePrepared | Gets whether the database name store has already been set for the process. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Password | Sets the password to be used in conjunction with User for connection authentication. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PlatformAttribute | Gets or sets a platform-specific attribute of the database engine. | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | PoolingTimeout | Gets or sets the database PoolingTimeOut (in minutes). | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | Port | Gets or sets the TCP port number used by the database server for TCP/IP-based transport (default 5042). | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Server | The database server host machine name. | 
| [ServerSupport](/reference/asna-qsys-runtime/server-support.html) | ServerSupport | For interactive connections, determines if program can issue server requests like open file or call program. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | SslCertificateName | Gets or sets the SSL Certificate name for the database connection. | 
| [SslOptions]($$TODO-ASNA.DataGate.Common.SslOptions.html) | SslOptions | Gets or sets the SLL Options for the database connection. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | TerminalDeviceName | For interactive connections, determines the name of the device. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Text | Gets or sets a description of the database connection. | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | User | Gets or sets the user name that used to authorize the current database connection. | 
| [VirtualTerminal](/reference/asna-qsys-runtime/virtual-terminal.html) | VirtualTerminal | VirtualTerminal summary. | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [AddMember](#addmemberstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Add a member to a file. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [ClearMember](#clearmemberstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Clear a file member. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Close](#close)() | Closes a connection to a Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Close](#closechar)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Closes a connection to a Database, trapping errors and returning an error condition. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Commit](#commitstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Commits an open transaction. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Commit](#commitstring-char)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Commits an open transaction, trapping errors and returning an error condition. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Connect](#connect)() | Open a connection to a Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [CopyFileToDb](#copyfiletodbstring-database-string-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/asna-qsys-runtime/classes/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a file with all its members and data, if they exist, from the current Database to another Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [CopyLogicalFileToDb](#copylogicalfiletodbstring-database-string-boolean-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/asna-qsys-runtime/classes/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Copies a logical file and its base physical files from the current Database to another Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [CreateDirectory](#createdirectorystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new directory (library) in the Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [DeleteFile](#deletefilestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Deletes a file from the Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Dispose](#disposeboolean)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases resources. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Dispose](#dispose)() | Releases resources. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [EndTpm](#endtpm)() | Ends a Database transaction operation. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [EndTpm](#endtpmchar)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Ends a Database transaction operation. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [GetNames](#getnamesboolean)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Returns an array of strings with all of the database names found. | 
| [SourceProfile]($$TODO-ASNA.DataGate.Providers.SourceProfile.html) | [GetSourceProfile](#getsourceprofilestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a SourceProfile from the Database name store. | The SourceProfile corresponding to the given dbName parameter.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [InitializeMember](#initializememberstring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a file member with the specified number of deleted records. | 
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Open](#open)() | Open a connection to a Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Open](#openindicator)([Indicator](/reference/asna-qsys-runtime/classes/indicator.html)) | Open a connection to a Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Open](#openchar)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Open a connection to a Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [PrepareNameStore\\`\\`1](#preparenamestore\`\`1namestoreoptions-string[])([NameStoreOptions](/reference/asna-qsys-runtime/name-store-options.html), [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Prepares the Database name store. Should be called anly once and before any attempt to use a DataGated database by name. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [RemoveDirectory](#removedirectorystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a directory (library) in the Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [RemoveMember](#removememberstring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes a member from the specified file. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [RenameFile](#renamefilestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the name of a file in the Database. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [RenameMember](#renamememberstring-string-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the name of a member in a file. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Rollback](#rollback)() | Rollbacks, i.e. cancels, a transaction. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Rollback](#rollbackchar)([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Rollbacks, i.e. cancels, a transaction. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SetDatabaseName](#setdatabasenamestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the Database name. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [SetSourceProfile](#setsourceprofilesourceprofile)([SourceProfile]($$TODO-ASNA.DataGate.Providers.SourceProfile.html)) | Sets the Database name. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [StartTpm](#starttpmint32-string-string)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Starts transaction processing. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [StartTpm](#starttpmint32-string-string-char)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Starts transaction processing. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.

<br>
<br>

### AddMember([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Add a member to a file.

```cs
AddMember(String filePath, String memberName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to be added. 


<br>
<br>

### ClearMember([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Clear a file member.

```cs
ClearMember(String filePath, String memberName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to clear. 


<br>
<br>

### Close()

Closes a connection to a Database.

```cs
Close();
```


<br>
<br>

### Close([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Closes a connection to a Database, trapping errors and returning an error condition.

```cs
Close(ref Char err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | err | Out parameter that contains '1' if the Close operation causes an exception; '0' otherwise. 


<br>
<br>

### Commit([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Commits an open transaction.

```cs
Commit(String boundary);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | boundary | Transaction name to commit. 


<br>
<br>

### Commit([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Commits an open transaction, trapping errors and returning an error condition.

```cs
Commit(String boundary, ref Char err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | boundary | Transaction name to commit. 
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | err | Out parameter that contains '1' if the Commit operation causes an exception; '0' otherwise. 


<br>
<br>

### Connect()

Open a connection to a Database.

```cs
Connect();
```


<br>
<br>

### CopyFileToDb([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/asna-qsys-runtime/classes/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a file with all its members and data, if they exist, from the current Database to another Database.

```cs
CopyFileToDb(String filePath, ASNA.QSys.Runtime.Database toDb, String toDirectory, Boolean copyData);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path of the file to be copied, as "library/fileName". 
| [Database](/reference/asna-qsys-runtime/classes/database.html) | toDb | Database onto which the file will be copied. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDirectory | Destination directory. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | copyData | True to copy also the file data. 


<br>
<br>

### CopyLogicalFileToDb([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Database](/reference/asna-qsys-runtime/classes/database.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Copies a logical file and its base physical files from the current Database to another Database.

```cs
CopyLogicalFileToDb(String filePath, ASNA.QSys.Runtime.Database toDb, String toDirectory, Boolean replaceBaseFiles, Boolean copyData);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path of the file to be copied, as "library/fileName". 
| [Database](/reference/asna-qsys-runtime/classes/database.html) | toDb | Database onto which the file will be copied. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | toDirectory | Destination directory. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | replaceBaseFiles | If true, if a base file already exists in the target DB it will be replaced.
            If false, if a base file already exists it will not be replaced. 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | copyData | True to copy also the physical file data. 


<br>
<br>

### CreateDirectory([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Creates a new directory (library) in the Database.

```cs
CreateDirectory(String directoryName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directoryName | Name of the directory to be created. 


<br>
<br>

### DeleteFile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Deletes a file from the Database.

```cs
DeleteFile(String filePath);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 


<br>
<br>

### Dispose([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases resources.

```cs
Dispose(Boolean disposing);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | If True, it is safe to dispose of class members. 


<br>
<br>

### Dispose()

Releases resources.

```cs
Dispose();
```


<br>
<br>

### EndTpm()

Ends a Database transaction operation.

```cs
EndTpm();
```


<br>
<br>

### EndTpm([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Ends a Database transaction operation.

```cs
EndTpm(ref Char err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | err | Out parameter that contains '1' if the EndTpm operation causes an exception; '0' otherwise. 


<br>
<br>

### GetNames([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Returns an array of strings with all of the database names found.

```cs
GetNames(Boolean publicDBs);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | publicDBs | 
            A boolean parameter indicating whether to get Public Databases (true) 
            or those private to the current user (false).
             

#### Returns

[String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string)




<br>
<br>

### GetSourceProfile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets a SourceProfile from the Database name store.

```cs
GetSourceProfile(String dbName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dbName | Database name to search. 

#### Returns

[SourceProfile]($$TODO-ASNA.DataGate.Providers.SourceProfile.html)

The SourceProfile corresponding to the given dbName parameter.


<br>
<br>

### InitializeMember([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a file member with the specified number of deleted records.

```cs
InitializeMember(String filePath, String memberName, Int32 recordCount);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to initialize. 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | recordCount | Number of deleted records to add to the member. 


<br>
<br>

### Open()

Open a connection to a Database.

```cs
Open();
```


<br>
<br>

### Open([Indicator](/reference/asna-qsys-runtime/classes/indicator.html))

Open a connection to a Database.

```cs
Open(ref ASNA.QSys.Runtime.Indicator err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Indicator](/reference/asna-qsys-runtime/classes/indicator.html) | err | Out parameter that contains '1' if the Open operation causes an exception; '0' otherwise. 


<br>
<br>

### Open([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Open a connection to a Database.

```cs
Open(ref Char err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | err | Out parameter that contains '1' if the Open operation causes an exception; '0' otherwise. 


<br>
<br>

### PrepareNameStore\`\`1([NameStoreOptions](/reference/asna-qsys-runtime/name-store-options.html), [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Prepares the Database name store. Should be called anly once and before any attempt to use a DataGated database by name.

```cs
PrepareNameStore``1(ASNA.QSys.Runtime.NameStoreOptions options, String[] configFiles);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [NameStoreOptions](/reference/asna-qsys-runtime/name-store-options.html) | options | Tells the name store where to look for database connection information, e.g. config files, user secrets, and others. 
| [String[]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | configFiles | Optional collection of configuration files containing database connection information. 


<br>
<br>

### RemoveDirectory([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Removes a directory (library) in the Database.

```cs
RemoveDirectory(String directoryName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | directoryName | Name of the directory to remove. 


<br>
<br>

### RemoveMember([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Removes a member from the specified file.

```cs
RemoveMember(String filePath, String memberName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Name of the member to remove. 


<br>
<br>

### RenameFile([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Changes the name of a file in the Database.

```cs
RenameFile(String filePath, String newName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New file name. 


<br>
<br>

### RenameMember([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Changes the name of a member in a file.

```cs
RenameMember(String filePath, String memberName, String newName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file as "library/fileName". 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | Current member name. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newName | New member name. 


<br>
<br>

### Rollback()

Rollbacks, i.e. cancels, a transaction.

```cs
Rollback();
```


<br>
<br>

### Rollback([Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Rollbacks, i.e. cancels, a transaction.

```cs
Rollback(ref Char err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | err | Out parameter that contains '1' if the Rollback operation causes an exception; '0' otherwise. 


<br>
<br>

### SetDatabaseName([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Sets the Database name.

```cs
SetDatabaseName(String databaseName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | databaseName | Database name. Use null for a blank source profile. 


<br>
<br>

### SetSourceProfile([SourceProfile]($$TODO-ASNA.DataGate.Providers.SourceProfile.html))

Sets the Database name.

```cs
SetSourceProfile(ASNA.DataGate.Providers.SourceProfile sourceProfile);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile]($$TODO-ASNA.DataGate.Providers.SourceProfile.html) | sourceProfile | The new source profile. 


<br>
<br>

### StartTpm([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Starts transaction processing.

```cs
StartTpm(Int32 level, String name, String options);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | level | Transaction level. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | Transaction name. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | options | Transaction options. 


<br>
<br>

### StartTpm([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Starts transaction processing.

```cs
StartTpm(Int32 level, String name, String options, ref Char err);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | level | Transaction level. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | Transaction name. 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | options | Transaction options. 
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | err | Out parameter that contains '1' if the StartTpm operation causes an exception; '0' otherwise. 


<br>
<br>

