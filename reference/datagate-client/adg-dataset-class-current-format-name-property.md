---
title: AdgDataSet.CurrentFormatName Property

---

The current format name of the **AdgDataSet** .

```cs
 public string CurrentFormatName { get; }
```


## Property Value

**String** . The format name of the record contained by the [ActiveRow](adg-dataset-class-active-row-property.html) property.
## Remarks

**CurrentFormatName** is related to **ActiveRow** , in that the format of the record contained by **ActiveRow** is identified by the value of **CurrentFormatName** . Upon construction, **ActiveRow** has no value and neither does **CurrentFormatName** . Reading the value of **CurrentFormatName** when **ActiveRow** has no value will result in a dgException being thrown, with an Error property value of dgEINVARG. 
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro
## See Also


[AdgDataSet Class](adg-dataset-class.html)
      <br />
[AdgDataSet Members](adg-dataset-members.html)
      <br />
[ActiveRow Property](adg-dataset-class-active-row-property.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

