---
title: "AdgFactory.NewMember Method"
description: "Creates a new instance of the interface."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new instance of the interface.

<a id="imember-newmember-adgconnection-cn-string-pathname"></a>
## IMember NewMember(AdgConnection cn, string PathName)

Creates a new instance of the  interface.

#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
IMember NewMember(AdgConnection cn, string PathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the member.

#### Returns

| Type | Description
| --- | ---
| [IMember](/reference/datagate/datagate-client/i-member.html) | A new instance of the  interface.

## See Also
- [AdgFactory class](adg-factory.html)
