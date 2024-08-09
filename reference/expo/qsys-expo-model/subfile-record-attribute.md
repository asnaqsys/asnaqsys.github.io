---
title: "SubfileRecordAttribute class  | QSYS API Reference Guide"
description: "Defines Subfile Record Attribute on a type "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines Subfile Record Attribute on a type

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Attribute](https://docs.microsoft.com/en-us/dotnet/api/system.attribute) --> [BaseRecordAttribute](/reference/expo/qsys-expo-model/base-record-attribute.html)
<br>
<br>

## Remarks

The `SubfileRecordAttribute` class is a specialized class derived from [RecordAttribute class](/reference/expo/qsys-expo-model/base-record-attribute.html) that provides meta-data to express in the Model [Subfile Displayfile Record](https://www.ibm.com/docs/en/i/7.4?topic=80-sfl-subfile-keyword-display-files) [DDS](https://www.ibm.com/docs/en/i/7.4?topic=dds-display-files) keywords.

The following excerpt of code describes to the `SFL1` Subfile model, the attribute `NextChanged` corresponding to the [legacy SFLNXTCHG DDS keyword](https://www.ibm.com/docs/en/i/7.4?topic=80-sflnxtchg-subfile-next-changed-keyword-display-files).

```cs
[
    SubfileRecord(NextChanged = "14")
]
public class SFL1_Model : SubfileRecordModel
{
    [Char(1, Protect = "*True")]
    public string SFCOLOR { get; set; }

    [Values(typeof(Decimal),"00","02","03","05","07","09","10","11")]
    [Dec(2, 0)]
    public decimal SFSEL { get; set; }
    .
    .
    .
}
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsMessageSubfile | Sets or gets a boolean value to indicate that the Subfile record is the Message Subfile. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NextChanged | Sets or gets a conditional indicator expression that determines if the record should be set as changed, to force the get-next-changed operation to succeed (SFLNXTCHG). Defaults to null |

## Methods

| Signature | Description |
| --- | --- |
| [GetFrom](#subfilerecordattribute-getfromtype-type)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Gets the SubfileRecordAttribute from the Custom attributes on a type.

### SubfileRecordAttribute GetFrom([Type type](https://docs.microsoft.com/en-us/dotnet/api/system.type))

Gets the SubfileRecordAttribute from the Custom attributes on a type.

```cs
SubfileRecordAttribute GetFrom(Type type)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type) | type | The object Type.

#### Returns

| Type | Description
| --- | ---
| [SubfileRecordAttribute](/reference/expo/qsys-expo-model/subfile-record-attribute.html) | The subfile record attribute.
