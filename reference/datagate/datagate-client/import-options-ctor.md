---
title: "ImportOptions Constructor"
description: "Initializes a new instance of the class with the specified target member, source path, clear member flag, and use target connection flag."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class with the specified target member, source path, clear member flag, and use target connection flag.

```cs
ImportOptions(IMember, String, Boolean, Boolean)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | target | The target member where the data will be imported.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | source | The source path from where the data will be imported.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bClearMember | A flag indicating whether the target member should be cleared before the import.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | bUseTargetConnection | A flag indicating whether the target connection should be used for the import.

## See Also
- [ImportOptions class](import-options.html)
