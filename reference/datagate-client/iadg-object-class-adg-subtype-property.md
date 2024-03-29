---
title: IAdgObject.AdgSubType Property

---

**AdgSubType** identifies the secondary type of the database object represented by **IAdgObject** . 

```cs
 public AdgSubTypes AdgSubType { get; }
```

Property Value <p> [AdgSubTypes](adg-subtypes-enumeration.html). ReadOnly. A sub-classification of the database object, such as Join, Physical, etc. 
<br />

## Exceptions

<br />



| ExceptionType | Condition |
| ---- | ---- |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEINVARG | The property is not available for this object type or the object name does not reference an existing database object. |
| dgEsAS400ERROR | The database provider encountered a system-level error. Details provided in the **dgException.Message** property. |
| dgEmNOTFND | The path name specified when the **IAdgObject** instance was created does not reference an existing database object. |



## Remarks

**AdgSubType** is a secondary type which may be assigned by the database provider to further classify the primary type (see [ AdgObjectType](iadg-object-class-adg-object-type-property.html)) of the database object represented by **IAdgObject** . The following table lists the possible values of **AdgSubType** for the various values of **AdgObjectType** .
<br />



| Value of AdgObjectType (primary type) | Possible values for AdgSubTypes<br /> 							 (secondary type) |
| ---- | ---- |
| Directory | Local |
| File | Join, Merge, Physical, SqlLogical, Simple (logical), OlePrint, NetPrint, Unknown |
| Member |



<table> <tbody> <tr> <td colspan="1" rowspan="1"> <p>Join, Merge, Physical, SqlLogical, Simple (logical), Unknown
</td>
            </tr>
          </tbody>
</table>

<br />

When the database provider does not support, or cannot readily determine the secondary type for a particular object, the **Unknown** value is assigned to **AdgSubType** . If **AdgSubType** is **Unknown** for a file object, the secondary type information can be obtained via the file definition regardless of the database provider (see [ IFileObject.WriteDefinition](ifile-object-class-write-definition-method.html) or [ IFileObject.WriteXml](ifile-object-class-write-definition-method.html)).

**IAdgObject** queries the database provider for certain object attributes such as **AdgSubType** only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values of **IAdgObject** .
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[IAdgObject Class](iadg-object-class.html)
      <br />
[AdgObjectType Property](iadg-object-class-adg-object-type-property.html)
      <br />
[AdgSubType Enumeration](adg-subtypes-enumeration.html)
      <br />
[IFileObject Class](ifile-object-class.html)
      <br />
[WriteDefinition Method](ifile-object-class-write-definition-method.html)
      <br />
[WriteXml Methods](ifile-object-class-write-definition-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

