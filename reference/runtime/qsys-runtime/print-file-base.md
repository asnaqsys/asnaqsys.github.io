---
title: "PrintFileBase class           | QSYS API Reference Guide"
description: "Base class for Database print files. Contains the print file setup information and some output operations. "
last_modified_at: 2024-08-08T21:41:46Z
---

Base class for Database print files. Contains the print file setup information and some output operations.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [PrintFileBase](#printfilebasestring-string-string-boolean-action)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0)) | Initializes a new instance of the PrintFileBase class.
| [PrintFileBase](#printfilebasestring-string-string-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the PrintFileBase class.
| [PrintFileBase](#printfilebasestring-string-sharetypes-boolean-action)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0)) | Initializes a new instance of the PrintFileBase class.
| [PrintFileBase](#printfilebasestring-string-sharetypes-boolean)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Initializes a new instance of the PrintFileBase class.

### PrintFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0))

Initializes a new instance of the PrintFileBase class.

```cs
PrintFileBase(String, String, String, Boolean, Action)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclPrintFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareType | String value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID.
| [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0) | infSR | Method called when there is an error in a file operation. Pass null if there is no infSR.

### PrintFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the PrintFileBase class.

```cs
PrintFileBase(String, String, String, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclPrintFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | shareType | String value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID.

### PrintFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean), [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0))

Initializes a new instance of the PrintFileBase class.

```cs
PrintFileBase(String, String, ShareTypes, Boolean, Action)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclPrintFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | ShareTypes value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID.
| [Action](https://learn.microsoft.com/en-us/dotnet/api/system.action?view=net-8.0) | infSR | Method called when there is an error in a file operation. Pass null if there is no infSR.

### PrintFileBase([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Initializes a new instance of the PrintFileBase class.

```cs
PrintFileBase(String, String, ShareTypes, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dclPrintFileName | Field name for this file in the program.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path to the file in the Database, given as "library/filename".
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | ShareTypes value that selects the type of file sharing.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isFormatID | True to check format ID.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Collate | Gets or sets whether collation will be used when printing multiple copies.  This property is of type *Boolean. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Copies | Gets or sets the number of copies to print.  This property is of type *Integer4.    |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CursorY | Gets the position, in Print Units, that the printer is from the top of the page.  This property is of type *Integer4. |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | DataSet | Gets the AdgDataSet that moves data between the program and the database. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DclFileName | Gets the name of this file field in the program. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DclPrintFileName | Gets the name of this file field in the program. |
| [Duplex](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.duplex?view=dotnet-plat-ext-8.0) | Duplex | Gets or sets whether the printer file is to print duplex (prints on both sides of the paper).  This property is of type ASNA.DataGate.Common.PrintDuplex.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FilePath | A string that specifies the path of the file.  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | FooterSize | Gets the size of the page footer.  This property is of type *Integer4. |
| [Dictionary\<String, String\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | formatIDs | When overriden in a derived class, gets the mapping from record format names to formatIDs. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormName | Gets or sets the customized page size to use.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormType | Gets or sets the type of forms used in the printer for printed output. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InOverflow | Return whether the printer has entered the overflow area of the page. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsFormatID | A boolean value that specifies if the Format IDs of the file should be checked when the file is opened. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsOpen | Gets a value indicating whether the file is open. |
| [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html) | LastException | Gets the last exception thrown for this file.  This is a protected public field of type ASNA.QSys.RuntimeException. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ManuscriptPath | Gets or sets the path and file name for the manuscript. |
| [PaperOrientation](/reference/datagate/datagate-common/paper-orientation.html) | Orientation | Gets or sets the printer’s paper orientation (Horizontal or Vertical).  This property is of type ASNA.DataGate.Common.PaperOrientation.    |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PageCount | Gets the count of pages already printed.  This property is of type *Integer4. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PaperLength | Gets or sets the paper length.  This property is of type *Integer4. |
| [PaperKind](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.paperkind?view=dotnet-plat-ext-8.0) | PaperSize | Gets or sets the paper size.  This property is of type ASNA.DataGate.Common.PaperSize.    |
| [PaperSourceKind](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.papersourcekind?view=dotnet-plat-ext-8.0) | PaperSource | Gets or sets the paper source.  This property is of type ASNA.DataGate.Common.PaperSource. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PaperWidth | Gets or sets the paper width.  This property is of type *Integer4. |
| [AccessMode](/reference/datagate/datagate-common/access-mode.html) | Preview | Gets or sets whether the print preview dialog is to be displayed before printing.  This property is of type ASNA.DataGate.Common.AccessMode.  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PrintableLength | Gets the printer's printable Length.  This property is of type *Integer4. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | PrintableWidth | Gets the printer’s printable width.  This property is of type *Integer4. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Printer | Gets or sets the name of the printer to be used.  This property is of type *string.     |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | PrintSetup | Gets or sets whether the print setup dialog is to display before printing.  This property is of type *Boolean. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PrintToFileName | Gets or sets the system file name, with path, where the report will be rendered.Setting the value to something other than *NOTHING will direct the printer to print to a file. This is particularly useful with the Microsoft Print To printers. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ProcessMacro | Gets or sets the whether DataGate is to search for “macros” and replace them with appropriate information before printing.  This property is of type *Boolean. |
| [PrinterResolutionKind](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.printerresolutionkind?view=dotnet-plat-ext-8.0) | Quality | Gets or sets the print quality.  This property is of type ASNA.DataGate.Common.PrintQuality.      |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ReportName | Gets or sets the name of the report.  If not assigned, the default name is the name given when the print file was declared.  This property is of type *string.  This is the name of the print file seen on the printer spool.  |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | SaveAfter | Gets or sets the value that specifies whether the manuscript is saved after output is produced  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Scale | Gets or sets the percentage factor by which the printed document is to be scaled.  This property is of type *Integer4. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ShareType | A string defining how a file will be shared.  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | StatusCode | Gets the status code resulting from a file operation. |
| [PrintTrueType](/reference/datagate/datagate-common/print-true-type.html) | TTOption | Gets or sets how true type fonts are to be printed.  This property is of type ASNA.DataGate.Common.PrintTrueType. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UseColor | Gets or sets whether to use color when a color printer is specified.  This property is of type *Boolean.  |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | UserData | Gets or sets a user defined string  |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | YResolution | Gets or sets the Y-Resolution in dot per inch.  This property is of type *Integer4.  |

## Methods

| Signature | Description |
| --- | --- |
| [allocateBuffer()](#adgdataset-allocatebuffer) | Allocates a DataSet Buffer.
| [close()](#void-close) | Close a file.
| [Close()](#void-close) | Close a file.
| [Dispose()](#void-dispose) | Releases resources.
| [Dispose](#void-disposebool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases resources.
| [feod](#void-feodstring-formatname-bool-reset)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Force end of data on the given record.
| [Feod](#void-feodstring-formatname-bool-reset)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Force end of data on the given record.
| [Finalize()](#void-finalize) | Releases resources when the instance is garbage-collected.
| [GetPrintFieldPropertyValue](#object-getprintfieldpropertyvaluestring-formatname-string-fieldname-string-propertyname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Get a field property value.
| [open](#void-opendatabase-database)([Database](/reference/runtime/qsys-runtime/database.html)) | Open the print file.
| [Open](#void-opendatabase-database)([Database](/reference/runtime/qsys-runtime/database.html)) | Open the print file.
| [populateBuffer](#void-populatebufferstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Calls the delegate to populate buffer from fields.
| [SetPrintFieldPropertyValue](#void-setprintfieldpropertyvaluestring-formatname-string-fieldname-string-propertyname-object-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Set a field property value.
| [write](#void-writestring-formatname-string-inddsstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Write a record.
| [write](#void-writestring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Write a record given its record format name.
| [Write](#void-writestring-formatname-string-inddsstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Write a record.
| [Write](#void-writestring-formatname-char--optionindicators)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Write a record given its record format name.

### AdgDataSet allocateBuffer()

Allocates a DataSet Buffer.

```cs
AdgDataSet allocateBuffer()
```

### void close()

Close a file.

```cs
void close()
```

### void Close()

Close a file.

```cs
void Close()
```

### void Dispose()

Releases resources.

```cs
void Dispose()
```

### void Dispose([bool isDisposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases resources.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | True when this method is called during nomral execution, when resources are guarantedd to be available to release.            False when called from the garbage collector.

### void feod([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool reset](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Force end of data on the given record.

```cs
void feod(string formatName, bool reset)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | reset | True to reset the print attributes.

### void Feod([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool reset](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Force end of data on the given record.

```cs
void Feod(string formatName, bool reset)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | reset | True to reset the print attributes.

### void Finalize()

Releases resources when the instance is garbage-collected.

```cs
void Finalize()
```

### object GetPrintFieldPropertyValue([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string fieldName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string propertyName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Get a field property value.

```cs
object GetPrintFieldPropertyValue(string formatName, string fieldName, string propertyName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldName | Name of the field.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | propertyName | Name of the property to get.

#### Returns

| Type | Description
| --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | The property value. Throws exception if file is not open.

### void open([Database database](/reference/runtime/qsys-runtime/database.html))

Open the print file.

```cs
void open(Database database)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Database](/reference/runtime/qsys-runtime/database.html) | database | Database where the file is located.

### void Open([Database database](/reference/runtime/qsys-runtime/database.html))

Open the print file.

```cs
void Open(Database database)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Database](/reference/runtime/qsys-runtime/database.html) | database | Database where the file is located.

### void populateBuffer([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Calls the delegate to populate buffer from fields.

```cs
void populateBuffer(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Input record format name.

### void SetPrintFieldPropertyValue([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string fieldName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string propertyName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [object value](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Set a field property value.

```cs
void SetPrintFieldPropertyValue(string formatName, string fieldName, string propertyName, object value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldName | Name of the field.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | propertyName | Name of the property to set.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | Value to set on the property.

### void write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string indDsString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Write a record.

```cs
void write(string formatName, string indDsString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | indDsString | String of 100 character representing the indicator data structure.

### void write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Write a record given its record format name.

```cs
void write(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the write operation.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string indDsString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Write a record.

```cs
void Write(string formatName, string indDsString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | indDsString | String of 100 character representing the indicator data structure.

### void Write([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [Char\[\] optionIndicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Write a record given its record format name.

```cs
void Write(string formatName, Char[] optionIndicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | Name of the record format to write.
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | optionIndicators | Indicator array to use in the write operation.
