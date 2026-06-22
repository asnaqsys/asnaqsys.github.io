---
title: "IndicatorExpression class"
description: "A condition is an ANDed grouping of two through nine indicators that must all be in effect (set off if N or ! is specified; set on if N or ! is not sp"
last_modified_at: 2024-08-09T17:25:07Z
---

A condition is an ANDed grouping of two through nine indicators that
must all be in effect (set off if N or ! is specified; set on if N
or ! is not specified) before the field or keyword is selected. You can
specify a maximum of nine indicators for each condition and nine
conditions for each field or keyword. You can also specify several
conditions for a field or keyword so that if any one of them is
satisfied, the field or the keyword is selected. This is called an OR
relationship
example: 1 & 2 & !3 | 44 & 55 | 60

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [IndicatorExpression](indicator-expression-ctor.html#indicatorexpression-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the  class with the specified expression string.

## Methods

| Signature | Description |
| --- | --- |
| [Eval](indicator-expression-eval.html#bool-eval-char-indicators-https-docs-microsoft-com-en-us-dotnet-api-system-char)([Char\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.char)) | Evaluates the indicator expression against the provided set of indicators.

