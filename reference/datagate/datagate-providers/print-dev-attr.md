---
title: "PrintDevAttr class"
description: "Compatibility class for dgPrintDeviceAttr structure. "
last_modified_at: 2024-08-09T17:25:07Z
---

Compatibility class for dgPrintDeviceAttr structure.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Hashtable](https://learn.microsoft.com/en-us/dotnet/api/system.collections.hashtable?view=net-8.0)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.



## Constructors

| Name | Description |
| --- | --- |
| [PrintDevAttr()](print-dev-attr-ctor.html#printdevattr) | Initializes a new instance of the  class.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Collate | Gets or sets a value indicating whether collation should be used when printing multiple copies. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Color | Gets or sets the color of the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Copies | Gets or sets the number of copies to print. |
| [PaperSourceKind](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.papersourcekind?view=dotnet-plat-ext-8.0) | DefaultSource | Gets or sets the default source of the printout. |
| [Duplex](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.duplex?view=dotnet-plat-ext-8.0) | Duplex | Gets or sets a value indicating whether duplex printing is enabled. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | FormName | Gets or sets the name of the form to be used for the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | LeftMargin | Gets or sets the left margin of the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Length | Gets or sets the length of the printout. |
| [PaperOrientation](/reference/datagate/datagate-common/paper-orientation.html) | Orientation | Gets or sets the orientation of the printout. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PrinterName | Gets or sets the name of the printer. |
| [PrinterResolutionKind](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.printerresolutionkind?view=dotnet-plat-ext-8.0) | Quality | Gets or sets the quality of the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Scale | Gets or sets the scale of the printout. |
| [PaperKind](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.printing.paperkind?view=dotnet-plat-ext-8.0) | Size | Gets or sets the size of the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | TopMargin | Gets or sets the top margin of the printout. |
| [PrintTrueType](/reference/datagate/datagate-common/print-true-type.html) | TTOption | Gets or sets the TrueType font option for the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Width | Gets or sets the width of the printout. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | YResolution | Gets or sets the vertical resolution of the printout. |

## Methods

| Signature | Description |
| --- | --- |
| [ReadXml](print-dev-attr-readxml.html#void-readxml-xmlreader-reader)([XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0)) | Generates an object from its XML representation.
| [WriteXml](print-dev-attr-writexml.html#void-writexml-xmlwriter-writer)([XmlWriter](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlwriter?view=net-8.0)) | Converts the current instance into an XML string.

