---
title: "EscapeProgram.SendErrorMessage Method"
description: "Sends an error message and sets error indicators."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Sends an error message and sets the specified error indicators.

## Overloads

| Signature | Description |
| --- | --- |
| [SendErrorMessage](#void-senderrormessagestringintarray)(string, int[]) |  Sends an error message using default file and sets indicators. |
| [SendErrorMessage](#void-senderrormessagestringstringintarray)(string, string, int[]) | Sends an error message with message file and sets indicators. |

<a id="void-senderrormessagestringintarray"></a>

## void SendErrorMessage(string, int[])

Sends an error message using default file and sets indicators.

```cs
void SendErrorMessage(string, int[])
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| string | msgID | Message ID. |
| int[] | errorIndicators | The Indicators. |

### Remarks
Sends an error message using default file and sets indicators.

<a id="void-senderrormessagestringstringintarray"></a>

## void SendErrorMessage(string, string, int[])

Sends an error message with message file and sets indicators.

```cs
void SendErrorMessage(string, string, int[])
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| string | msgID | Message ID. |
| string | msgFile | Message File. |
| int[] | errorIndicators | Array of error indicators. |

### Remarks
Sends an error message with message file and sets indicators.

## See Also
- [EscapeProgram class](escape-program.html)
