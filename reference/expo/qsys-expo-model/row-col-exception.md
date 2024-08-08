---
title: "RowColException class         | QSYS API Reference Guide"
description: "Provides an Exception derived class with the detailed invalid row, col string format (typically from VirtualRowCol field property) "
last_modified_at: 2024-08-08T21:42:10Z
---

Provides an Exception derived class with the detailed invalid row, col string format (typically from VirtualRowCol field property)

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [RowColException](#rowcolexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes an instance of RowColException class

### RowColException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes an instance of RowColException class

```cs
RowColException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | rowCol | Row and Colum string specification. Comma separated values
