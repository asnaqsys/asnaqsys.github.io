---
title: "RecordModel class             | QSYS API Reference Guide"
description: "Defines the RecordModel class "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines the RecordModel class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Remarks

The class `RecordModel Class` encapsulates methods, property fields to implement the concept of [Record-Level entries for IBM i Display File](https://www.ibm.com/docs/en/i/7.4?topic=files-defining-display-file-dds).

[SubfileControlModel](/reference/expo/qsys-expo-model/subfile-control-model.html) and [SubfileRecordModel](/reference/expo/qsys-expo-model/subfile-record-model.html) are specialized classes based on `RecordModel Class`.

The following is a typical use of a class derived from `RecordModel Class`, which describes - *among other things* - the Display fields in the record.

```cs
[
    Record(FunctionKeys = "F4 04;F6 06:!30;F11 11:!30;F12 12",
        EraseFormats = "SFLC KEYS SALESREC"
    )
]
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

    [Char(10)]
    public string SCPGM { get; private set; }

    [Dec(6, 0)]
    public decimal SFCUSTNO { get; private set; } // CUSTOMER NUMBER

    [Char(40)]
    public string SFOLDNAME { get; private set; }

    [Char(40)]
    public string SFNAME { get; set; }

    [Char(35)]
    public string SFADDR1 { get; set; }

    [Char(35)]
    public string SFADDR2 { get; set; }

    [Char(30)]
    public string SFCITY { get; set; }

    [Char(2)]
    public string SFSTATE { get; set; }

    [Char(10)]
    public string SFPOSTCODE { get; set; }

    [Dec(10, 0)]
    public decimal SFFAX { get; set; }

    [Char(20)]
    public string SFPHONE { get; set; }

    [Char(1)]
    public string SFSTATUS { get; set; }

    [Char(40)]
    public string SFCONTACT { get; set; }

    [Char(40)]
    public string SFCONEMAL { get; set; }

    [Char(1)]
    public string SFYN01 { get; set; }
}

```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AidProperty](/reference/expo/qsys-expo-model/aid-property.html) | AttnKeys | Gets or sets the Attention Keys AID Property |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | BlueDirection | Internal use - Record direction code. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CursorLocationFieldName | Gets or sets the Cursor Location Field Name |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | CursorLocationFormatName | Gets or sets the Cursor Location Format Name |
| [AidProperty](/reference/expo/qsys-expo-model/aid-property.html) | FuncKeys | Gets or sets the Function Keys AID Property |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsActive | Gets a boolean value indicating that the Record is active |

## Methods

