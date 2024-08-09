---
title: "FileOpenAttr class            | QSYS API Reference Guide"
description: "Represents the attributes for opening a file. "
last_modified_at: 2024-08-09T17:25:07Z
---

Represents the attributes for opening a file.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.



## Constructors

| Name | Description |
| --- | --- |
| [FileOpenAttr()](#fileopenattr) | Initializes a new instance of the FileOpenAttr class.

### FileOpenAttr()

Initializes a new instance of the FileOpenAttr class.

```cs
FileOpenAttr()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | BlockingFactor | Gets or sets the blocking factor for the file to be opened. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | BulkCopyTimeout | The number of seconds to wait for a SQL bulk copy operation tocomplete.  If this quantum elapses prior to completion, the SQLprovider may throw an exception.  The default value is provider-defined.  The provider may define special values as well.For example, this property directly corresponds to theBulkCopyTimeout property of System.Data.SqlClient.SqlBulkCopy,which has a default value of 30 seconds.  A value of zero disablesthe timeout function, and the operation waits indefinitely forcompletion. |
| [FileLocks](/reference/datagate/datagate-common/file-locks.html) | FileLocks | Gets or sets the file locks for the file to be opened. |
| [Byte\[\]\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.byte) | FormatIDs | Gets or sets the format IDs for the file to be opened. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InhibitWrite | Gets or sets a value indicating whether writing to the file to be opened is inhibited. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Item | Gets or sets the value associated with the specified key. |
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | Item | Gets or sets the value associated with the specified key. |
| [ServerCursors](/reference/datagate/datagate-common/server-cursors.html) | ServerCursor | Gets or sets a value indicating whether a server cursor is used for the file to be opened. |
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | ShareTypes | Gets or sets the share types for the file to be opened. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WaitForEOF | Gets or sets the number of seconds to wait for the end of file (EOF) to be reached. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WaitForFile | Gets or sets the number of seconds to wait for the file to be opened. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | WaitForRecord | Gets or sets the number of seconds to wait for the record to be opened. |

## Methods

| Signature | Description |
| --- | --- |
| [Add](#void-addstring-key-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds an element with the provided key and value to the FileOpenAttr.
| [ContainsKey](#bool-containskeystring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the FileOpenAttr contains an element with the specified key.
| [Remove](#bool-removestring-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes the element with the specified key from the FileOpenAttr.
| [TryGetValue](#bool-trygetvaluestring-key-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object&](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the value associated with the specified key.

### void Add([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Adds an element with the provided key and value to the FileOpenAttr.

```cs
void Add(string key, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | The object to use as the key of the element to add.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | The object to use as the value of the element to add.

### bool ContainsKey([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Determines whether the FileOpenAttr contains an element with the specified key.

```cs
bool ContainsKey(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | The key to locate in the FileOpenAttr.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the FileOpenAttr contains an element with the key; otherwise, false.

### bool Remove([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Removes the element with the specified key from the FileOpenAttr.

```cs
bool Remove(string key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | The key of the element to remove.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the element is successfully found and removed; otherwise, false.

### bool TryGetValue([string key](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object& value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Gets the value associated with the specified key.

```cs
bool TryGetValue(string key, Object& value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | The key of the value to get.
| [Object&](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | When this method returns, contains the value associated with the specified key, if the key is found; otherwise, the default value for the type of the value parameter.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the FileOpenAttr contains an element with the specified key; otherwise, false.
