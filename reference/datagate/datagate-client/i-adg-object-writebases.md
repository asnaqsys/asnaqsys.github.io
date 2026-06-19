---
title: "IAdgObject interface.WriteBases Method"
description: "Writes the base objects of the ADG object to an XML writer."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes the base objects of the ADG object to an XML writer.

<a id="void-writebases-xmlwriter-writer"></a>
## void WriteBases(XmlWriter writer)

Writes the base objects of the ADG object to an XML writer.

#### Remarks
This method is used to write the base objects of the ADG object to an XML writer. The writer parameter specifies the XML writer to write to. This can be useful for serializing the object's state to XML.

```cs
void WriteBases(XmlWriter writer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.

## See Also
- [IAdgObject interface class](i-adg-object.html)
