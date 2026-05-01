---
title: "BuildDropdownList class"
description: "Represents the BuildDropdownList type in ASNA.QSys.EscapeFX."
---

Represents the BuildDropdownList type in ASNA.QSys.EscapeFX.

**Namespace:** ASNA.QSys.EscapeFX
**Assembly:** ASNA.QSys.EscapeFX.dll

**Inheritance:** EscapeProgram

BuildDropdownList is a utility program that produces a single string with the list of the valid values for a filed defined with a ListID. 

BuildDropdownList is implemented as an EscapeProgram with four string parameters:

| Parameter   | Direction | Description |
| ----------- | --------- | ----------- |
| ListHTML    | output    | The formatted list values
| ModelPrefix | input     | The first two character of the file containing the list definition
| ListID      | input     | The ID of the desired List
| TargetValue | input     | The value that will be used to determine which *row*, if any, will be marked as 'selected'.

The output parameter ListHTML will contain a string representing a 3 'column table', with each *row* delimited by a new line character and each column separated with a Tab, something like this (where → represents a Tab character /u0009):<br/>
```
     A →           →  A-Allowed
     B →  selected →  B-Bypassed
     C →           →  C-Canceled
     D →           →  D-Delayed
```

The first column contains the 'option' value, the second column whether that value is 'selected' and the third column the external value aka. description.

The program utilizes a database file with a name equal to the concatenation of the `ModelPrefix` parameter with the string `"VLLSL_E"`, for example `"Y2VLLSL_E"`. The file should have at least three fields:
 - INTVAL : List ID
 - EXTVAL : Option Value
 - CNDTXT : Option Description

 The returned list is formed by formatting the `EXTVAL` and `CNDDTXT` of all the records with an `INTVAL` equal to the parameter `ListID`.

The BuildDropdownList can be the target of a [Dynamic Program CALL](/reference/runtime/qsys-runtime/dynamic-caller.html) or, more typically, can be invoked by a [DdsDynamicList](/reference/expo/qsys-expo-tags/dds-dynamic-list-tag-helper.html).

```html
<DdsDynamicList Col="60" ProgramName="ASNA.QSys.EscapeFX.BuildDropdownList" TargetField="REC1.STATUS" ParmsData="Y2,1100123">
```