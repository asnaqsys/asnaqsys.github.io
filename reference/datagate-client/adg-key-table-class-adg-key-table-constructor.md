---
title: AdgKeyTable(System.Data.DataTable)

Id: dcsAdgKeyTableClassAdgKeyTableConstructor
TocParent: dcsAdgKeyTableAdgKeyTableConstructorsMain
TocOrder: 0

---

This member supports DCS infrastructure and is not intended to be used directly from your code .
<pre>
        <span class="lang">[C#]
</span> **public AdgKeyTable(
   System.Data.DataTable keyTable
);** 
      </pre>
<pre>
        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal keyTable As System.Data.DataTable _
)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)
   DclSrParm keyTable Type(System.Data.DataTable)** 
      </pre>

## Parameters

<dl>
        <dt>
 *keyTable* 
        </dt>
        <dd>System.Data.DataTable. 
						Initializes a key.
					</dd>
</dl>

## Remarks

**NOTE:** It is <u>not</u> recommended to use this constructor to construct valid **AdgKeyTable** objects. New **AdgKeyTable** instances are available to the application via the [ AdgDataSet.NewKeyTable](adg-dataset-class-new-key-table-methods.html) method. 
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgDataSet.NewKeyTable Method](adg-dataset-class-new-key-table-methods.html)
      <br />
[AdgKeyTable Class](adg-key-table-class.html)
      <br />
[AdgKeyTable Class Members](adg-key-table-members.html)
      <br />System.Data.DataTable
      <br />[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

