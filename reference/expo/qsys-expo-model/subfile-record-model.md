---
title: "SubfileRecordModel class      | QSYS API Reference Guide"
description: "Defines the SubfileRecordModel class "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines the SubfileRecordModel class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [RecordModel](/reference/expo/qsys-expo-model/record-model.html)
<br>
<br>

## Remarks

[SubfileRecordModel](/reference/expo/qsys-expo-model/subfile-record-model.html) is a specialized class based on [RecordModel](/reference/expo/qsys-expo-model/record-model.html).

The following excerpt shows the `MSGSF` `SubfileRecordModel class`, which describes the fact that this Subfile Record is the [Message Subfile](https://www.ibm.com/docs/en/i/7.4?topic=type-example-message-subfile-using-dds), which contains three fields: `@MSGKY, @PGMQ and MessageText`.

```cs
[
    SubfileRecord(IsMessageSubfile = true)
]
public class MSGSF_Model : SubfileRecordModel
{
    [Char(4, Alias = "@MSGKY")]
    public string aMSGKY { get; private set; }

    [Char(10, Alias = "@PGMQ")]
    public string aPGMQ { get; private set; }

    [Char(128)]
    public string MessageText { get; private set; }

}
```

>Notes: 

1. SubfileRecordModel classes are expressed in the Model as [nested C# classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/nested-types) inside their corresponding [SubfileControl records](/reference/expo/qsys-expo-model/subfile-control-model.html).

2. The field `MessageText` is added to the Subfile by the Migration process, to implement the assumed place (by IBM i design) where messages are displayed.

## Constructors

| Name | Description |
| --- | --- |
| [SubfileRecordModel](#subfilerecordmodelint32)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Initializes a new instance of the class SubfileRecordModel to the row-number initial value

### SubfileRecordModel([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Initializes a new instance of the class SubfileRecordModel to the row-number initial value

```cs
SubfileRecordModel(Int32)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | rowNumber | Initial row-number

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | _RecordNumber | Gets or sets the Record Number |
