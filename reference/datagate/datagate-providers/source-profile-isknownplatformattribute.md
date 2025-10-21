---
title: "SourceProfile.IsKnownPlatformAttribute Method"
description: "Determines whether the provided platform attribute is a known platform attribute."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Determines whether the provided platform attribute is a known platform attribute.

```cs
bool IsKnownPlatformAttribute(string platformAttr)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | platformAttr | The platform attribute to check. |

## Remarks
This method is used to validate that the platform attribute provided is one that the system recognizes and can handle.

## See Also
- [SourceProfile class](source-profile.html)
