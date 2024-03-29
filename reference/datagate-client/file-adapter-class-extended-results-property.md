---
title: FileAdapter.ExtendedResults Property

---

Specialized collection of status information associated with the file.

```cs
 public Hashtable ExtendedResults { get; }
```


## Property Value

Read-only. System.Collections.Hashtable. A set of properties' values, keyed by name, associated with specialized DataGate files. 
## Remarks

Properties associated with specialized files will be found in the **ExtendedResults** collection. Items in the collection are keyed by string values identifying them.

DataGate OLE print files, when written to, communicate information about the document being printed through ExtendedResults. The following table summarizes the information available for open OLE print files, after a record has been added to the file.
<br />



| Property Key Name | Property Value |
| ---- | ---- |
| CursorY | Integer. The position that the printer is from the top of the page. Print Units are measured in 1/100th of a millimeter.  - To get the measurement in millimeters, divide by 100. - To get the measurement in centimeters, divide by 1,000. - To get the measurement in inches, divide by 2,540. |
| PageLength | Integer. The total page length based on the page orientation selected. Print Units are measured in 1/100th of a millimeter.  - To get the measurement in millimeters, divide by 100. - To get the measurement in centimeters, divide by 1,000. - To get the measurement in inches, divide by 2,540. |
| PageWidth | Integer. The total page width based upon the page orientation selected. Print Units are measured in 1/100th of a millimeter.  - To get the measurement in millimeters, divide by 100. - To get the measurement in centimeters, divide by 1,000. - To get the measurement in inches, divide by 2,540. |



## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[FileAdapter Class](file-adapter-class.html)
      <br />
[FileAdapter Members](file-adapter-members.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

