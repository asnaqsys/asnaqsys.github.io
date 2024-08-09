---
title: "SubfileControlModel class     | QSYS API Reference Guide"
description: "Defines the SubfileControlModel class "
last_modified_at: 2024-08-09T17:26:04Z
---

Defines the SubfileControlModel class

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [RecordModel](/reference/expo/qsys-expo-model/record-model.html)
<br>
<br>

## Remarks

The `SubfileControlModel` class is a specialized class derived from [RecordModel](/reference/expo/qsys-expo-model/record-model.html) 

This class implements in the Model, an instance of [Subfile Control Displayfile Record](https://www.ibm.com/docs/en/i/7.4?topic=80-sflctl-subfile-control-keyword-display-files) [DDS](https://www.ibm.com/docs/en/i/7.4?topic=dds-display-files) concept.

As the name implies, `SubfileControl` (or controller), serves as the abstraction to describe the Subfile record's behaviour it controls.  

The Subfile is expressed as a [nested class](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/nested-types) in the `SubfileControlModel` derived class.

For example, the following excerpt shows how Subfile Controller `SFLC` is declared with its Subfile `SFL1`.

As any Record, the class declares and describes the attributes of the fields in the Record and Subfile record template.

```cs
public class SFLC_Model : SubfileControlModel
{
    public List<SFL1_Model> SFL1 { get; set; } = new List<SFL1_Model>();

    [Char(10, OutputData=false)]
    public string SETNAME { get; set; }

    public class SFL1_Model : SubfileRecordModel
    {
        [Char(1, Protect = "*True")]
        public string SFCOLOR { get; set; }

        [Values(typeof(Decimal),"00","02","03","05","07","09","10","11")]
        [Dec(2, 0)]
        public decimal SFSEL { get; set; }

        [Dec(6, 0)]
        public decimal SFCUSTNO { get; private set; } // CUSTOMER NUMBER

        [Char(40)]
        public string SFNAME1 { get; private set; }

        [Char(25)]
        public string SFCSZ { get; private set; } // CITY-STATE-ZIP

    }
}
```

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | CursorRecordNumber | Gets or sets the CursorRecordNumber |
