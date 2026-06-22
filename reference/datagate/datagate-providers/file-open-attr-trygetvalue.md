---
title: "FileOpenAttr.TryGetValue Method"
description: "Gets the value associated with the specified key."
---

## Definition

**Namespace:** ASNA.DataGate.Providers  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the value associated with the specified key.

<a id="bool-trygetvalue-string-key-object-value"></a>
## bool TryGetValue(string key, Object& value)

Gets the value associated with the specified key.

```cs
bool TryGetValue(string key, Object& value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | key | The key of the value to get.
| [Object&](https://docs.microsoft.com/en-us/dotnet/api/system.object) | value | When this method returns, contains the value associated with the specified key, if the key is found; otherwise, the default value for the type of the value parameter.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the FileOpenAttr contains an element with the specified key; otherwise, false.

## See Also
- [FileOpenAttr class](file-open-attr.html)
