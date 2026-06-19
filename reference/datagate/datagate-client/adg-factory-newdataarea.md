---
title: "AdgFactory.NewDataArea Method"
description: "Creates a new instance of the interface with an unknown subtype."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Creates a new instance of the interface with an unknown subtype.

## Overloads

| Signature | Description |
| --- | --- |
| [NewDataArea](#idataarea-newdataarea-adgconnection-cn-string-pathname)(IDataArea NewDataArea(AdgConnection cn, string PathName)) | Creates a new instance of the interface with an unknown subtype. |
| [NewDataArea](#idataarea-newdataarea-adgconnection-cn-string-pathname-adgsubtypes-dataareatype)(IDataArea NewDataArea(AdgConnection cn, string PathName, AdgSubTypes DataAreaType)) | Creates a new instance of the interface with a specified subtype. |

<a id="idataarea-newdataarea-adgconnection-cn-string-pathname"></a>
## IDataArea NewDataArea(AdgConnection cn, string PathName)

Creates a new instance of the  interface with an unknown subtype.

#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.The subtype of the data area is set to .

```cs
IDataArea NewDataArea(AdgConnection cn, string PathName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the data area.

#### Returns

| Type | Description
| --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | A new instance of the  interface.

<a id="idataarea-newdataarea-adgconnection-cn-string-pathname-adgsubtypes-dataareatype"></a>
## IDataArea NewDataArea(AdgConnection cn, string PathName, AdgSubTypes DataAreaType)

Creates a new instance of the  interface with a specified subtype.

#### Remarks
This method uses the  method to create a new instance of the  interface.The  method is a generic method that takes a function delegate as a parameter.The function delegate is responsible for creating the new instance.If the  parameter is null, an  is thrown.The subtype of the data area is set to the value of the  parameter.

```cs
IDataArea NewDataArea(AdgConnection cn, string PathName, AdgSubTypes DataAreaType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The  to use for the operation.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | PathName | The path name of the data area.
| [AdgSubTypes](/reference/datagate/datagate-common/adg-sub-types.html) | DataAreaType | The subtype of the data area.

#### Returns

| Type | Description
| --- | ---
| [IDataArea](/reference/datagate/datagate-client/i-data-area.html) | A new instance of the  interface.

## See Also
- [AdgFactory class](adg-factory.html)
