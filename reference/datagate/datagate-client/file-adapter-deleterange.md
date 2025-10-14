---
title: "FileAdapter.DeleteRange Method"
description: "Deletes a range of records from the file that the FileAdapter is working with."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Deletes a range of records from the file that the FileAdapter is working with.

```cs
public void DeleteRange(AdgKeyTable firstKey, RangeFirst rangeFirst,
                        AdgKeyTable lastKey, RangeLast rangeLast)
```                        

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | firstKey | The AdgKeyTable containing the key of the first record in the range to delete. |
| [RangeFirst](/reference/datagate/datagate-common/range-first.html) | rangeFirst | The RangeFirst value indicating whether to include the first record in the deletion. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | lastKey | The AdgKeyTable containing the key of the last record in the range to delete. |
| [RangeLast](/reference/datagate/datagate-common/range-last.html) | rangeLast | The RangeLast value indicating whether to include the last record in the deletion. |

## Remarks

**DeleteRange** positions the file to the range of records specified and deletes those records. This operation is equivalent to a client-side program implemented as follows:
 - Seek to the position specified by the _firstKey_ and _rangeFirst_ parameters.
 - If the record is found, delete it.
 - Select the next sequential record as the current record.
 - If the key of the current record has a value less than the value specified by the _lastKey_ and _rangeLast_ parameters, loop to step 2.

The value added by **DeleteRange** to the above program is that all processing is performed by the database provider on the server side of the connection, this increase performance.

Use the **DeleteRange** method in conjunction with the `ReadRange` method to optimize processing and to enhance client/server performance with all supported database engines with dynamic Network Blocking.


## See Also
- [FileAdapter class](file-adapter.html)
