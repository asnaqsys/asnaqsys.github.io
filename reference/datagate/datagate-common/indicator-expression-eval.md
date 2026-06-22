---
title: "IndicatorExpression.Eval Method"
description: "Evaluates the indicator expression against the provided set of indicators."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Evaluates the indicator expression against the provided set of indicators.

<a id="bool-eval-char-indicators-https-docs-microsoft-com-en-us-dotnet-api-system-char"></a>
## bool Eval([Char\[\] indicators](https://docs.microsoft.com/en-us/dotnet/api/system.char))

Evaluates the indicator expression against the provided set of indicators.

#### Remarks
This method evaluates the indicator expression, which is a string representation of a boolean expression involving indicators. The indicators are represented as an array of characters, where each character represents the state of an indicator (typically '0' for off and '1' for on).The indicator expression is evaluated in the context of the provided indicators, and the result of the evaluation is returned as a boolean value.Note that the indicator expression must be a valid boolean expression involving the indicators, and any invalid expression will cause an exception to be thrown when this method is called.

```cs
bool Eval(Char[] indicators)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char) | indicators | An array of characters representing the indicators to be evaluated.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | A boolean value that represents the result of the evaluation.

## See Also
- [IndicatorExpression class](indicator-expression.html)
