---
title: DataTypes Enumeration

---

The <span> **DataTypes** </span> enumerated constant defines values on the types of fields available. This enumeration is used by the [DataType](field-type-class-data-type-property.html) property for [FieldType](field-type-class.html) objects.

```cs
 public enum DataTypes;
```


## Remarks

Packed, zoned and binary types are numeric fields containing decimal numbers which are expressed in digits and decimals. Float and integer types are defined in bytes.

<span> **DataTypes** </span> defines values in which you can select one of the choices. 
## Members



| Member | Description | Value |
| ---- | ---- | ---- |
| Binary | Field is binary. | 4 |
| Boolean | Field is a Boolean, true/false. | 15 |
| Char | Field is character. | 1 |
| Date | Field is a date. | 7 |
| DBCS | Field is a double byte character field. | 12 |
| DontCare | Field is of any type. | 14 |
| Float | Field is float. | 5 |
| Hex | Field is hexadecimal. | 10 |
| Integer | Field is an integer. | 6 |
| MaxType | The total number of valid values for the Type property. | 17 |
| NoType | Field has no type. | 0 |
| Packed | Field is packed. | 2 |
| Print | Field is a print field. | 11 |
| Structured | Field is structured. | 13 |
| Time | Field is time. | 8 |
| Timestamp | Field is a timestamp. | 9 |
| Unicode | Field is a Unicode data type. | 16 |
| Zoned | Field is packed. | 3 |



## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
## See Also


[FieldType Class](field-type-class.html)
      <br />
[DataType Property](field-type-class-data-type-property.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

