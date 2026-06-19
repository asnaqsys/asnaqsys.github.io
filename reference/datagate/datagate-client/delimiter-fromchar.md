---
title: "Delimiter.FromChar Method"
description: "Creates a new instance from a given character."
---

## Definition

**Namespace:** ASNA.DataGate.Client.CopyData  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new instance from a given character.

<a id="delimiter-fromchar-char-ch"></a>
## Delimiter FromChar(char ch)

Creates a new  instance from a given character.

#### Remarks
This method creates a new  instance and sets its  property to the given character.If the given character is '\0', the created  instance will represent no delimiter (IsStarNone will be true).

```cs
Delimiter FromChar(char ch)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char](https://docs.microsoft.com/en-us/dotnet/api/system.char) | ch | The character to create a  from.

#### Returns

| Type | Description
| --- | ---
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | A new  instance with its value set to the given character.

## See Also
- [Delimiter class](delimiter.html)
