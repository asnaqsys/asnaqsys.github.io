---
title: "dgException.FormatMessage Method"
description: "Formats the error message into a single string for logging or displaying to the user."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Formats the error message into a single string for logging or displaying to the user.

<a id="string-formatmessage-iformatprovider-provider-string-msg"></a>
## string FormatMessage(IFormatProvider provider, string msg)

Formats the error message into a single string for logging or displaying to the user.

```cs
string FormatMessage(IFormatProvider provider, string msg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFormatProvider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0) | provider | An object that supplies culture-specific formatting information.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msg | The error message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | A formatted string containing the error message.

## See Also
- [dgException class](dg-exception.html)
