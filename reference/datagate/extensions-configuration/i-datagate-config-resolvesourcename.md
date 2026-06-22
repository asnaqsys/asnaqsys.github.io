---
title: "IDataGateConfig interface.ResolveSourceName Method"
description: "Resolves a configured SourceProfile with behavior similar to the DatabaseName.ToSourceProfile methods for traditional database names."
---

## Definition

**Namespace:** ASNA.Extensions.Configuration  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Resolves a configured SourceProfile with behavior similar to the DatabaseName.ToSourceProfile methods for traditional database names.

<a id="sourceprofile-resolvesourcename-string-name"></a>
## SourceProfile ResolveSourceName(string name)

Resolves a configured SourceProfile with behavior similar to the DatabaseName.ToSourceProfile methods for traditional database names.

#### Remarks
This method is used to resolve a SourceProfile from its name. If the name is not found, it throws a NoDbNameException.

```cs
SourceProfile ResolveSourceName(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the source to resolve.

#### Returns

| Type | Description
| --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | The resolved SourceProfile.

## See Also
- [IDataGateConfig interface class](i-datagate-config.html)
