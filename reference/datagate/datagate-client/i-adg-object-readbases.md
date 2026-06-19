---
title: "IAdgObject interface.ReadBases Method"
description: "Reads the base objects of the ADG object from an XML reader."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads the base objects of the ADG object from an XML reader.

<a id="void-readbases-xmlreader-reader"></a>
## void ReadBases(XmlReader reader)

Reads the base objects of the ADG object from an XML reader.

#### Remarks
This method is used to read the base objects of the ADG object from an XML reader. The reader parameter specifies the XML reader to read from. This can be useful for deserializing the object's state from XML.

```cs
void ReadBases(XmlReader reader)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The XML reader to read from.

## See Also
- [IAdgObject interface class](i-adg-object.html)
