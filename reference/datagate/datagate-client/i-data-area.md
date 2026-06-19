---
title: "IDataArea interface"
description: "Defines the contract for managing a data area in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines the contract for managing a data area in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html), [IComparable](https://learn.microsoft.com/en-us/dotnet/api/system.icomparable-1?view=net-8.0), [IConnectionHandler](/reference/datagate/datagate-client/i-connection-handler.html), [IDisposable](https://learn.microsoft.com/en-us/dotnet/api/system.idisposable?view=net-8.0)
<br>
<br>

## Remarks
This interface provides properties and methods to manage a data area in the ASNA DataGate client. 
It includes properties to get and set the length and number of decimal places of the data area, 
methods to set the initial value, change the value, retrieve the value, 
and convert between ProgParm parameters and objects.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Decimals | Gets or sets the number of decimal places in the data area. The number of decimals can be between 0 and 9. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets or sets the length of the data area. The length can be between 1 and 2000. |

## Methods

| Signature | Description |
| --- | --- |
| [AppendParm](i-data-area-appendparm.html#void-appendparm-progparm-parameter)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Appends a ProgParm parameter to the data area.
| [Change](i-data-area-change.html#void-change-bool-value)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Changes the value of the data area to a boolean value.
| [Change](i-data-area-change.html#void-change-decimal-value)([Decimal](https://docs.microsoft.com/en-us/dotnet/api/system.decimal)) | Changes the value of the data area to a decimal value.
| [Change](i-data-area-change.html#void-change-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Changes the value of the data area to a string value.
| [Change](i-data-area-change.html#void-change-string-value-int-startingoffset-int-substringlength)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Changes a subset of the data area to a string value.
| [Change](i-data-area-change.html#void-change-progparm-value)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Changes the value of the data area to a ProgParm value.
| [Change](i-data-area-change.html#void-change-progparm-value-int-startingoffset-int-substringlength)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Changes a subset of the data area to a ProgParm value.
| [ObjectToParm](i-data-area-objecttoparm.html#void-objecttoparm-object-value-string-parametername)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts an object to a ProgParm parameter and assigns it to the data area.
| [ObjectToParm](i-data-area-objecttoparm.html#void-objecttoparm-progparm-parameter-object-value)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Converts an object to a ProgParm parameter and assigns it to the data area.
| [ObjectToParm](i-data-area-objecttoparm.html#void-objecttoparm-progparm-parameter-object-value-int-element)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts an object to a ProgParm parameter and assigns it to the data area.
| [ObjectToParm](i-data-area-objecttoparm.html#void-objecttoparm-object-value-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts an object to a ProgParm parameter and assigns it to the data area.
| [ParmToObject](i-data-area-parmtoobject.html#object-parmtoobject-type-returntype-string-parametername)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Converts a ProgParm parameter to an object.
| [ParmToObject](i-data-area-parmtoobject.html#object-parmtoobject-progparm-parameter-type-returntype)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type)) | Converts a ProgParm parameter to an object.
| [ParmToObject](i-data-area-parmtoobject.html#object-parmtoobject-progparm-parameter-type-returntype-int-element)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a ProgParm parameter to an object.
| [ParmToObject](i-data-area-parmtoobject.html#object-parmtoobject-type-returntype-string-parametername-int32-elementindices-https-docs-microsoft-com-en-us-dotnet-api-system-int32)([Type](https://docs.microsoft.com/en-us/dotnet/api/system.type), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Converts a ProgParm parameter to an object.
| [Retrieve()](i-data-area-retrieve.html#object-retrieve) | Retrieves the value of the data area.
| [Retrieve](i-data-area-retrieve.html#string-retrieve-int-startingoffset-int-substringlength)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Get a subset of the data in a character-type data area.
| [Retrieve](i-data-area-retrieve.html#void-retrieve-progparm-value)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html)) | Retrieves the value of the data area into a ProgParm value.
| [Retrieve](i-data-area-retrieve.html#void-retrieve-progparm-value-int-startingoffset-int-substringlength)([ProgParm](/reference/datagate/datagate-data-link/prog-parm.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Retrieves a subset of the data area into a ProgParm value.
| [SetInitialValue](i-data-area-setinitialvalue.html#void-setinitialvalue-string-value)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Sets the initial value of the data area.

