---
title: "IFileObject interface.InspectFile Method"
description: "Inspects the file."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Inspects the file.

<a id="void-inspectfile-inspectfileparts-parts-inspectfileoutput-output-int32-errorcount-adgobserver-observer"></a>
## void InspectFile(InspectFileParts parts, InspectFileOutput output, Int32& ErrorCount, AdgObserver observer)

Inspects the file.

```cs
void InspectFile(InspectFileParts parts, InspectFileOutput output, Int32& ErrorCount, AdgObserver observer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [InspectFileParts](/reference/datagate/datagate-common/inspect-file-parts.html) | parts | The parts of the file to inspect.
| [InspectFileOutput](/reference/datagate/datagate-common/inspect-file-output.html) | output | The output of the inspection.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ErrorCount | The number of errors found during the inspection.
| [AdgObserver](/reference/datagate/datagate-client/adg-observer.html) | observer | The observer to use during the inspection.

## See Also
- [IFileObject interface class](i-file-object.html)
