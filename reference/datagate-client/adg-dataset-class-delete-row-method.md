---
title: AdgDataSet.DeleteRow Method

Id: dcsAdgDataSetClassDeleteRowMethod
TocParent: dcsAdgDataSetMethods
TocOrder: 1

keywords: DeleteRow method
keywords: AdgDataSet.DeleteRow method

keywords: mark rows as deleted
keywords: rows, mark as deleted
keywords: how to, mark rows as deleted
keywords: tables, mark rows as deleted

---

Mark a DataRow in the **AdgDataSet** as deleted.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void DeleteRow(
   string strFormat,
   int rrn
);** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub DeleteRow( _
   ByVal strFormat As String _
   ByVal rrn As Integer
)** 
      </pre>
<pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr DeleteRow Access(*Public)
   DclSrParm strFormat Type(*String)
   DclSrParm rrn Type(*Integer) Len(4)** 
      </pre>

## Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>The name of the format containing the row to delete. </dd>
        <dt>
 *rrn* 
        </dt>
        <dd>The index of the row to delete in the Rows collection of the table.
							</dd>
</dl>

## Exceptions

**ASNA.DataGate.Common.dgException** is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| NullReferenceException | Can occur if *strFormat* specifies an invalid format name, or *rrn* specifies an invalid index in the DataRowCollection. |



## Remarks

**DeleteRow** marks the DataRow object specified by *rrn* as deleted in the format table specified by *strFormat* . Upon return, the [ActiveRow Property](adg-dataset-class-active-row-property.html) of the **AdgDataSet** is set to null and the RowState of the DataRow is RowDeleted.

The *rrn* parameter is a zero-relative index referring to a DataRow object contained in the Rows collection of the DataTable corresponding to the *strFormat* parameter. The Rows collection and its containing DataTable object is accessible via the [ GetFormatTable](adg-dataset-class-get-format-table-method.html) method.
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgDataSet Class](adg-dataset-class.html)
      <br />
[AdgDataSet Class Members](adg-dataset-members.html)
      <br />
[ActiveRow Property](adg-dataset-class-active-row-property.html)
      <br />
[GetFormatTable Method](adg-dataset-class-get-format-table-method.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

