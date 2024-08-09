---
title: "DatabaseFileBase class        | QSYS API Reference Guide"
description: "Common base class for Database data files, single format and multiformat. It contains methods common to both kinds. "
last_modified_at: 2024-08-09T16:18:25Z
---

Common base class for Database data files, single format and multiformat. It contains methods common to both kinds.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [FileBase](/reference/runtime/qsys-runtime/file-base.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [DatabaseFileBase](#databasefilebasestring-string-string-int32-string-boolean-int32-string-string-string-boolean-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the DatabaseFileBase class.
| [DatabaseFileBase](#databasefilebasestring-string-string-int32-string-boolean-int32-string-string-string-boolean-boolean-action)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0)) | Initializes a new instance of the DatabaseFileBase class.
| [DatabaseFileBase](#databasefilebasestring-string-string-int32-sharetypes-boolean-int32-string-string-string-boolean-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the DatabaseFileBase class.
| [DatabaseFileBase](#databasefilebasestring-string-string-int32-sharetypes-boolean-int32-string-string-string-boolean-boolean-action)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0)) | Initializes a new instance of the DatabaseFileBase class.

### DatabaseFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the DatabaseFileBase class.

```cs
DatabaseFileBase(String, String, String, Int32, String, Boolean, Int32, String, String, String, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclDiskFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | The name of the file member. Default is "*FIRST".
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | blockingFactor |  An integer that determines if and optionally how many database records             will be blocked across the Network for better performance when reading or writing groups of records. Pass -1 for no blocking.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareType | String value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | waitRec | An integer specifying the waiting period for a record.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qrySelect | Simple query select statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryKeyFlds | Simple query search keys statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryFileName | Simple query file name. Default is "*NAME".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultRFN | True to use the default renamed format.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isKeyed | True if the file has a key.

### DatabaseFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0))

Initializes a new instance of the DatabaseFileBase class.

```cs
DatabaseFileBase(String, String, String, Int32, String, Boolean, Int32, String, String, String, Boolean, Boolean, Action)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclDiskFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | The name of the file member. Default is "*FIRST".
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | blockingFactor |  An integer that determines if and optionally how many database records             will be blocked across the Network for better performance when reading or writing groups of records. Default is -1, which means no blocking.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareType | String value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID..
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | waitRec | An integer specifying the waiting period for a record.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qrySelect | Simple query select statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryKeyFlds | Simple query search keys statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryFileName | Simple query file name. Default is "*NAME".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultRFN | DatabaseFileBase isDefaultRFN param.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isKeyed | DatabaseFileBase isKeyed param.
| [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0) | infSR | DatabaseFileBase infSR param.

### DatabaseFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the DatabaseFileBase class.

```cs
DatabaseFileBase(String, String, String, Int32, ShareTypes, Boolean, Int32, String, String, String, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclDiskFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | The name of the file member. Default is "*FIRST".
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | blockingFactor |  An integer that determines if and optionally how many database records             will be blocked across the Network for better performance when reading or writing groups of records. Pass -1 for no blocking.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | ShareTypes value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID..
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | waitRec | An integer specifying the waiting period for a record.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qrySelect | Simple query select statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryKeyFlds | Simple query search keys statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryFileName | Simple query file name. Default is "*NAME".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultRFN | True to use the default renamed format.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isKeyed | True if the file has a key.

### DatabaseFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0))

Initializes a new instance of the DatabaseFileBase class.

```cs
DatabaseFileBase(String, String, String, Int32, ShareTypes, Boolean, Int32, String, String, String, Boolean, Boolean, Action)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclDiskFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | memberName | The name of the file member. Default is "*FIRST".
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | blockingFactor |  An integer that determines if and optionally how many database records             will be blocked across the Network for better performance when reading or writing groups of records. Default is -1, which means no blocking.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | ShareTypes value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID..
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | waitRec | An integer specifying the waiting period for a record.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qrySelect | Simple query select statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryKeyFlds | Simple query search keys statement. Default is "*NONE".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | qryFileName | Simple query file name. Default is "*NAME".
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDefaultRFN | DatabaseFileBase isDefaultRFN param.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isKeyed | DatabaseFileBase isKeyed param.
| [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0) | infSR | DatabaseFileBase infSR param.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | BlockingFactor | Gets or sets the integer that determines if and optionally how many database records will be blocked across the Network for better performance when reading or writing groups of records. Network blocking significantly reduces the network burden of transferring records between server and client machines, and this is demonstrated by the substantial increase of data throughput. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | CheckFormatID | Gets or sets the value that specifies if the Format IDs of the file should be checked when the file is opened. |
| [FileAdapter](/reference/datagate/datagate-client/file-adapter.html) | fileAdapter | fileAdapter summary. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FilePath | Gets or sets the path to the file in the Database, given as "library/filename". |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormatName | Gets the name of the record format. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InhibitWrites | Prevents operations to the file from actually updating it, effectively treating the operation as a no-op. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsDefaultRFN | Gets or sets the value that specifies if the "default" renamed format is going to be used. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsFormatID | Obsolete. Use CheckFormatID. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsKeyed | Gets the value that specifies if the file has been opened for "keyed" access. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LibraryName | Gets the library name for an open fileAdapter. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | MemberName | Gets or sets the name of the file member. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QryFileName | Gets or sets the string that specifies the name of the query file created for the QrySelect and QryKeyFlds parameters. If *Name is specified, which is the default, the file name given on the DCLDISKFILE command is used. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QryKeyFlds | Gets or sets the string used to specify the name of one or more key fields used to arrange the query records. Each key field is composed of a field name followed by optional attributes that determine the sorting order (ascending descending, or absolute value for numeric fields). |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | QrySelect | Gets or sets the string specifying the selection expression used to determine which records are to be made available for processing. The select expression syntax is the same as for a Select/Omit expression in Acceler8DB.  |
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | queryKeys | Gets or sets the list of keys for building queries. |
| [List\<KeyUsages\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | queryUsages | Gets or sets the list of key usages for queries. |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecCount | Gets the current number of records in the file.  |
| [Int64](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | RecNum | Gets the current RRN for input operations made to a database file opened with type of access as Input or Update. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ShareOpenDataPath | Gets or sets the value that specifies if the file can be shared with other programs. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ShareType | Gets or sets the string defining how a file will be shared.  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StarFile | Integer value of the *FILE constant.  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WaitRec | Gets or sets the integer specifying the waiting period for a record. |

## Methods

| Signature | Description |
| --- | --- |
| [chainKey](#void-chainkeystring-formatname-adgkeytable-key-bool-nolock)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read a record format using a key.
| [chainKey](#void-chainkeystring-formatname-adgkeytable-key-bool-nolock-ids-intods)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record format using a key.
| [chainRRN](#void-chainrrnstring-formatname-int-rrn-bool-nolock)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read a record format using the relative record number.
| [chainRRN](#void-chainrrnstring-formatname-int-rrn-bool-nolock-ids-intods)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record format using the relative record number.
| [CheckKey](#bool-checkkeystring-formatname-adgkeytable-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Check whether a record exists.
| [close()](#void-close) | Close the database file.
| [DeleteByKey](#void-deletebykeystring-formatname-adgkeytable-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html)) | Delete a record.
| [deleteByRRN](#void-deletebyrrnstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Delete a record using its relative record number.
| [DeleteCurrent](#void-deletecurrentstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete the current record.
| [DeleteRange](#void-deleterangestring-formatname-adgkeytable-firstkey-adgkeytable-lastkey-bool-includefirstkey-int-includelastkey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Delete a range of records.
| [Feod](#void-feodstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Force end of data on the given record.
| [GetAlternateKeyTable](#adgkeytable-getalternatekeytablestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | For multiformat files, get the alternate AdgKeyTable for a given record format.
| [GetKeyTable](#adgkeytable-getkeytablestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | For multiformat files, get the AdgKeyTable for a given record format.
| [open](#void-opendatabase-database-accessmode-accessmode-bool-iscachewrite-bool-iscommit-servercursors-servercursor)([Database](/reference/runtime/qsys-runtime/database.html), [AccessMode](/reference/datagate/datagate-common/access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ServerCursors](/reference/datagate/datagate-common/server-cursors.html)) | Open the database file.
| [Open](#void-opendatabase-database-accessmode-accessmode-bool-iscachewrite-bool-iscommit-servercursors-servercursor)([Database](/reference/runtime/qsys-runtime/database.html), [AccessMode](/reference/datagate/datagate-common/access-mode.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ServerCursors](/reference/datagate/datagate-common/server-cursors.html)) | Open the database file.
| [ReadEqualIncompleteKey](#void-readequalincompletekeystring-formatname-adgkeytable-key-string-incompletekeybuffer-bool-nolock-bool-previous)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read sequentially a record with an incomplete key buffer.
| [ReadEqualIncompleteKey](#void-readequalincompletekeystring-formatname-adgkeytable-key-string-incompletekeybuffer-bool-nolock-bool-previous-ids-intods)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read sequentially a record with an incomplete key buffer.
| [ReadEqualKey](#void-readequalkeystring-formatname-adgkeytable-key-bool-nolock-bool-previous)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read the adjacent record sequentially, if it has the same key.
| [ReadEqualKey](#void-readequalkeystring-formatname-adgkeytable-key-bool-nolock-bool-previous-ids-intods)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read the adjacent record sequentially, if it has the same key.
| [ReadRange](#void-readrangestring-formatname-adgkeytable-firstkey-adgkeytable-lastkey-bool-startat-bool-includefirstkey-int-includelastkey-bool-nolock)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read a range of records.
| [ReadSeq](#void-readseqstring-formatname-bool-nolock-bool-previous)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read the next record sequentially.
| [ReadSeq](#void-readseqstring-formatname-bool-nolock-bool-previous-ids-intods)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read the next record sequentially.
| [Seek](#void-seekstring-formatname-adgkeytable-key-int-readmode)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Seek to a particular record. Position the cursor according to the readMode parameter.
| [SeekRRN](#void-seekrrnstring-formatname-int-rrn-int-readmode)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Seek to a particular record using its relative record number. Position the cursor according to the readMode parameter.
| [SetRange](#void-setrangestring-formatname-adgkeytable-firstkey-adgkeytable-lastkey-bool-startat-bool-includefirstkey-int-includelastkey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Seek a range of records.
| [Unlock()](#void-unlock) | Unlock a record.
| [update](#void-updatestring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Update a record.
| [update](#void-updatestring-formatname-char--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Update a record.
| [Update](#void-updatestring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Update a record.
| [Update](#void-updatestring-formatname-indicator--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Update a record.
| [updateFlds](#void-updatefldsstring-formatname-string--fieldnames)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Update a record, only those fields listed in fieldNames.
| [write](#void-writestring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Write a record.
| [write](#void-writestring-formatname-char--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Write a record.
| [Write](#void-writestring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Write a record.
| [Write](#void-writestring-formatname-indicator--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Write a record.

### void chainKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read a record format using a key.

```cs
void chainKey(string formatName, AdgKeyTable key, bool noLock)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.

### void chainKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read a record format using a key.

```cs
void chainKey(string formatName, AdgKeyTable key, bool noLock, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

### void chainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read a record format using the relative record number.

```cs
void chainRRN(string formatName, int rrn, bool noLock)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.

### void chainRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read a record format using the relative record number.

```cs
void chainRRN(string formatName, int rrn, bool noLock, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

### bool CheckKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html))

Check whether a record exists.

```cs
bool CheckKey(string formatName, AdgKeyTable key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to check.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record exists.

### void close()

Close the database file.

```cs
void close()
```

### void DeleteByKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html))

Delete a record.

```cs
void DeleteByKey(string formatName, AdgKeyTable key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.

### void deleteByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Delete a record using its relative record number.

```cs
void deleteByRRN(string formatName, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.

### void DeleteCurrent([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete the current record.

```cs
void DeleteCurrent(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.

### void DeleteRange([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable firstKey](/reference/datagate/datagate-client/adg-key-table.html), [AdgKeyTable lastKey](/reference/datagate/datagate-client/adg-key-table.html), [bool includeFirstKey](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int includeLastKey](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Delete a range of records.

```cs
void DeleteRange(string formatName, AdgKeyTable firstKey, AdgKeyTable lastKey, bool includeFirstKey, int includeLastKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | Key of the first record in the range.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | Key of the last record in the range.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | includeFirstKey | True to include the first record in the delete operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | includeLastKey | 0 to include, 1 to exclude, 2 to use the same option as the one for the first record.

### void Feod([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Force end of data on the given record.

```cs
void Feod(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.

### AdgKeyTable GetAlternateKeyTable([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

For multiformat files, get the alternate AdgKeyTable for a given record format.

```cs
AdgKeyTable GetAlternateKeyTable(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.

#### Returns

| Type | Description
| --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | The alternate AdgKeyTable for the record format.

### AdgKeyTable GetKeyTable([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

For multiformat files, get the AdgKeyTable for a given record format.

```cs
AdgKeyTable GetKeyTable(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.

#### Returns

| Type | Description
| --- | ---
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | The AdgKeyTable for the record format.

### void open([Database database](/reference/runtime/qsys-runtime/database.html), [AccessMode accessMode](/reference/datagate/datagate-common/access-mode.html), [bool isCacheWrite](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool isCommit](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ServerCursors serverCursor](/reference/datagate/datagate-common/server-cursors.html))

Open the database file.

```cs
void open(Database database, AccessMode accessMode, bool isCacheWrite, bool isCommit, ServerCursors serverCursor)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Database](/reference/runtime/qsys-runtime/database.html) | database | Database where the file is located.
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | accessMode | AccessMode of the file.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isCacheWrite | True to enable cache writes.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isCommit | True to have file operations under commitment control.
| [ServerCursors](/reference/datagate/datagate-common/server-cursors.html) | serverCursor | ServerCursors option value.

### void Open([Database database](/reference/runtime/qsys-runtime/database.html), [AccessMode accessMode](/reference/datagate/datagate-common/access-mode.html), [bool isCacheWrite](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool isCommit](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [ServerCursors serverCursor](/reference/datagate/datagate-common/server-cursors.html))

Open the database file.

```cs
void Open(Database database, AccessMode accessMode, bool isCacheWrite, bool isCommit, ServerCursors serverCursor)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Database](/reference/runtime/qsys-runtime/database.html) | database | Database where the file is located.
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | accessMode | AccessMode of the file.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isCacheWrite | True to enable cache writes.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isCommit | True to have file operations under commitment control.
| [ServerCursors](/reference/datagate/datagate-common/server-cursors.html) | serverCursor | ServerCursors option value.

### void ReadEqualIncompleteKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [string incompleteKeyBuffer](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool previous](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read sequentially a record with an incomplete key buffer.

```cs
void ReadEqualIncompleteKey(string formatName, AdgKeyTable key, string incompleteKeyBuffer, bool noLock, bool previous)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | incompleteKeyBuffer | Incomplete key buffer.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | previous | True to read the previous record. False to read the next.

### void ReadEqualIncompleteKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [string incompleteKeyBuffer](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool previous](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read sequentially a record with an incomplete key buffer.

```cs
void ReadEqualIncompleteKey(string formatName, AdgKeyTable key, string incompleteKeyBuffer, bool noLock, bool previous, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | incompleteKeyBuffer | Incomplete key buffer.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | previous | True to read the previous record. False to read the next.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

### void ReadEqualKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool previous](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read the adjacent record sequentially, if it has the same key.

```cs
void ReadEqualKey(string formatName, AdgKeyTable key, bool noLock, bool previous)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | previous | True to read the previous record. False to read the next.

### void ReadEqualKey([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool previous](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read the adjacent record sequentially, if it has the same key.

```cs
void ReadEqualKey(string formatName, AdgKeyTable key, bool noLock, bool previous, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | previous | True to read the previous record. False to read the next.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

### void ReadRange([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable firstKey](/reference/datagate/datagate-client/adg-key-table.html), [AdgKeyTable lastKey](/reference/datagate/datagate-client/adg-key-table.html), [bool startAt](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool includeFirstKey](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int includeLastKey](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read a range of records.

```cs
void ReadRange(string formatName, AdgKeyTable firstKey, AdgKeyTable lastKey, bool startAt, bool includeFirstKey, int includeLastKey, bool noLock)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | Key of the first record in the range.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | Key of the last record in the range.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | startAt | True to use RangeMode.Last.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | includeFirstKey | True to include the first record in the delete operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | includeLastKey | 0 to include, 1 to exclude, 2 to use the same option as the one for the first record.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.

### void ReadSeq([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool previous](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read the next record sequentially.

```cs
void ReadSeq(string formatName, bool noLock, bool previous)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | previous | True to read the previous record. False to read the next.

### void ReadSeq([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool noLock](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool previous](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read the next record sequentially.

```cs
void ReadSeq(string formatName, bool noLock, bool previous, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | noLock | True to leave the record unlocked after the operation.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | previous | True to read the previous record. False to read the next.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

### void Seek([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable key](/reference/datagate/datagate-client/adg-key-table.html), [int readMode](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Seek to a particular record. Position the cursor according to the readMode parameter.

```cs
void Seek(string formatName, AdgKeyTable key, int readMode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | key | An AdgKeyTable object containing the key of the record to seek.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | readMode | The SeekMode integer value indicating where the cursor will be in relation to the record.

### void SeekRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int readMode](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Seek to a particular record using its relative record number. Position the cursor according to the readMode parameter.

```cs
void SeekRRN(string formatName, int rrn, int readMode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to seek.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | readMode | The SeekMode integer value indicating where the cursor will be in relation to the record.

### void SetRange([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [AdgKeyTable firstKey](/reference/datagate/datagate-client/adg-key-table.html), [AdgKeyTable lastKey](/reference/datagate/datagate-client/adg-key-table.html), [bool startAt](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [bool includeFirstKey](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int includeLastKey](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Seek a range of records.

```cs
void SetRange(string formatName, AdgKeyTable firstKey, AdgKeyTable lastKey, bool startAt, bool includeFirstKey, int includeLastKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | Key of the first record in the range.
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | Key of the last record in the range.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | startAt | True to use RangeMode.Last.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | includeFirstKey | True to include the first record in the delete operation.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | includeLastKey | 0 to include, 1 to exclude, 2 to use the same option as the one for the first record.

### void Unlock()

Unlock a record.

```cs
void Unlock()
```

### void update([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Update a record.

```cs
void update(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to update.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the update operation.

### void update([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char), [IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Update a record.

```cs
void update(string formatName, Char[] optionIndicators, IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to update.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the update operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | IDS object where the data comes from.

### void Update([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Update a record.

```cs
void Update(string formatName, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to update.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the update operation.

### void Update([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html), [IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Update a record.

```cs
void Update(string formatName, Indicator[] optionIndicators, IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to update.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the update operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | IDS object where the data comes from.

### void updateFlds([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] fieldNames](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Update a record, only those fields listed in fieldNames.

```cs
void updateFlds(string formatName, String[] fieldNames)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to update.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldNames | Array of field names to update.

### void write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Write a record.

```cs
void write(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the write operation.

### void write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char), [IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Write a record.

```cs
void write(string formatName, Char[] optionIndicators, IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the write operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | IDS object where the data comes from.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Write a record.

```cs
void Write(string formatName, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the write operation.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html), [IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Write a record.

```cs
void Write(string formatName, Indicator[] optionIndicators, IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the write operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | IDS object where the data comes from.
