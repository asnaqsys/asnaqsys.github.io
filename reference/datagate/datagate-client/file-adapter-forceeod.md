---
title: "FileAdapter.ForceEOD Method"
description: "Forces the end of data (EOD) for the file that the FileAdapter is working with."
last_modified_at: 2025-09-26
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll


Forces the end of data (EOD) for the file that the FileAdapter is working with.

```cs
void ForceEOD()
```

## Remarks

For print files, **ForceEOD** causes a document to start printing by first flushing the current page, then the document starts printing immediately without closing.
 
For database files, **ForceEOD** flushes any provider-specific buffers associated with the open file, releases locks, and seeks to the last record in the file.



## See Also
- [FileAdapter class](file-adapter.html)
