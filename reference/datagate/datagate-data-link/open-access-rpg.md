---
title: "OpenAccessRpg Delegate"
description: "Represents a method that handles I/O operations with an Open Access RPG program."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Represents a method that handles I/O operations with an Open Access RPG program.

```csharp
public delegate void OpenAccessRpg(IOpenAccessReader rdr, IOpenAccessWriter wrt)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [IOpenAccessReader](/reference/datagate/datagate-data-link/i-open-access-reader.html) | rdr | The reader to read data from the RPG program. |
| [IOpenAccessWriter](/reference/datagate/datagate-data-link/i-open-access-writer.html) | wrt | The writer to write data to the RPG program. |

## Remarks
Use this delegate for callbacks that manage reading from and writing to an Open Access RPG program via the provided channel interfaces.

## See Also
- [IOpenAccessReader](/reference/datagate/datagate-data-link/i-open-access-reader.html)
- [IOpenAccessWriter](/reference/datagate/datagate-data-link/i-open-access-writer.html)
