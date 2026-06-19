---
title: "As400Program.GetParmByName Method"
description: "Gets the parameter with the specified name."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the parameter with the specified name.

## Overloads

| Signature | Description |
| --- | --- |
| [GetParmByName](#progparm-getparmbyname-string-name)(ProgParm GetParmByName(string name)) | Gets the parameter with the specified name. |
| [GetParmByName](#progparm-getparmbyname-string-name-2)(ProgParm GetParmByName(string name)) | Gets the parameter with the specified name from the specified list of parameters. |

<a id="progparm-getparmbyname-string-name"></a>
## ProgParm GetParmByName(string name)

Gets the parameter with the specified name.

#### Remarks
This method returns the parameter with the specified name in the ASNA DataGate client. The name comparison is case-insensitive. If no such parameter exists, it returns null.

```cs
ProgParm GetParmByName(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the parameter.

#### Returns

| Type | Description
| --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | The parameter with the specified name, or null if no such parameter exists.

<a id="progparm-getparmbyname-string-name-2"></a>
## ProgParm GetParmByName(string name)

Gets the parameter with the specified name from the specified list of parameters.

#### Remarks
This method returns the parameter with the specified name from the specified list of parameters in the ASNA DataGate client. The name comparison is case-insensitive. If no such parameter exists, it returns null.

```cs
ProgParm GetParmByName(string name)
```

## See Also
- [As400Program class](as400-program.html)
