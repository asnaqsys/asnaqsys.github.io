---
title: FileAdapter.DeleteCurrent Method

Id: dcsFileAdapterClassDeleteCurrentMethod
TocParent: dcsFileAdapterMethods
TocOrder: 5

keywords: DeleteCurrent method
keywords: FileAdapter.DeleteCurrent method
keywords: database files, delete current record in
keywords: files, delete current record in
keywords: records, delete current
keywords: delete current records in a file
keywords: how to, delete current record in a file

---

Deletes the current record associated with an open file.
<pre class="prettyprint">         <span class="lang">[C#]</span>
 **public void DeleteCurrent()** ;</pre>
<pre class="prettyprint">         <span class="lang">[Visual Basic] </span>
 **Public Sub DeleteCurrent()** 
      </pre>
<pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegSr DeleteCurrent Access(*Public)** 
      </pre>

## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| NullReferenceException | **FileAdapter** open method has not been called (file is not open). |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />



| Value of 							<br /> 							dgException.Error | Condition |
| ---- | ---- |
| dgEaNOCURR | There is not a current record associated with the file. If the file is open for "network blocking", the current record position on the server is unknown. |
| dgEsAS400ERROR | The database server encountered a system error. Details may be available via the SystemError and Text fields of dgException. |



## Remarks

The current record of an open file is marked as deleted by **DeleteCurrent** . After the delete, any lock on the record is released. The file should be opened with the [AccessMode](file-adapter-class-access-mode-property.html) property set to a value including the [AccessMode.Delete](access-mode-enumeration.html) flag in order to permit delete access to the file.
## Examples

<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read | AccessMode.Delete;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error opening file! " + dgEx.Message, "Error");
      //Exit procedure or end application here.
  }

  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default);

  /* We retrieve the record for customer number 7800... */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 7800;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl);
      /*... and delete it! */
      dbFile.DeleteCurrent();
  }
  catch(dgException dgEx)
  {
      MessageBox.Show("Error deleting the record: " + dgEx.Message,
      dgEx.Error.ToString());
  }

  dbFile.Close();
  db.Close();</pre>
<pre class="OH_CodeSnippetContainerCode">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read Or AccessMode.Delete

  Dim myDS As AdgDataSet = Nothing
  Try
      dbFile.OpenNewAdgDataSet(myDS)
  Catch dgEx As dgException
      MsgBox("Error opening file! " + dgEx.Message, MsgBoxStyle.OKOnly, "Error")
      'Exit procedure or end application here.
  End Try

  dbFile.ReadSequential(myDS, ReadSequentialMode.First, LockRequest.Default)

  ' We retrieve the record for customer number 7800... 
  Dim keyTbl As AdgKeyTable = myDS.NewKeyTable("RCMMASTL1")
  keyTbl.Row.Item("CMCUSTNO") = 7800
  Try
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Default, keyTbl)
      '... and delete it! 
      dbFile.DeleteCurrent()
  Catch dgEx As dgException
      MsgBox("Error deleting the record: " + dgEx.Message, MsgBoxStyle.OKOnly, "Error")
  End Try

  dbFile.Close()
  db.Close()</pre>

## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Class Members](file-adapter-members.html)
      <br />
[AccessMode Property](file-adapter-class-access-mode-property.html)
      <br />
[AccessMode Enumeration](access-mode-enumeration.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

