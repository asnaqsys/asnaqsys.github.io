---
title: "XmlElementConverter.GetXsdBooleanAttribute Method"
description: "Gets the value of the attribute with the specified name from the current XmlElement and converts it to a boolean."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the value of the attribute with the specified name from the current XmlElement and converts it to a boolean.

<a id="bool-getxsdbooleanattribute-string-name-bool-defaultvalue"></a>
## bool GetXsdBooleanAttribute(string name, bool defaultValue)

Gets the value of the attribute with the specified name from the current XmlElement and converts it to a boolean. If the attribute does not exist, returns the specified default value.

```cs
bool GetXsdBooleanAttribute(string name, bool defaultValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | defaultValue | The value to return if the attribute does not exist.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | The boolean value of the attribute, or the default value if the attribute does not exist.

## See Also
- [XmlElementConverter class](xml-element-converter.html)
