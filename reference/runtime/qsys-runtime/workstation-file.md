---
title: "WorkstationFile class         | QSYS API Reference Guide"
description: "Represents a Workstation file. It contains methods to handle all Input and Output operations on the file. "
last_modified_at: 2024-08-08T21:41:46Z
---

Represents a Workstation file. It contains methods to handle all Input and Output operations on the file.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [FileBase](/reference/runtime/qsys-runtime/file-base.html) --> [WorkstationFileBase](/reference/runtime/qsys-runtime/workstation-file-base.html)
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [allocateBuffer()](#adgdataset-allocatebuffer) | Allocates internal objects and constructs the file DataSet.
| [attachBuffer](#void-attachbufferadgdataset-adgdataset)([AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html)) | Set this file's DataSet to the given AdgDataSet.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-int-rrn-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-int-rrn-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-int-rrn-ids-optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-decimal-rrn-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-decimal-rrn-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Read a record by relative record number.
| [ChainByRRN](#bool-chainbyrrnstring-formatname-decimal-rrn-ids-optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record by relative record number.
| [DeleteByRRN](#bool-deletebyrrnstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Delete a record by relative record number.
| [DeleteByRRN](#bool-deletebyrrnstring-formatname-decimal-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Delete a record by relative record number.
| [ExFmt](#void-exfmtstring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Execute Format operation (Write followed by Read).
| [Read](#bool-readstring-formatname-ids-indds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Read a record.
| [Read](#bool-readstring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Read a record.
| [Read](#bool-readstring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Read a record.
| [Update](#void-updatestring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Update a record.
| [Update](#void-updatestring-formatname-indicator--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Update a record.
| [UpdateFlds](#void-updatefldsstring-formatname-string--fields)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Update a record, only the given named fields.
| [Write](#void-writestring-formatname-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Executes WRITE record operation.
| [Write](#void-writestring-formatname-indicator--optionindicators-ids-fromds)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html), [IDS](/reference/runtime/qsys-runtime/ids.html)) | Executes WRITE record operation.
| [WriteSubfile](#bool-writesubfilestring-formatname-int-rrn-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes WRITE Subfile record operation.
| [WriteSubfile](#bool-writesubfilestring-formatname-int-rrn-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Executes WRITE Subfile record operation.
| [WriteSubfile](#bool-writesubfilestring-formatname-decimal-rrn-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Executes WRITE Subfile record operation.
| [WriteSubfile](#bool-writesubfilestring-formatname-decimal-rrn-indicator--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html)) | Executes WRITE Subfile record operation.

### AdgDataSet allocateBuffer()

Allocates internal objects and constructs the file DataSet.

```cs
AdgDataSet allocateBuffer()
```

### void attachBuffer([AdgDataSet adgDataSet](/reference/datagate/datagate-client/adg-data-set.html))

Set this file's DataSet to the given AdgDataSet.

```cs
void attachBuffer(AdgDataSet adgDataSet)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | adgDataSet | The dataset to attach.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Read a record by relative record number.

```cs
bool ChainByRRN(string formatName, int rrn, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Read a record by relative record number.

```cs
bool ChainByRRN(string formatName, int rrn, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [IDS optionIndicators](/reference/runtime/qsys-runtime/ids.html))

Read a record by relative record number.

```cs
bool ChainByRRN(string formatName, int rrn, IDS optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Relative record number of the record to read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | optionIndicators | Indicator data structure to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Read a record by relative record number.

```cs
bool ChainByRRN(string formatName, decimal rrn, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to read.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Read a record by relative record number.

```cs
bool ChainByRRN(string formatName, decimal rrn, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to read.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool ChainByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [IDS optionIndicators](/reference/runtime/qsys-runtime/ids.html))

Read a record by relative record number.

```cs
bool ChainByRRN(string formatName, decimal rrn, IDS optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Relative record number of the record to read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | optionIndicators | Indicator data structure to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool DeleteByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Delete a record by relative record number.

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
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### bool DeleteByRRN([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types))

Delete a record by relative record number.

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
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, false otherwise.

### void ExFmt([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Execute Format operation (Write followed by Read).

```cs
void ExFmt(string formatName, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to execute.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the operation.

### bool Read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [IDS indDS](/reference/runtime/qsys-runtime/ids.html))

Read a record.

```cs
bool Read(string formatName, IDS indDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | indDS | Indicator data structure to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, False otherwise.

### bool Read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Read a record.

```cs
bool Read(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, False otherwise.

### bool Read([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Read a record.

```cs
bool Read(string formatName, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the read operation.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if record is found, False otherwise.

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
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | Input indicator Data Structure.

### void UpdateFlds([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String\[\] fields](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Update a record, only the given named fields.

```cs
void UpdateFlds(string formatName, String[] fields)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to update.
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fields | Input field name collection.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Executes WRITE record operation.

```cs
void Write(string formatName, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input format name.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the read operation.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html), [IDS fromDS](/reference/runtime/qsys-runtime/ids.html))

Executes WRITE record operation.

```cs
void Write(string formatName, Indicator[] optionIndicators, IDS fromDS)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input format name.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Indicator array to use in the read operation.
| [IDS](/reference/runtime/qsys-runtime/ids.html) | fromDS | Input Indicator Data Structure.

### bool WriteSubfile([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes WRITE Subfile record operation.

```cs
bool WriteSubfile(string formatName, int rrn, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Input subfile Relative Record Number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Input Option indicators.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT End of File condition reached, False otherwise.

### bool WriteSubfile([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Executes WRITE Subfile record operation.

```cs
bool WriteSubfile(string formatName, int rrn, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rrn | Input subfile Relative Record Number.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Input Option indicators.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT End of File condition reached, False otherwise.

### bool WriteSubfile([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Executes WRITE Subfile record operation.

```cs
bool WriteSubfile(string formatName, decimal rrn, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Input subfile Relative Record Number.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Input Option indicators.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT End of File condition reached, False otherwise.

### bool WriteSubfile([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [decimal rrn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [Indicator\[\] optionIndicators](/reference/runtime/qsys-runtime/indicator.html))

Executes WRITE Subfile record operation.

```cs
bool WriteSubfile(string formatName, decimal rrn, Indicator[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to read.
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | rrn | Input subfile Relative Record Number.
| [Indicator\[\]](/reference/runtime/qsys-runtime/indicator.html) | optionIndicators | Input Option indicators.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if NOT End of File condition reached, False otherwise.
