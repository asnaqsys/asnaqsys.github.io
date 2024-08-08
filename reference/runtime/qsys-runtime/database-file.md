---
title: "DatabaseFile class            | QSYS API Reference Guide"
description: "Represents a single format Database data file. It contains methods to handle all Input and Output operations on the file. "
last_modified_at: 2024-08-08T21:41:46Z
---

Represents a single format Database data file. It contains methods to handle all Input and Output operations on the file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [FileBase](/reference/runtime/qsys-runtime/file-base.html) --> [DatabaseFileBase](/reference/runtime/qsys-runtime/database-file-base.html)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | Key | Gets or sets the main search key. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | Kez | Gets or sets the secondary search key, used as the limit for range operations. |

## Methods

| Signature | Description |
| --- | --- |
| [allocateBuffer()](#adgdataset-allocatebuffer) | Allocates internal objects and constructs the file DataSet.
| [Chain](#bool-chainbool-lockrecord-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read a record format using a key.
| [Chain](#bool-chainbool-lockrecord-ids-intods-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read a record format using a key.
| [ChainByRRN](#bool-chainbyrrnbool-lockrecord-int-rrn)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnbool-lockrecord-int-rrn-ids-intods)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnbool-lockrecord-decimal-rrn)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnbool-lockrecord-decimal-rrn-ids-intods)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record by relative record number.
| [Check](#bool-checkobject--keyparts)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Validate that a record exists.
| [Delete()](#bool-delete) | Delete the current record.
| [Delete](#bool-deleteobject--keyparts)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Delete the current record.
| [DeleteByRRN](#bool-deletebyrrnint-rrn)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Delete a record using its relative record number.
| [DeleteByRRN](#bool-deletebyrrndecimal-rrn)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Delete a record using its relative record number.
| [DeleteRange](#bool-deleterangeobject--firstkey-object--lastkey-rangefirst-rangefirstkey-rangelast-rangelastkey)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Delete a range of records.
| [Feod()](#void-feod) | Force end of data on the current record.
| [ReadNext](#bool-readnextbool-lockrecord)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read the next record sequentially.
| [ReadNext](#bool-readnextbool-lockrecord-ids-intods)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read the next record sequentially.
| [ReadNextEqual](#bool-readnextequalbool-lockrecord-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the next record sequentially, if it has the same key.
| [ReadNextEqual](#bool-readnextequalbool-lockrecord-ids-intods-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the next record sequentially, if it has the same key.
| [ReadNextEqualIncompleteKey](#bool-readnextequalincompletekeybool-lockrecord-string-incompletekey-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read sequentially a record with an incomplete key buffer.
| [ReadNextEqualIncompleteKey](#bool-readnextequalincompletekeybool-lockrecord-ids-intods-string-incompletekey-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read sequentially a record with an incomplete key buffer.
| [ReadPrevious](#bool-readpreviousbool-lockrecord)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read the previous record sequentially.
| [ReadPrevious](#bool-readpreviousbool-lockrecord-ids-intods)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read the previous record sequentially.
| [ReadPreviousEqual](#bool-readpreviousequalbool-lockrecord-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the previous record sequentially, if it has the same key.
| [ReadPreviousEqual](#bool-readpreviousequalbool-lockrecord-ids-intods-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the previous record sequentially, if it has the same key.
| [ReadPreviousEqualIncompleteKey](#bool-readpreviousequalincompletekeybool-lockrecord-string-incompletekey-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the previous record sequentially, with an incomplete key buffer.
| [ReadPreviousEqualIncompleteKey](#bool-readpreviousequalincompletekeybool-lockrecord-ids-intods-string-incompletekey-object--keyparts)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS](/reference/runtime/qsys-runtime/ids.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Read the previous record sequentially, with an incomplete key buffer.
| [ReadRange](#bool-readrangeobject--firstkey-object--lastkey-rangemode-mode-rangefirst-rangefirstkey-rangelast-rangelastkey-bool-lockrecord)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [RangeLast](/reference/datagate/datagate-common/range-last.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Read a range of records.
| [Seek](#bool-seekseekmode-mode-object--keyparts)([SeekMode](/reference/datagate/datagate-common/seek-mode.html), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Positions the file cursor in the record indicated by key.
| [SeekByRRN](#bool-seekbyrrnseekmode-mode-int-rrn)([SeekMode](/reference/datagate/datagate-common/seek-mode.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Positions the file cursor in the record indicated by relative record number.
| [SetRange](#void-setrangeobject--firstkey-object--lastkey-rangemode-mode-rangefirst-rangefirstkey-rangelast-rangelastkey)([Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst](/reference/datagate/datagate-common/range-first.html), [RangeLast](/reference/datagate/datagate-common/range-last.html)) | Sets the range of records for input operations.
| [Update()](#void-update) | Update a record.
| [Update](#void-updateids-fromds)([IDS](/reference/runtime/qsys-runtime/ids.html)) | Update a record.
| [UpdateFlds](#void-updatefldsstring--fields)([String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Update a record, only those fields listed.
| [Write()](#void-write) | Write a record.
| [Write](#void-writeids-fromds)([IDS](/reference/runtime/qsys-runtime/ids.html)) | Write a record.

### AdgDataSet allocateBuffer()

Allocates internal objects and constructs the file DataSet.

```cs
AdgDataSet allocateBuffer()
```

### bool Chain([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read a record format using a key.

```cs
bool Chain(bool lockRecord, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool Chain([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read a record format using a key.

```cs
bool Chain(bool lockRecord, IDS intoDS, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool ChainByRRN([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Read a record by relative record number.

```cs
bool ChainByRRN(bool lockRecord, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True if locking should be performed; false otherwise.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool ChainByRRN([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read a record by relative record number.

```cs
bool ChainByRRN(bool lockRecord, int rrn, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True if locking should be performed; false otherwise.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool ChainByRRN([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Read a record by relative record number.

```cs
bool ChainByRRN(bool lockRecord, decimal rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True if locking should be performed; false otherwise.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool ChainByRRN([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read a record by relative record number.

```cs
bool ChainByRRN(bool lockRecord, decimal rrn, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True if locking should be performed; false otherwise.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool Check([Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Validate that a record exists.

```cs
bool Check(Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool Delete()

Delete the current record.

```cs
bool Delete()
```

### bool Delete([Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Delete the current record.

```cs
bool Delete(Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Input search key collection.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool DeleteByRRN([int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Delete a record using its relative record number.

```cs
bool DeleteByRRN(int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to delete.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool DeleteByRRN([decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Delete a record using its relative record number.

```cs
bool DeleteByRRN(decimal rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to delete.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record is found, false otherwise.

### bool DeleteRange([Object\[\] firstKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\] lastKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeFirst rangeFirstKey](/reference/datagate/datagate-common/range-first.html), [RangeLast rangeLastKey](/reference/datagate/datagate-common/range-last.html))

Delete a range of records.

```cs
bool DeleteRange(Object[] firstKey, Object[] lastKey, RangeFirst rangeFirstKey, RangeLast rangeLastKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | firstKey | Array of key values for the first key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | lastKey | Array of key values for the last key.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirstKey | RangeFirst value.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLastKey | RangeLast value.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if records were found; false otherwise.

### void Feod()

Force end of data on the current record.

```cs
void Feod()
```

### bool ReadNext([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read the next record sequentially.

```cs
bool ReadNext(bool lockRecord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadNext([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read the next record sequentially.

```cs
bool ReadNext(bool lockRecord, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadNextEqual([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the next record sequentially, if it has the same key.

```cs
bool ReadNextEqual(bool lockRecord, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadNextEqual([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the next record sequentially, if it has the same key.

```cs
bool ReadNextEqual(bool lockRecord, IDS intoDS, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadNextEqualIncompleteKey([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [string incompleteKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read sequentially a record with an incomplete key buffer.

```cs
bool ReadNextEqualIncompleteKey(bool lockRecord, string incompleteKey, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | incompleteKey | Incomplete search key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadNextEqualIncompleteKey([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html), [string incompleteKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read sequentially a record with an incomplete key buffer.

```cs
bool ReadNextEqualIncompleteKey(bool lockRecord, IDS intoDS, string incompleteKey, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | incompleteKey | Incomplete search key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadPrevious([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read the previous record sequentially.

```cs
bool ReadPrevious(bool lockRecord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadPrevious([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html))

Read the previous record sequentially.

```cs
bool ReadPrevious(bool lockRecord, IDS intoDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadPreviousEqual([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the previous record sequentially, if it has the same key.

```cs
bool ReadPreviousEqual(bool lockRecord, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadPreviousEqual([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the previous record sequentially, if it has the same key.

```cs
bool ReadPreviousEqual(bool lockRecord, IDS intoDS, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadPreviousEqualIncompleteKey([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [string incompleteKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the previous record sequentially, with an incomplete key buffer.

```cs
bool ReadPreviousEqualIncompleteKey(bool lockRecord, string incompleteKey, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | incompleteKey | Incomplete search key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadPreviousEqualIncompleteKey([bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [IDS intoDS](/reference/runtime/qsys-runtime/ids.html), [string incompleteKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Read the previous record sequentially, with an incomplete key buffer.

```cs
bool ReadPreviousEqualIncompleteKey(bool lockRecord, IDS intoDS, string incompleteKey, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | lockRecord | True to lock the record after the Read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | intoDS | IDS object that receives the data read.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | incompleteKey | Incomplete search key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if End Of File condition is NOT reached, false otherwise.

### bool ReadRange([Object\[\] firstKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\] lastKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode mode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst rangeFirstKey](/reference/datagate/datagate-common/range-first.html), [RangeLast rangeLastKey](/reference/datagate/datagate-common/range-last.html), [bool lockRecord](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Read a range of records.

```cs
bool ReadRange(Object[] firstKey, Object[] lastKey, RangeMode mode, RangeFirst rangeFirstKey, RangeLast rangeLastKey, bool lockRecord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
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

### bool Seek([SeekMode mode](/reference/datagate/datagate-common/seek-mode.html), [Object\[\] keyParts](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Positions the file cursor in the record indicated by key.

```cs
bool Seek(SeekMode mode, Object[] keyParts)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | Seek mode.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | keyParts | Collection of search keys.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record was found, false otherwise.

### bool SeekByRRN([SeekMode mode](/reference/datagate/datagate-common/seek-mode.html), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Positions the file cursor in the record indicated by relative record number.

```cs
bool SeekByRRN(SeekMode mode, int rrn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | Seek mode.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative Record Number.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the record was found, false otherwise.

### void SetRange([Object\[\] firstKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object\[\] lastKey](https://docs.microsoft.com/en-us/dotnet/api/system.object), [RangeMode mode](/reference/datagate/datagate-common/range-mode.html), [RangeFirst rangeFirstKey](/reference/datagate/datagate-common/range-first.html), [RangeLast rangeLastKey](/reference/datagate/datagate-common/range-last.html))

Sets the range of records for input operations.

```cs
void SetRange(Object[] firstKey, Object[] lastKey, RangeMode mode, RangeFirst rangeFirstKey, RangeLast rangeLastKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | firstKey | Array of key values for the first key.
| [Object\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.object) | lastKey | Array of key values for the last key.
| [RangeMode](/reference/datagate/datagate-common/range-mode.html) | mode | RangeMode value.
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirstKey | Include/Exclude initial search key option.
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLastKey | Include/Exclude last search key option.

### void Update()

Update a record.

```cs
void Update()
```

### void Update([IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Update a record.

```cs
void Update(IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | Update record by copying record data from Data Structure.

### void UpdateFlds([String\[\] fields](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Update a record, only those fields listed.

```cs
void UpdateFlds(String[] fields)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fields | Collection of record fields.

### void Write()

Write a record.

```cs
void Write()
```

### void Write([IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Write a record.

```cs
void Write(IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | IDS object where the data comes from.
