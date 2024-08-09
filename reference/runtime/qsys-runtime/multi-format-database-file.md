---
title: "MultiFormatDatabaseFile class | QSYS API Reference Guide"
description: "Represents a multiformat Database data file. It contains methods to handle all Input and Output operations on the file.  "
last_modified_at: 2024-08-09T16:18:25Z
---

Represents a multiformat Database data file. It contains methods to handle all Input and Output operations on the file. 

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [FileBase](/reference/runtime/qsys-runtime/file-base.html) --> [DatabaseFileBase](/reference/runtime/qsys-runtime/database-file-base.html)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Dictionary\<String, AdgKeyTable\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | Keys | Gets the dictionary relating the format name to its key table. These are the main key tables for random access. |
| [Dictionary\<String, AdgKeyTable\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | Kezs | Gets the secondary dictionary relating the format name to its key table. These are the 'to' key tables for operations that require from/to keys. |

## Methods

| Signature | Description |
| --- | --- |
| [allocateBuffer()](#adgdataset-allocatebuffer) | Allocates a DataSet Buffer.
| [Chain](#bool-chainstring-formatname-bool-lockrecord-object--keyparts)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read a record format using a key.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-bool-lockrecord-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Read a record format using the relative record number.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-bool-lockrecord-decimal-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Read a record format using the relative record number.
| [Delete](#bool-deletestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Delete the current record.
| [Delete](#bool-deletestring-formatname-object--keyparts)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Delete the current record.
| [DeleteByRRN](#bool-deletebyrrnstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Delete a record using its relative record number.
| [DeleteByRRN](#bool-deletebyrrnstring-formatname-decimal-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Delete a record using its relative record number.
| [DeleteRange](#bool-deleterangestring-formatname-object--firstkey-object--lastkey-rangefirst-rangefirstkey-rangelast-rangelastkey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Delete a range of records.
| [ReadNext](#bool-readnextstring-formatname-bool-lockrecord)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read the next record sequentially.
| [ReadNextEqual](#bool-readnextequalstring-formatname-bool-lockrecord-object--keyparts)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the next record sequentially, if it has the same key.
| [ReadPrevious](#bool-readpreviousstring-formatname-bool-lockrecord)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read the previous record sequentially.
| [ReadPreviousEqual](#bool-readpreviousequalstring-formatname-bool-lockrecord-object--keyparts)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the previous record sequentially, if it has the same key.
| [ReadRange](#bool-readrangestring-formatname-object--firstkey-object--lastkey-rangemode-mode-rangefirst-rangefirstkey-rangelast-rangelastkey-bool-lockrecord)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [RangeLast](/reference/datagate/datagate-common/range-last.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read a range of records.
| [Seek](#bool-seekstring-formatname-seekmode-mode-object--keyparts)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [SeekMode](/reference/datagate/datagate-common/seek-mode.html), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Positions the file cursor in the record indicated by key.
| [SeekByRRN](#bool-seekbyrrnstring-formatname-seekmode-mode-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [SeekMode](/reference/datagate/datagate-common/seek-mode.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Positions the file cursor in the record indicated by relative record number.
| [SetRange](#void-setrangestring-formatname-object--firstkey-object--lastkey-rangemode-mode-rangefirst-rangefirstkey-rangelast-rangelastkey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Sets the range of records for input operations.

### AdgDataSet allocateBuffer()

Allocates a DataSet Buffer.

```cs
AdgDataSet allocateBuffer()
```

### bool Chain([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read a record format using a key.

```cs
bool Chain(string formatName, bool lockRecord, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Read a record format using the relative record number.

```cs
bool ChainByRRN(string formatName, bool lockRecord, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Read a record format using the relative record number.

```cs
bool ChainByRRN(string formatName, bool lockRecord, decimal rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool Delete([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Delete the current record.

```cs
bool Delete(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record was found, false otherwise.

### bool Delete([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Delete the current record.

```cs
bool Delete(string formatName, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record was found, false otherwise.

### bool DeleteByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Delete a record using its relative record number.

```cs
bool DeleteByRRN(string formatName, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to delete.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record found, otherwise false.

### bool DeleteByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Delete a record using its relative record number.

```cs
bool DeleteByRRN(string formatName, decimal rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to delete.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record found, otherwise false.

### bool DeleteRange([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] firstKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\] lastKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeFirst rangeFirstKey](/reference/datagate/datagate-common/range-first.html), [RangeLast rangeLastKey](/reference/datagate/datagate-common/range-last.html))

Delete a range of records.

```cs
bool DeleteRange(string formatName, Object[] firstKey, Object[] lastKey, RangeFirst rangeFirstKey, RangeLast rangeLastKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to delete.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | firstKey | Array of key values for the first key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | lastKey | Array of key values for the last key.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirstKey | Initial include/exclude option.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLastKey | Last include/exclude option.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if found, false otherwise.

### bool ReadNext([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read the next record sequentially.

```cs
bool ReadNext(string formatName, bool lockRecord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadNextEqual([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the next record sequentially, if it has the same key.

```cs
bool ReadNextEqual(string formatName, bool lockRecord, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT Eof of File condition reached, false otherwise.

### bool ReadPrevious([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read the previous record sequentially.

```cs
bool ReadPrevious(string formatName, bool lockRecord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT End of File condition is reached, otherwise false.

### bool ReadPreviousEqual([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the previous record sequentially, if it has the same key.

```cs
bool ReadPreviousEqual(string formatName, bool lockRecord, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT End of File condition is reached, otherwise false.

### bool ReadRange([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] firstKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\] lastKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode mode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst rangeFirstKey](/reference/datagate/datagate-common/range-first.html), [RangeLast rangeLastKey](/reference/datagate/datagate-common/range-last.html), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read a range of records.

```cs
bool ReadRange(string formatName, Object[] firstKey, Object[] lastKey, RangeMode mode, RangeFirst rangeFirstKey, RangeLast rangeLastKey, bool lockRecord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | firstKey | Initial search key collection.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | lastKey | Last search key collection.
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | Requested Range mode.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirstKey | Initial Exclude/Include option.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLastKey | Last Exclude/Include option.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if a record was found, false otherwise.

### bool Seek([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [SeekMode mode](/reference/datagate/datagate-common/seek-mode.html), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Positions the file cursor in the record indicated by key.

```cs
bool Seek(string formatName, SeekMode mode, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to seek.
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | Seek mode.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record was found, false otherwise.

### bool SeekByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [SeekMode mode](/reference/datagate/datagate-common/seek-mode.html), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Positions the file cursor in the record indicated by relative record number.

```cs
bool SeekByRRN(string formatName, SeekMode mode, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | Seek mode.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record was found, false otherwise.

### void SetRange([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] firstKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\] lastKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode mode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst rangeFirstKey](/reference/datagate/datagate-common/range-first.html), [RangeLast rangeLastKey](/reference/datagate/datagate-common/range-last.html))

Sets the range of records for input operations.

```cs
void SetRange(string formatName, Object[] firstKey, Object[] lastKey, RangeMode mode, RangeFirst rangeFirstKey, RangeLast rangeLastKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | File format over which this operation will act.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | firstKey | Array of key values for the first key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | lastKey | Array of key values for the last key.
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | RangeMode value.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirstKey | Include/Exclude initial search key option.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLastKey | Include/Exclude last search key option.
