---
title: AdgDataSet.PrepareRow(string, System.Data.DataRow)

Id: dcsAdgDataSetClassPrepareRowMethod3
TocParent: dcsAdgDataSetClassPrepareRowMethodMain
TocOrder: 2

keywords: DataRow objects, prepare existing object to be inserted into DataTable
keywords: how to, prepare existing DataRow object for insertion into DataTable

---

Establish an existing **DataRow** object as the currently prepared row, for subsequently adding it to the **AdgDataSet** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void PrepareRow(
   string strFormat,
   DataRow row
);** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub PrepareRow( _
   ByVal strFormat As String, _
   ByVal row As DataRow
)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr PrepareRow Access(*Public)
   DclSrParm strFormat Type(*String)
   DclSrParm row Type(DataRow)** 
      </pre>

## Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>A string identifying the format corresponding to the **DataTable**  
						to which the **DataRow**  can be added. </dd>
        <dt>
 *row* 
        </dt>
        <dd>A **DataRow**  object to be set as the currently prepared row.</dd>
</dl>

## Exceptions

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| NullReferenceException | Can occur if *strFormat* specifies an invalid format name. |



## Remarks

Adding **DataRow** objects to **AdgDataSet** is generally a three step process. In the first step a **DataRow** object is established as the "prepared row". Secondly, fields represented in the **DataRow** columns are set to appropriate values. Finally, the **DataRow** is added to the **DataTable** .

This version of **PrepareRow** stages a pre-existing **DataRow** object, rather than creating a new one. Since a valid **DataRow** is not created, care should be taken to ensure that *row* is a valid **DataRow** object for the record format corresponding to *strFormat* . A valid **DataRow** may be obtained from one of the other versions of **PrepareRow** or from .NET framework methods in the **System.Data** namespace.

The **DataRow** object returned by this method is not a member of the **DataTable** corresponding to the format specified, until it has been explicitly inserted via [ AddPreparedRowAndSetActive](adg-dataset-class-add-prepared-row-and-set-active-method.html), [ FileAdapter.AddRecord](file-adapter-class-add-record-method.html), or a method of **DataTable** .

Note that **PrepareRow** performs no validation of the *strFormat* parameter.
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgDataSet Class](adg-dataset-class.html)
      <br />
[AdgDataSet Class Members](adg-dataset-members.html)
      <br />
      [AddPreparedRowAndSetActive 
					Method](adg-dataset-class-add-prepared-row-and-set-active-method.html)
      <br />
[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Class Members](file-adapter-members.html)
      <br />
[AddRecord Method](file-adapter-class-add-record-method.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](datagate-client-namespace.html)

