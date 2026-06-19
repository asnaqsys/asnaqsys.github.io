---
title: "ILibraryList interface.AddEntry Method"
description: "Adds a library to the library list at a specified position."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Adds a library to the library list at a specified position.

<a id="void-addentry-string-path-liblposition-pos-string-reflib"></a>
## void AddEntry(string path, LiblPosition pos, string refLib)

Adds a library to the library list at a specified position.

```cs
void AddEntry(string path, LiblPosition pos, string refLib)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The path of the library to add.
| [LiblPosition](/reference/datagate/datagate-client/libl-position.html) | pos | The position to add the library at.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | refLib | Optional reference library.

## See Also
- [ILibraryList interface class](i-library-list.html)
