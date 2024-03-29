---
title: RecordModel Class
---

Defines the RecordModel class

**Namespace:** ASNA.QSys.Expo.Model <br/>
**Assembly:** ASNA.QSys.Expo.Model

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> RecordModel

<br>
<br>

## Remarks

The class `RecordModel Class` encapsulates methods, property fields to implement the concept of [Record-Level entries for IBM i Display File](https://www.ibm.com/docs/en/i/7.4?topic=files-defining-display-file-dds).

[SubfileControlModel](/reference/asna-qsys-expo/expo-model/subfile-control-model.html) and [SubfileRecordModel](/reference/asna-qsys-expo/expo-model/subfile-record-model.html) are specialized classes based on `RecordModel Class`.

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

<br>
<br>

## Properties

| Type | Name | Description | Indexer
| --- | --- | --- | --- 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CursorLocationFieldName | Gets or sets the Cursor Location Field Name | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | CursorLocationFormatName | Gets or sets the Cursor Location Format Name | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsActive | Gets a boolean value indicating that the Record is active | 

<br>
<br>

## Methods

| Type | Name | Description | Return Description 
| --- | --- | --- | --- 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [AddErrorMessage](#adderrormessagestring-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Adds an Error Message to the list of Validation errors | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [Equals](https://docs.microsoft.com/en-us/dotnet/api/system.object.equals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified object is equal to the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if the specified object is equal to the current object; otherwise, false.
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void) | [Finalize](https://docs.microsoft.com/en-us/dotnet/api/system.object.finalize)() | Allows an object to try to free resources and perform other cleanup operations before it is reclaimed by garbage collection.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | [GetHashCode](https://docs.microsoft.com/en-us/dotnet/api/system.object.gethashcode)() | Serves as the default hash function.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A hash code for the current object.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [GetMessageText](#getmessagetextstring-string-int32)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a string value with the text corresponding to the message requested. | The Message text
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean[])[]| GetOptionIndicators() | Gets a copy of the array of option indicators. | boolean array.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)| GetOptionIndicator([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets the option indicator value. | Boolean value.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)[]| GetResponseIndicators() | Gets a copy of the response indicators. | Char array.
| [Char](https://learn.microsoft.com/en-us/dotnet/api/system.char) | GetResponseIndicator([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the response indicator value. May be '0', '1' or 'X'. | Char value.
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | [GetType](https://docs.microsoft.com/en-us/dotnet/api/system.object.gettype)() | Gets the Type of the current instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | The exact runtime type of the current instance.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsAidKeyInEffect](#isaidkeyineffectaidkey-int32)([AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a boolean value indicating if the Aid Key is in effect | true if the Aid key is in effect
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsAidKeyInEffect](#isaidkeyineffectconditionalproperty-int32)([ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a boolean value indicating if the Aid Key is in effect given a conditional property | true if the Aid key is in effect
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsFalse](#isfalsestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the resulting value of the evaluation of condition using the optionIndicators. | Return true only if there is no doubt about it. If anything goes wrong, return false
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsNotFalse](#isnotfalsestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the resulting value of the evaluation of condition using the optionIndicators. | Return true only if there is no doubt about it. If anything goes wrong, return false
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsNotTrue](#isnottruestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a boolean value indicating the result of evaluation of the condition using the optionIndicators. | Return false only if there is no doubt about it. If anything goes wrong, return true
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [IsTrue](#istruestring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the resulting value of the evaluation of the condition using the optionIndicators. | false only if there is no doubt about it. If anything goes wrong, return true
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | [MemberwiseClone](https://docs.microsoft.com/en-us/dotnet/api/system.object.memberwiseclone)() | Creates a shallow copy of the current Object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A shallow copy of the current Object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ProcessErrorMessages](#processerrormessagesstring-string-conditionalproperty-conditionalproperty)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html), [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html)) | Process Error Message for a field in a record if the condition succeeds | true if error condition and error message was added to the validation error collection
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ReferenceEquals](https://docs.microsoft.com/en-us/dotnet/api/system.object.referenceequals)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the specified Object instances are the same instance.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | true if objA is the same instance as objB or if both are null; otherwise, false.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ResolveConditionalProperty](#resolveconditionalpropertystring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a string value that indicates the result of the condition in the property given as a string | The value corresponding to the condition
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | [ResolveConditionalProperty](#resolveconditionalpropertyconditionalproperty)([ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html)) | Gets a string value that indicates the result of the condition in the property given | The value corresponding to the condition
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void)| SetOptionIndicator([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Sets the option indicator value. | 
| [Void](https://docs.microsoft.com/en-us/dotnet/api/system.void)| SetResponseIndicator([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Char](https://learn.microsoft.com/en-us/dotnet/api/system.char)) | Sets the response indicator value. | 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [ToString](https://docs.microsoft.com/en-us/dotnet/api/system.object.tostring)() | Returns a string that represents the current object.<br>(Inherited from [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | A string that represents the current object.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | [WasRecordPosted](#wasrecordpostedstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a boolean value that indicates if the Record was posted | true is the Record was posted

<br>
<br>

### AddErrorMessage([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Adds an Error Message to the list of Validation errors

```cs
AddErrorMessage(String errorMessageInfo, String fieldNameID);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | errorMessageInfo | error information 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldNameID | field name ID 


<br>
<br>

### GetMessageText([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Gets a string value with the text corresponding to the message requested.

```cs
GetMessageText(String messageFileName, String messageId, Int32 maxLength);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageFileName | Message filename 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageId | Message ID 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | maxLength | Maximum chars to copy 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The Message text


<br>
<br>

### IsAidKeyInEffect([AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Gets a boolean value indicating if the Aid Key is in effect

```cs
IsAidKeyInEffect(ASNA.QSys.Expo.Model.AidKey key, ref Int32 responseIndicator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AidKey](/reference/asna-qsys-expo/expo-model/aid-key.html) | key | Aid key 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | responseIndicator | output response indicator number 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

true if the Aid key is in effect


<br>
<br>

### IsAidKeyInEffect([ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Gets a boolean value indicating if the Aid Key is in effect given a conditional property

```cs
IsAidKeyInEffect(ASNA.QSys.Expo.Model.ConditionalProperty conditionalProperty, ref Int32 responseIndicator);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | conditionalProperty | Conditional Property 
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | responseIndicator | output response indicator number 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

true if the Aid key is in effect


<br>
<br>

### IsFalse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the resulting value of the evaluation of condition using the optionIndicators.

```cs
IsFalse(String condition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Return true only if there is no doubt about it. If anything goes wrong, return false


<br>
<br>

### IsNotFalse([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the resulting value of the evaluation of condition using the optionIndicators.

```cs
IsNotFalse(String condition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Return true only if there is no doubt about it. If anything goes wrong, return false


<br>
<br>

### IsNotTrue([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets a boolean value indicating the result of evaluation of the condition using the optionIndicators.

```cs
IsNotTrue(String condition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

Return false only if there is no doubt about it. If anything goes wrong, return true


<br>
<br>

### IsTrue([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets the resulting value of the evaluation of the condition using the optionIndicators.

```cs
IsTrue(String condition);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | condition | conditional expression 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

false only if there is no doubt about it. If anything goes wrong, return true


<br>
<br>

### ProcessErrorMessages([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html), [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html))

Process Error Message for a field in a record if the condition succeeds

```cs
ProcessErrorMessages(String recordName, String fieldNameID, ASNA.QSys.Expo.Model.ConditionalProperty errorMessage, ASNA.QSys.Expo.Model.ConditionalProperty errorMessageId);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordName | name of record 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | fieldNameID | field ID 
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | errorMessage | error message 
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | errorMessageId | error message ID 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

true if error condition and error message was added to the validation error collection


<br>
<br>

### ResolveConditionalProperty([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets a string value that indicates the result of the condition in the property given as a string

```cs
ResolveConditionalProperty(String conditionalPropertyString);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | conditionalPropertyString | conditional property string 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The value corresponding to the condition


<br>
<br>

### ResolveConditionalProperty([ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html))

Gets a string value that indicates the result of the condition in the property given

```cs
ResolveConditionalProperty(ASNA.QSys.Expo.Model.ConditionalProperty conditionalProperty);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ConditionalProperty](/reference/asna-qsys-expo/expo-model/conditional-property.html) | conditionalProperty | conditional property string 

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)

The value corresponding to the condition


<br>
<br>

### WasRecordPosted([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Gets a boolean value that indicates if the Record was posted

```cs
WasRecordPosted(String recordName);
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | recordName | name of the Record to check 

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)

true is the Record was posted


<br>
<br>

## Fields

| Type | Name | Description
| --- | --- | --- 
| [AidProperty](/reference/asna-qsys-expo/expo-model/aid-property.html) | AttnKeys | Gets or sets the Attention Keys AID Property
| [AidProperty](/reference/asna-qsys-expo/expo-model/aid-property.html) | FuncKeys | Gets or sets the Function Keys AID Property

<br>
<br>

