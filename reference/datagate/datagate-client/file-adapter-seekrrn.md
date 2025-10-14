---
title: "FileAdapter.SeekRRN Method"
description: "Positions the file pointer at the record with a specified relative record number (RRN)."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Positions the file pointer at the record with the specified relative record number (RRN) in the file that the FileAdapter is working with.

void SeekRRN(SeekMode mode, long RRN)


#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [SeekMode](/reference/datagate/datagate-common/seek-mode.html) | mode | The SeekMode to use when seeking the record. |
| [Int64](https://docs.microsoft.com/en-us/dotnet/api/system.int64) | RRN | The relative record number of the record to seek. |


## Remarks

**SeekRRN** positions the file pointer to a particular record using the specified relative record number (_RRN_) and _mode_ as a point of reference.  The record pointed to by this method will be either relative to the _RRN_ parameter (_mode_ **Equal**, **Greater**, **SetGT**, **SetGE**, or **SetLL**); or, relative to the absolute position in the file (_mode_ **First** or **Last**).  If the record sought does not exist in the file, the method throws dgException with an Error property value of dgEaNOTFND.
 
When **SeekMode.SetLL** or **SeekMode.SetGT** values for _mode_ are specified and the record sought is not found, the file pointer is placed at the end of the file and then dgException is thrown.
 
Calling this method cancels "range mode".  A prior successful call to `ReadRange`or `SeekRange` places the **FileAdapter** in range mode, in which only records with keys in a specified range are accessed.  This method cancels the restriction.


## See Also
- [FileAdapter class](file-adapter.html)
