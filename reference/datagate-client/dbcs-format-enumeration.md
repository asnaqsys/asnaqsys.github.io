---
title: DbcsFormat Enumeration

---

The <span> **DbcsFormat** </span> enumerated constant defines values on whether shift-control characters appear internally on the IBM i. This enumeration is used by the [ Dbcs](field-type-class-dbcs-property.html) property for [FieldType](field-type-class.html) objects.

```cs
 public enum DbcsFormat;
```


## Remarks

<span>Dbcs</span> defines values in which you can select one of the choices. 
## Members



| Member | Description | Value |
| ---- | ---- | ---- |
| Either | Double byte (with shift-control) or single byte. | 4 |
| Graphic | Double byte only (no shift-control). | 5 |
| None | Shift-control characters do not appear. | 0 |
| Only | Double byte only (with shift-control). | 3 |
| Open | Mixed single byte/double byte (with shift-control). | 2 |



## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
## See Also


[AdgDataSet Class](adg-dataset-class.html)
        <br />
[Dbcs Property](field-type-class-dbcs-property.html)
        <br />
[FieldType Class](field-type-class.html)
        <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

