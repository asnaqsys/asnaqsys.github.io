---
title: "AdgFactory.NewObject Method"
description: "Creates a new instance of the interface."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new instance of the interface.

<a id="iadgobject-newobject-adgconnection-cn-adgobjecttypes-type-string-path"></a>
## IAdgObject NewObject(AdgConnection cn, AdgObjectTypes type, string path)

Creates a new instance of the  interface.

#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.

```cs
IAdgObject NewObject(AdgConnection cn, AdgObjectTypes type, string path)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html) | type | The type of the object to create.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | path | The path of the object to create.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A new instance of the  interface.

## See Also
- [AdgFactory class](adg-factory.html)
