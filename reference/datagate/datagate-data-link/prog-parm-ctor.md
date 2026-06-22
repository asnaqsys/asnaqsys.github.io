---
title: "ProgParm Constructors"
description: "Initializes a new instance of the class with the specified parameter type and data direction."
---

## Definition

**Namespace:** ASNA.DataGate.DataLink  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Initializes a new instance of the class with the specified parameter type and data direction.

## Overloads

| Name | Description |
| --- | --- |
| [ProgParm](#progparm-progparmtype-datadirection)([ProgParmType](/reference/datagate/datagate-data-link/prog-parm-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html)) | Initializes a new instance of the class with the specified parameter type and data direction. |
| [ProgParm](#progparm-structuretype-datadirection)([StructureType](/reference/datagate/datagate-data-link/structure-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html)) | Initializes a new instance of the class with the specified structure type and data direction. |

<a id="progparm-progparmtype-datadirection"></a>
### ProgParm([ProgParmType](/reference/datagate/datagate-data-link/prog-parm-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html))

Initializes a new instance of the  class with the specified parameter type and data direction.

```cs
ProgParm(ProgParmType, DataDirection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ProgParmType](/reference/datagate/datagate-data-link/prog-parm-type.html) | ppt | The type of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | dir | The direction of the data (input, output, or both).

<a id="progparm-structuretype-datadirection"></a>
### ProgParm([StructureType](/reference/datagate/datagate-data-link/structure-type.html), [DataDirection](/reference/datagate/datagate-common/data-direction.html))

Initializes a new instance of the  class with the specified structure type and data direction.

```cs
ProgParm(StructureType, DataDirection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [StructureType](/reference/datagate/datagate-data-link/structure-type.html) | st | The structure type of the parameter.
| [DataDirection](/reference/datagate/datagate-common/data-direction.html) | dir | The direction of the data (input, output, or both).

## See Also
- [ProgParm class](prog-parm.html)
