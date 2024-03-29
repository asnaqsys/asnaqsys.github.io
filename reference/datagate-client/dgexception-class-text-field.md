---
title: dgException.Text Field

---

Provider-dependent text information association with the dgException.

```cs
 public String Text
```

## Field Value

String. A system-level message associated with certain exceptions.
## Remarks

<span> **Text** </span> is a string which may be returned by DataGate providers for certain conditions. Its use is provider dependent. If not set by the provider, **Text** refers to the empty string.

If the DataGate provider is an IBM i database, <span>Text</span> will contain useful information only if the value of [ ErrorClass](dgexception-class-error-class-field.html) is one of the following:

- dgEC_AS400CPF
- dgEC_AS400MCH
- dgEC_AS400CPI
- dgEC_AS400DG8

In these cases, **Text** will contain a message associated with a system error. This is usually the "extended error" message associated with an IBM i system error. Note that in this case, the Message property will return the value of the <span>Text</span> field. Also in these cases, [Error](dgexception-class-error-field.html) will be set to dgEsAS400ERROR.
## Requirements

Namespace: [ ASNA.DataGate.Common](datagate-common-namespace.html)

Assembly: ASNA DataGate Client

Platforms: Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[dgException Class](dgexception-class.html)
      <br />
[dgException Members](dgexception-class-members.html)
      <br />
[ASNA.DataGate.Common Namespace](datagate-common-namespace.html)
      <br />
[Error Field](dgexception-class-error-field.html)
      <br />
[ErrorClass Field](dgexception-class-error-class-field.html)

