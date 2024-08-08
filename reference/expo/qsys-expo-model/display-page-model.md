---
title: "DisplayPageModel class        | QSYS API Reference Guide"
description: "Defines a specialized YellowPageModel class to provide support for fields in Records with data from the DataSet "
last_modified_at: 2024-08-08T21:42:10Z
---

Defines a specialized YellowPageModel class to provide support for fields in Records with data from the DataSet

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [PageModel](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.razorpages.pagemodel?view=aspnetcore-8.0) --> [YellowPageModel](/reference/expo/qsys-expo-model/yellow-page-model.html)
<br>
<br>

## Remarks

Record Model classes have a member instance of DisplayPageModel to provide support for data in the DataSet.

For example, the following `CUSTREC` Record Model definition:

```cs
public class CUSTREC_Model : RecordModel
{
    [Char(10)]
    private string CSRREC
    {
        get => CursorLocationFormatName;
        set { }
    }

    [Char(10)]
    private string CSRFLD
    {
        get => CursorLocationFieldName;
        set { }
    }
```

Is the implementation for the Legacy DDS [RTNCSRLOC](https://www.ibm.com/docs/en/i/7.2?topic=80-rtncsrloc-return-cursor-location-keyword-display-files). 

With the following Legacy DDS Record specification lines:

```
0076.00     A          R CUSTREC                                                       080401
.
.
.
0083.00     A                                      RTNCSRLOC(&CSRREC &CSRFLD)          080401
```

Which specify that the location of the Cursor (*record-name* and *row-and-column* values) should be copied to hidden fields in `CUSTREC` Model class, named `CSRREC` and `CSRFLD`.

When a Page is posted, the DataSet is loaded with feedback information (from posted data) and the instance of DisplayPageModel is updated, such that when the Logic Project's fields (such as `CSRREC` and `CSRFLD`) get populated, they will have the updated values from the recent user interaction.

## Constructors

| Name | Description |
| --- | --- |
| [DisplayPageModel()](#displaypagemodel) | Initializes a new instance of the DisplayPageModel class

### DisplayPageModel()

Initializes a new instance of the DisplayPageModel class

```cs
DisplayPageModel()
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AidProperty](/reference/expo/qsys-expo-model/aid-property.html) | AttnKeys | Gets an array of AidProperty Attention values, as defined in the Page Model. Attention Aid keys do not post data. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CursorLocationFieldName | Gets a value that indicating the name of field where the Cursor was last located on the Page. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CursorLocationFormatName | Gets a value that indicating the name of the format where the Cursor was last located on the Page. |
| [AidProperty](/reference/expo/qsys-expo-model/aid-property.html) | FuncKeys | Gets an array of AidProperty Function values, as defined in the Page Model.  |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | InputDataAvailable | Provides a mechanism to override the input data available state. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarDate | Gets the current day formatted as *DATE |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarSystemName | Gets the System Name formatted as *SYSTEMDATE |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarTime | Gets the current time formatted as *TIME |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | StarUserName | Gets the User Name formatted as *USER |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | UserDataIsInvalid | Gets a value indicating if the data entered by user is valid. |
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | ValidationErrorList | Gets a collection of validation error messages |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | ValidationErrorsFound | Gets a value indicating the existence of validation errors. |

## Methods

| Signature | Description |
| --- | --- |
| [ApplyEditCode](#string-applyeditcodedecimal-numeric-int-length-int-decimals-editcodes-editcode)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html)) | Formats value according to the provided EditCode
| [ApplyEditWord](#string-applyeditworddecimal-numeric-int-length-int-decimals-string-editword)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Formats value according to the provided EditWord
| [ClearModelProperties()](#void-clearmodelproperties) | Resets all records properties to their default values.
| [DumpModelPropertiesToDataSet()](#void-dumpmodelpropertiestodataset) | Updates the Dataset byc copying the field values from the Model properties
| [GetAidKeyType](#char-getaidkeytypeaidkey-key)([AidKey](/reference/expo/qsys-expo-model/aid-key.html)) | Gets a value that represents the code for the type of Aid key. 'A' for attention, 'F' for function.
| [GetDataRow](#datarow-getdatarowstring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the first DataRow from the DataTable with the given formatName from the active DataSet.
| [GetDataTable](#datatable-getdatatablestring-formatname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the DataTable with the format name given from the active Dataset. 
| [GetHasBeenRead()](#bool-gethasbeenread) | Gets value that indicates Workstation Dataset status
| [GetLastRecordModelWritten()](#recordmodel-getlastrecordmodelwritten) | Gets a value that indicates the last RecordModel written by the application logic.
| [GetMessageText](#string-getmessagetextstring-messagefilename-string-messageid-int-maxlength-string-replacementtext)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the message text from the external message file. Message files are external XML resources.
| [GetSubfileDataRow](#datarow-getsubfiledatarowstring-formatname-int-rrn)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the first DataRow from the DataTable with the given subfile formatName from the active DataSet.
| [IsKeyEnabled](#bool-iskeyenabledaidkey-aidkey)([AidKey](/reference/expo/qsys-expo-model/aid-key.html)) | Gets the state of the requested AidKey.
| [LoadFeedbackValues()](#bool-loadfeedbackvalues) | Populates the Feedback values on the Active DisplayFile from posted data.
| [LoadModelPropertiesFromDataSet](#void-loadmodelpropertiesfromdatasetbool-onlynonpostedfields)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Refreshes the Model properties by loading values from the active Dataset
| [LoadModelStateErrors()](#void-loadmodelstateerrors) | Populates the collection of validation errors.
| [SelectMyAction](#iactionresult-selectmyactionbool-valid)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Selects the appropriate action to format a response Page.
| [SetResponseIndicators()](#void-setresponseindicators) | Sets the response indicators in the Dataset from the Display page attributes.

### string ApplyEditCode([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [EditCodes editCode](/reference/expo/qsys-expo-model/edit-codes.html))

Formats value according to the provided EditCode

```cs
string ApplyEditCode(decimal numeric, int length, int decimals, EditCodes editCode)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | input decimal value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | field decimal positions
| [EditCodes](/reference/expo/qsys-expo-model/edit-codes.html) | editCode | EditCodes enumeration value

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted value as string

### string ApplyEditWord([decimal numeric](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int decimals](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string editWord](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Formats value according to the provided EditWord

```cs
string ApplyEditWord(decimal numeric, int length, int decimals, string editWord)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal) | numeric | input decimal value
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | field length
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | decimals | field decimal positions
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | editWord | EditWord specification

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the formatted value as string

### void ClearModelProperties()

Resets all records properties to their default values.

```cs
void ClearModelProperties()
```

### void DumpModelPropertiesToDataSet()

Updates the Dataset byc copying the field values from the Model properties

```cs
void DumpModelPropertiesToDataSet()
```

### char GetAidKeyType([AidKey key](/reference/expo/qsys-expo-model/aid-key.html))

Gets a value that represents the code for the type of Aid key. 'A' for attention, 'F' for function.

```cs
char GetAidKeyType(AidKey key)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | key | AidKey enumeration value

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | character 'A' for attention, 'F' for function

### DataRow GetDataRow([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the first DataRow from the DataTable with the given formatName from the active DataSet.

```cs
DataRow GetDataRow(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | 

#### Returns

| Type | Description
| --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | The first DataRow.

### DataTable GetDataTable([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the DataTable with the format name given from the active Dataset. 

```cs
DataTable GetDataTable(string formatName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | 

#### Returns

| Type | Description
| --- | ---
| [DataTable](https://learn.microsoft.com/en-us/dotnet/api/system.data.datatable.select?view=net-8.0) | The DataTable

### bool GetHasBeenRead()

Gets value that indicates Workstation Dataset status

```cs
bool GetHasBeenRead()
```

### RecordModel GetLastRecordModelWritten()

Gets a value that indicates the last RecordModel written by the application logic.

```cs
RecordModel GetLastRecordModelWritten()
```

### string GetMessageText([string messageFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string messageId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int maxLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string replacementText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the message text from the external message file. Message files are external XML resources.

```cs
string GetMessageText(string messageFileName, string messageId, int maxLength, string replacementText)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageFileName | name of message XML file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageId | named identifier for the message to retrieve.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxLength | maximum characters to copy from message text in the file, defaults to MaxValue.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | replacementText | data to use for replacment text place holders in message, defaults to empty.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | the text as string

### DataRow GetSubfileDataRow([string formatName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int RRN](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the first DataRow from the DataTable with the given subfile formatName from the active DataSet.

```cs
DataRow GetSubfileDataRow(string formatName, int RRN)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | formatName | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | RRN | 

#### Returns

| Type | Description
| --- | ---
| [DataRow](https://learn.microsoft.com/en-us/dotnet/api/system.data.datarow?view=net-8.0) | The first DataRow.

### bool IsKeyEnabled([AidKey aidKey](/reference/expo/qsys-expo-model/aid-key.html))

Gets the state of the requested AidKey.

```cs
bool IsKeyEnabled(AidKey aidKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AidKey](/reference/expo/qsys-expo-model/aid-key.html) | aidKey | Value from enumeration indicating the key to test

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the AidKey is enabled

### bool LoadFeedbackValues()

Populates the Feedback values on the Active DisplayFile from posted data.

```cs
bool LoadFeedbackValues()
```

### void LoadModelPropertiesFromDataSet([bool onlyNonPostedFields](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Refreshes the Model properties by loading values from the active Dataset

```cs
void LoadModelPropertiesFromDataSet(bool onlyNonPostedFields)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | onlyNonPostedFields | Determines which fields should be refreshed

### void LoadModelStateErrors()

Populates the collection of validation errors.

```cs
void LoadModelStateErrors()
```

### IActionResult SelectMyAction([bool valid](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Selects the appropriate action to format a response Page.

```cs
IActionResult SelectMyAction(bool valid)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | valid | indicates if the posted page passed validation

#### Returns

| Type | Description
| --- | ---
| [IActionResult](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.iactionresult?view=aspnetcore-8.0) | Action method result

### void SetResponseIndicators()

Sets the response indicators in the Dataset from the Display page attributes.

```cs
void SetResponseIndicators()
```
