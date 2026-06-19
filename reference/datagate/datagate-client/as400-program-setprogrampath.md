---
title: "As400Program.SetProgramPath Method"
description: "Sets the path of the program to be executed."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Sets the path of the program to be executed.

<a id="void-setprogrampath-string-value"></a>
## void SetProgramPath(string value)

Sets the path of the program to be executed.

#### Remarks
This method sets the program path for the ASNA DataGate client. The provided path is converted to upper case invariant culture before being set.

```cs
void SetProgramPath(string value)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | value | The path of the program.

## See Also
- [As400Program class](as400-program.html)
