---
title: "AdgFactory.NewLibraryList Method"
description: "Creates a new instance of the interface."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new instance of the interface.

<a id="ilibrarylist-newlibrarylist-adgconnection-cn"></a>
## ILibraryList NewLibraryList(AdgConnection cn)

Creates a new instance of the  interface.

#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
ILibraryList NewLibraryList(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.

#### Returns

| Type | Description
| --- | ---
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | A new instance of the  interface.

## See Also
- [AdgFactory class](adg-factory.html)
