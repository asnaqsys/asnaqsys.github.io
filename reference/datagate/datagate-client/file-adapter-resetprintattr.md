---
title: "FileAdapter.ResetPrintAttr Method"
description: "Resets the print attributes for the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll


Resets the print attributes for the file that the FileAdapter is working with.

```cs
void ResetPrintAttr()
```

## Remarks

**ResetPrintAttr** completes the printer job associated with the open print file and begins a new printer job with new printer job properties as specified by the _**docName**_ and _**attr**_parameters.  The [ForceEOD](./file-adapter-forceeod.html) method provides similar printer job functionality for print files but does not change the job name or device attributes.

The **_attr_** parameter refers to an instance of [ASNA.DataGate.Providers.PrintDevAttr](/reference/datagate/datagate-providers/print-dev-attr.html) object specified when the file is opened.  For example, the program’s print operation can print several documents using one setting for margins (set via the **PrintFileOpenAttr.DevAttr** property), then change the margins before printing the next set of documents (via the **ResetPrintAttr** method).

The **_docName_** parameter allows you to associate a new name with the new printer job.  This name can be used by the operating system to identify a job in a printer queue.  If **_docName_** is _null_ , the next printer job will have the same name as the current printer job.


## See Also
- [FileAdapter class](file-adapter.html)
