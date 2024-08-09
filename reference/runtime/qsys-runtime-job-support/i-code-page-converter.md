---
title: "ICodePageConverter interface  | QSYS API Reference Guide"
description: "Implement this interface to add your own CodePage conversion if Wings or the 5250 emulator don&#39;t already know it. "
last_modified_at: 2024-08-09T17:25:29Z
---

Implement this interface to add your own CodePage conversion if Wings or the 5250 emulator don't already know it.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Methods

| Signature | Description |
| --- | --- |
| [MSCodePageFromIBMCodePage](#bool-mscodepagefromibmcodepageint-ibmcodepage-int32-mscodepage)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts IBM i CodePage numbers to the corresponding .Net Encoding CodePage numbers. See "Code Page Identifiers" in MSDN help: http://msdn.microsoft.com/en-us/library/dd317756%28v=vs.85%29.aspx.

### bool MSCodePageFromIBMCodePage([int ibmCodePage](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [Int32& msCodePage](https://docs.microsoft.com/en-us/dotnet/api/system.int32))

Converts IBM i CodePage numbers to the corresponding .Net Encoding CodePage numbers. See "Code Page Identifiers" in MSDN help: http://msdn.microsoft.com/en-us/library/dd317756%28v=vs.85%29.aspx.

```cs
bool MSCodePageFromIBMCodePage(int ibmCodePage, Int32& msCodePage)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | ibmCodePage | The CodePage number in the IBM i.
| [Int32&](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | msCodePage | The CodePage number in .Net Encoding corresponding to the IBM i CodePage.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the conversion for a particular IBM i CodePage succeeded. False if not.
