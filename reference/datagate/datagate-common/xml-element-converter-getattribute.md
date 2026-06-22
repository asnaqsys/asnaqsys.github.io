---
title: "XmlElementConverter.GetAttribute Method"
description: "Gets the value of the attribute with the specified name from the current XmlElement."
---

## Definition

**Namespace:** ASNA.DataGate.Common  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Gets the value of the attribute with the specified name from the current XmlElement.

## Overloads

| Signature | Description |
| --- | --- |
| [GetAttribute](#string-getattribute-string-name)(string GetAttribute(string name)) | Gets the value of the attribute with the specified name from the current XmlElement. |
| [GetAttribute](#string-getattribute-string-name-object-defaultvalue)(string GetAttribute(string name, object defaultValue)) | Gets the value of the attribute with the specified name from the current XmlElement. |

<a id="string-getattribute-string-name"></a>
## string GetAttribute(string name)

Gets the value of the attribute with the specified name from the current XmlElement.

```cs
string GetAttribute(string name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of the attribute.

<a id="string-getattribute-string-name-object-defaultvalue"></a>
## string GetAttribute(string name, object defaultValue)

Gets the value of the attribute with the specified name from the current XmlElement. If the attribute does not exist, returns the specified default value.

```cs
string GetAttribute(string name, object defaultValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | name | The name of the attribute.
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | defaultValue | The value to return if the attribute does not exist.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The value of the attribute, or the default value if the attribute does not exist.

## See Also
- [XmlElementConverter class](xml-element-converter.html)
