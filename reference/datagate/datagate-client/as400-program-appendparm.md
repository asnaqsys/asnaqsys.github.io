---
title: "As400Program.AppendParm Method"
description: "Appends a parameter to the program."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Appends a parameter to the program.

## Overloads

| Signature | Description |
| --- | --- |
| [AppendParm](#void-appendparm-progparm-parameter)(void AppendParm(ProgParm parameter)) | Appends a parameter to the program. |
| [AppendParm](#void-appendparm-progparm-parameter-2)(void AppendParm(ProgParm parameter)) | Appends a parameter to the specified list of parameters. |

<a id="void-appendparm-progparm-parameter"></a>
## void AppendParm(ProgParm parameter)

Appends a parameter to the program.

#### Remarks
This method appends a parameter to the program in the ASNA DataGate client. It checks if the provided parameter is null, and if so, throws an ArgumentNullException. It then adds the parameter to the list of parameters for the program.

```cs
void AppendParm(ProgParm parameter)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParm](/reference/datagate/datagate-data-link/prog-parm.html) | parameter | The parameter to append.

<a id="void-appendparm-progparm-parameter-2"></a>
## void AppendParm(ProgParm parameter)

Appends a parameter to the specified list of parameters.

#### Remarks
This method appends a parameter to the specified list of parameters in the ASNA DataGate client. It checks if the provided parameter is named, and if not, throws an ArgumentException. It also checks if a parameter with the same name already exists in the list, and if so, throws an ArgumentException. It then adds the parameter to the list.

```cs
void AppendParm(ProgParm parameter)
```

## See Also
- [As400Program class](as400-program.html)
