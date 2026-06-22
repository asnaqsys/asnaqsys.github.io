---
title: "FileOpenAttr class"
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
| [FileOpenAttr()](file-open-attr-ctor.html#fileopenattr) | Initializes a new instance of the FileOpenAttr class.

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
| [Add](file-open-attr-add.html#void-add-string-key-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Adds an element with the provided key and value to the FileOpenAttr.
| [ContainsKey](file-open-attr-containskey.html#bool-containskey-string-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Determines whether the FileOpenAttr contains an element with the specified key.
| [Remove](file-open-attr-remove.html#bool-remove-string-key)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Removes the element with the specified key from the FileOpenAttr.
| [TryGetValue](file-open-attr-trygetvalue.html#bool-trygetvalue-string-key-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object&](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Gets the value associated with the specified key.