| Signature | Description |
| --- | --- |
| [AddErrorMessage](#void-adderrormessagestring-errormessageinfo-string-fieldnameid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds an Error Message to the list of Validation errors
| [GetMessageText](#string-getmessagetextstring-messagefilename-string-messageid-int-maxlength-string-replacementtext)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string value with the text corresponding to the message requested.
| [GetOptionIndicator](#bool-getoptionindicatorint-indicator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the option indicator value.
| [GetOptionIndicators()](#boolean--getoptionindicators) | Gets a copy of the array of option indicators.
| [GetResponseIndicator](#char-getresponseindicatorint-indicator)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the response indicator value. May be '0', '1' or 'X'.
| [GetResponseIndicators()](#char--getresponseindicators) | Gets a copy of the response indicators.
| [IsFalse](#bool-isfalsestring-condition)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the resulting value of the evaluation of condition using the optionIndicators.  
| [IsNotFalse](#bool-isnotfalsestring-condition)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the resulting value of the evaluation of condition using the optionIndicators.
| [IsNotTrue](#bool-isnottruestring-condition)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a boolean value indicating the result of evaluation of the condition using the optionIndicators.  
| [IsTrue](#bool-istruestring-condition)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the resulting value of the evaluation of the condition using the optionIndicators.
| [ProcessErrorMessages](#bool-processerrormessagesstring-recordname-string-fieldnameid-conditionalproperty-errormessage-conditionalproperty-errormessageid)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html), [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html)) | Process Error Message for a field in a record if the condition succeeds
| [ResolveConditionalProperty](#string-resolveconditionalpropertystring-conditionalpropertystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string value that indicates the result of the condition in the property given as a string
| [ResolveConditionalProperty](#string-resolveconditionalpropertyconditionalproperty-conditionalproperty)([ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html)) | Gets a string value that indicates the result of the condition in the property given
| [SetOptionIndicator](#void-setoptionindicatorint-indicator-bool-newvalue)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Sets the option indicator value.
| [SetResponseIndicator](#void-setresponseindicatorint-indicator-char-newvalue01x)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Sets the response indicator value.
| [WasRecordPosted](#bool-wasrecordpostedstring-recordname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a boolean value that indicates if the Record was posted

### void AddErrorMessage([string errorMessageInfo](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string fieldNameID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Adds an Error Message to the list of Validation errors

```cs
void AddErrorMessage(string errorMessageInfo, string fieldNameID)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | errorMessageInfo | error information
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldNameID | field name ID

### string GetMessageText([string messageFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string messageId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int maxLength](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string replacementText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a string value with the text corresponding to the message requested.

```cs
string GetMessageText(string messageFileName, string messageId, int maxLength, string replacementText)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageFileName | Message filename
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageId | Message ID
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxLength | Maximum chars to copy
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | replacementText | data to use for replacment text place holders in message, defaults to empty.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The Message text

### bool GetOptionIndicator([int indicator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the option indicator value.

```cs
bool GetOptionIndicator(int indicator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indicator | 1 ... 99

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Boolean value

### Boolean[] GetOptionIndicators()

Gets a copy of the array of option indicators.

```cs
Boolean[] GetOptionIndicators()
```

### char GetResponseIndicator([int indicator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets the response indicator value. May be '0', '1' or 'X'.

```cs
char GetResponseIndicator(int indicator)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indicator | 1 ... 99

#### Returns

| Type | Description
| --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | Char value.

### Char[] GetResponseIndicators()

Gets a copy of the response indicators.

```cs
Char[] GetResponseIndicators()
```

### bool IsFalse([string condition](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the resulting value of the evaluation of condition using the optionIndicators.  

```cs
bool IsFalse(string condition)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Return true only if there is no doubt about it. If anything goes wrong, return false

### bool IsNotFalse([string condition](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the resulting value of the evaluation of condition using the optionIndicators.

```cs
bool IsNotFalse(string condition)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Return true only if there is no doubt about it. If anything goes wrong, return false

### bool IsNotTrue([string condition](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a boolean value indicating the result of evaluation of the condition using the optionIndicators.  

```cs
bool IsNotTrue(string condition)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Return false only if there is no doubt about it. If anything goes wrong, return true

### bool IsTrue([string condition](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets the resulting value of the evaluation of the condition using the optionIndicators.

```cs
bool IsTrue(string condition)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | false only if there is no doubt about it. If anything goes wrong, return true

### bool ProcessErrorMessages([string recordName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string fieldNameID](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ConditionalProperty errorMessage](/reference/expo/qsys-expo-model/conditional-property.html), [ConditionalProperty errorMessageId](/reference/expo/qsys-expo-model/conditional-property.html))

Process Error Message for a field in a record if the condition succeeds

```cs
bool ProcessErrorMessages(string recordName, string fieldNameID, ConditionalProperty errorMessage, ConditionalProperty errorMessageId)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordName | name of record
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldNameID | field ID
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | errorMessage | error message
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | errorMessageId | error message ID

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if error condition and error message was added to the validation error collection

### string ResolveConditionalProperty([string conditionalPropertyString](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a string value that indicates the result of the condition in the property given as a string

```cs
string ResolveConditionalProperty(string conditionalPropertyString)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | conditionalPropertyString | conditional property string

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value corresponding to the condition

### string ResolveConditionalProperty([ConditionalProperty conditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html))

Gets a string value that indicates the result of the condition in the property given

```cs
string ResolveConditionalProperty(ConditionalProperty conditionalProperty)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ConditionalProperty](/reference/expo/qsys-expo-model/conditional-property.html) | conditionalProperty | conditional property string

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value corresponding to the condition

### void SetOptionIndicator([int indicator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [bool newValue](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Sets the option indicator value.

```cs
void SetOptionIndicator(int indicator, bool newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indicator | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | newValue | 

### void SetResponseIndicator([int indicator](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [char newValue01X](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char))

Sets the response indicator value.

```cs
void SetResponseIndicator(int indicator, char newValue01X)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | indicator | 1 ... 99
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | newValue01X | New value, may be '0', '1' or 'X'

### bool WasRecordPosted([string recordName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Gets a boolean value that indicates if the Record was posted

```cs
bool WasRecordPosted(string recordName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordName | name of the Record to check

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true is the Record was posted
