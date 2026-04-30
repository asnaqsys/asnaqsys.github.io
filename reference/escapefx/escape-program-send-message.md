---
title: "EscapeProgram.SendMessage Method"
description: "Sends a message to the program message queue."
---

## Definition

**Namespace:** ASNA.QSys.EscapeFX  
**Assembly:** ASNA.QSys.EscapeFX.dll

Sends a message to the program's message queue.

## Overloads

| Signature | Description |
| --- | --- |
| [SendMessage](#void-sendmessage)() | Sends a message using current message fields. |
| [SendMessage](#void-sendmessagestringstring)(string, string) | Sends a message with the specified ID and file. |

<a id="void-sendmessage"></a>

## void SendMessage()

Sends a message using current message fields.

```cs
void SendMessage()
```

### Remarks
Sends a message using current message fields.

<a id="void-sendmessagestringstring"></a>

## void SendMessage(string, string)

Sends a message with the specified ID and file.

```cs
void SendMessage(string, string)
```

#### Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| string | msgID | Parameter. |
| string | msgFile | Parameter. |

### Remarks
Sends a message with the specified ID and file.

## See Also
- [EscapeProgram class](escape-program.html)
