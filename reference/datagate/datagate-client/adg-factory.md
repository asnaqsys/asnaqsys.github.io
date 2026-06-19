---
title: "AdgFactory class"
description: "The AdgFactory class static methods construct instances of IAdgObject representing database files, libraries, and members along with IDataArea for dat"
last_modified_at: 2024-08-09T17:25:07Z
---

The AdgFactory class static methods construct instances of IAdgObject representing database files, libraries, and members along with IDataArea for data areas.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (**Shared**) members of this type are safe for multithreaded operations. 

Any instance members are not guaranteed to be thread safe.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | AppDefaultBulkCopyTimeout | Gets or sets the default timeout for bulk copy operations. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | AppUseBulkCopyByDefault | Gets or sets a value indicating whether the application should use bulk copy by default. |

## Methods

| Signature | Description |
| --- | --- |
| [NewDataArea](adg-factory-newdataarea.html#idataarea-newdataarea-adgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface with an unknown subtype.
| [NewDataArea](adg-factory-newdataarea.html#idataarea-newdataarea-adgconnection-cn-string-pathname-adgsubtypes-dataareatype)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgSubTypes](/reference/datagate/datagate-common/adg-sub-types.html)) | Creates a new instance of the  interface with a specified subtype.
| [NewDirectory](adg-factory-newdirectory.html#idirectory-newdirectory-adgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewFile](adg-factory-newfile.html#ifileobject-newfile-adgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewLibraryList](adg-factory-newlibrarylist.html#ilibrarylist-newlibrarylist-adgconnection-cn)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Creates a new instance of the  interface.
| [NewMember](adg-factory-newmember.html#imember-newmember-adgconnection-cn-string-pathname)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewObject](adg-factory-newobject.html#iadgobject-newobject-adgconnection-cn-adgobjecttypes-type-string-path)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Creates a new instance of the  interface.
| [NewSystemValue](adg-factory-newsystemvalue.html#isystemvalue-newsystemvalue-adgconnection-cn-bool-withnewtransaction)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Creates a new instance of the  interface.
| [ReadXml](adg-factory-readxml.html#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html)) | Reads an XML document and creates a new instance of the  interface.
| [ReadXml](adg-factory-readxml.html#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-string-docobjectnewname-xmlreader-reader-xmloptions-options)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html)) | Reads an XML document and creates a new instance of the  interface.
| [ReadXml](adg-factory-readxml.html#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options-xmlcanceleventhandler-observer)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html), [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html)) | Reads an XML document and creates a new instance of the  interface.
| [ReadXml](adg-factory-readxml.html#iadgobject-readxml-adgconnection-cn-string-containerpath-adgobjecttypes-docobjecttype-xmlreader-reader-xmloptions-options)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [AdgObjectTypes](/reference/datagate/datagate-common/adg-object-types.html), [XmlReader](https://learn.microsoft.com/en-us/dotnet/api/system.xml.xmlreader?view=net-8.0), [XmlOptions](/reference/datagate/datagate-client/xml-options.html)) | Reads an XML document and creates a new instance of the  interface.
| [Synchronized](adg-factory-synchronized.html#iadgobject-synchronized-iadgobject-adgobj)([IAdgObject](/reference/datagate/datagate-client/i-adg-object.html)) | Wraps an  in a synchronized (thread-safe) wrapper.
| [Synchronized](adg-factory-synchronized.html#ilibrarylist-synchronized-ilibrarylist-llobj)([ILibraryList](/reference/datagate/datagate-client/i-library-list.html)) | Wraps an  in a synchronized (thread-safe) wrapper.

