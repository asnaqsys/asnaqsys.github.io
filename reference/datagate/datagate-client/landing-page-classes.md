---
title: "ASNA.DataGate.Client Classes"
description: TOC Landing page for ASNA.DataGate.Client Classes
---

## Remarks

The following are the classes provided by **ASNA DataGate Client** namespace.


| Type | Description |
| --- | --- |
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | The AdgConnection class controls database connection resources and allows them to be shared among DataGate objects in your program.  |
| [AdgDataSet](/reference/datagate/datagate-client/adg-data-set.html) | A DataGate-compatible DataSet class for record-oriented database access. |
| [AdgEnumerator](/reference/datagate/datagate-client/adg-enumerator.html) | Represents a method that handles an IAdgObject. |
| [AdgFactory](/reference/datagate/datagate-client/adg-factory.html) | The AdgFactory class static methods construct instances of IAdgObject representing database files, libraries, and members along with IDataArea for data areas. |
| [AdgKeyTable](/reference/datagate/datagate-client/adg-key-table.html) | The AdgKeyTable class contains a DataTable object for manipulating key values. |
| [AdgObserver](/reference/datagate/datagate-client/adg-observer.html) | Represents a method that processes a string. |
| [AdgTable](/reference/datagate/datagate-client/adg-table.html) | The AdgTable class supports DG infrastructure and is not intended to be used directly from your code. |
| [As400Program](/reference/datagate/datagate-client/as400-program.html) | Represents a program in the ASNA DataGate client. |
| [AuthorityEntry](/reference/datagate/datagate-client/authority-entry.html) | The AuthorityEntry class describes a user or group authorization to a database object. |
| [CopyFromImportFileOptions](/reference/datagate/datagate-client/copy-from-import-file-options.html) | Provides options for copying data from an import file. |
| [DatabaseLabel](/reference/datagate/datagate-client/database-label.html) | The `DatabaseLabel` class provides static methods for managing and interacting with database labels in a DataGate environment. |
| [DataRowColumnComparer\<T\>](/reference/datagate/datagate-client/data-row-column-comparer-1.html) | This minor variation of the System.Data.DataRowComparer<T> classimplements IEqualityComparer<T> using value based semantics whencomparing certain columns of DataRow instances. |
| [DbXmlNameConverter](/reference/datagate/datagate-client/db-xml-name-converter.html) | This class is a filter used in the XML transforms ExportToXml.xslt andImportToXml.xslt.  Encode() takes an arbitrary string and returns anXML-compliant Name string.  For example, "$ITEMTEST" is returned as"_x0024_ITEMTEST".  Decode() performs the inverse function. |
| [Delimiter](/reference/datagate/datagate-client/delimiter.html) | Represents a delimiter in a data stream. |
| [Dependent](/reference/datagate/datagate-client/dependent.html) | The `Dependent` class represents a dependency in the ASNA DataGate environment. |
| [Export](/reference/datagate/datagate-client/export.html) | Provides functionality for exporting data to XML or CSV format.This class includes methods for creating tasks to perform the export, logging messages, writing to a database file, and transforming the data to XML or CSV format. |
| [ExportOptions](/reference/datagate/datagate-client/export-options.html) | Provides methods for exporting data to XML or CSV formats.This class includes functionality for transforming data using XSLT, logging, and handling cancellation tokens. |
| [ExportToCsvOptions](/reference/datagate/datagate-client/export-to-csv-options.html) | Provides options for exporting data to CSV format.This class includes properties for specifying whether field names should be included, whether trailing delimiters should be omitted, and what characters should be used for text delimiters, field delimiters, and decimal points in the exported data. |
| [ExportToXmlOptions](/reference/datagate/datagate-client/export-to-xml-options.html) | Provides options for exporting data to XML format.This class includes properties for specifying whether fields should be exported as elements and whether the schema should be included in the exported data. |
| [FileAdapter](/reference/datagate/datagate-client/file-adapter.html) | The  class manages file operations like opening, closing, reading, writing, and querying, handling various access modes and settings. |
| [Import](/reference/datagate/datagate-client/import.html) | Provides functionality for importing data into the application. |
| [ImportFromCsvOptions](/reference/datagate/datagate-client/import-from-csv-options.html) | Represents options for importing data from a CSV file. |
| [ImportOptions](/reference/datagate/datagate-client/import-options.html) | Provides options for importing data from XML or CSV format.This class includes properties for specifying the target member where the data will be imported, the source path from where the data will be imported, whether the target member should be cleared before the import, whether the target connection should be used for the import, and whether detailed feedback should be provided during the import operation. |
| [MultiCharDelimiter](/reference/datagate/datagate-client/multi-char-delimiter.html) | Represents a delimiter in a data stream. |
| [NewLineDelimeter](/reference/datagate/datagate-client/new-line-delimeter.html) | Represents a newline delimiter in a data stream. |
| [OpenFileAdapterDelegate](/reference/datagate/datagate-client/open-file-adapter-delegate.html) | Represents the method that will handle the opening of a file adapter. |
| [OpMessageArgs](/reference/datagate/datagate-client/op-message-args.html) | Represents the arguments for an operation message event.This class is derived from EventArgs and is used to pass a message string with an event. |
| [PrintingProps](/reference/datagate/datagate-client/printing-props.html) | Represents the application settings for printing properties.This class is auto-generated and changes may be overwritten. |
| [XmlCancelEventArgs](/reference/datagate/datagate-client/xml-cancel-event-args.html) | Provides data for the XmlCancelEvent event. |
| [XmlCancelEventHandler](/reference/datagate/datagate-client/xml-cancel-event-handler.html) | Represents the method that will handle an event when an XML operation can be canceled. |
