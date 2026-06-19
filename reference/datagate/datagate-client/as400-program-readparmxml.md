---
title: "As400Program.ReadParmXml Method"
description: "Reads the parameters of the program from an XML reader."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Reads the parameters of the program from an XML reader.

<a id="void-readparmxml-xmlreader-reader"></a>
## void ReadParmXml(XmlReader reader)

Reads the parameters of the program from an XML reader.

#### Remarks
This method reads the parameters of the program in the ASNA DataGate client from an XML reader. It checks if the provided XML reader is null, and if so, throws an ArgumentNullException. It also checks if the read state of the XML reader is not Initial, and if so, throws an ArgumentException. It then reads the "apcml" and "program" elements from the XML. If the "program" element is not found, it throws an XmlException. It then reads the name attribute of the "program" element and creates a new list of parameters. It then reads each parameter from the XML using the ProgParm constructor, appends it to the list, and creates a new buffer for it. It then reads the end of the "program" and "apcml" elements and closes the XML reader, and sets the program name and parameters to the new values.

```cs
void ReadParmXml(XmlReader reader)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0) | reader | The XML reader to read from.

## See Also
- [As400Program class](as400-program.html)
