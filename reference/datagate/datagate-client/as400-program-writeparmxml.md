---
title: "As400Program.WriteParmXml Method"
description: "Writes the parameters of the program to an XML writer."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Writes the parameters of the program to an XML writer.

<a id="void-writeparmxml-xmlwriter-writer"></a>
## void WriteParmXml(XmlWriter writer)

Writes the parameters of the program to an XML writer.

#### Remarks
This method writes the parameters of the program in the ASNA DataGate client to an XML writer. It checks if the provided XML writer is null, and if so, throws an ArgumentNullException. It also checks if the write state of the XML writer is not Start, and if so, throws an ArgumentException. It then writes the start of the document, the start of the "apcml" element with the appropriate namespace and version attribute, the start of the "program" element with the program name attribute, and the XML representation of each parameter using the WriteXml method of the parameter. It then writes the end of the "program" and "apcml" elements and the end of the document, and closes the XML writer.

```cs
void WriteParmXml(XmlWriter writer)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0) | writer | The XML writer to write to.

## See Also
- [As400Program class](as400-program.html)
