---
title: FieldType.NewInteger Method

---

Creates a new integer [ FieldType](field-type-class.html).

## Parameters



 *length* 

: Integer.  The length of the field in bytes, either 2 or 4.
					


## Exceptions

**System.ArgumentException** . Thrown if *length* is not equal to 2 or 4.
## Remarks

**NewInteger** constructs a **FieldType** object that represents a DataGate integer field. Integer fields contain integer numeric data stored in unsigned binary format in 2 or 4 bytes. The upper limit of 2-byte integer field values is 65535 and the upper limit of 4-byte integer field values is 4294967295.
## Requirements

**Namespace:** [ASNA.DataGate.Common](datagate-common-namespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FieldType Class](field-type-class.html)
      <br />
[FieldType Class Members](field-type-members.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)

