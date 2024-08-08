---
title: "XmlInfoMsgType enum           | QSYS API Reference Guide"
description: "Enum representing various types of XML information messages. "
last_modified_at: 2024-08-08T21:41:32Z
---

Enum representing various types of XML information messages.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| aaaFirstMsgType | Represents the first message type in the enumeration. | 0 |
| AbandonMemberExport | Represents the event of abandoning a member export. | 94 |
| AddDataOpenError | Represents an error when opening data. | 1 |
| AddRecordBatchErrorCount | Represents an error count when adding a batch of records. | 2 |
| AddRecordCount | Represents the count of records added. | 3 |
| AddRecordDataError | Represents an error when adding record data. | 4 |
| AddRecordError | Represents an error when adding a record. | 5 |
| AddRecordErrorCount | Represents the count of errors when adding records. | 6 |
| AdgObjectAttrExportComplete | Represents the completion of an ADG object attribute export. | 7 |
| AdgObjectAttrImportComplete | Represents the completion of an ADG object attribute import. | 8 |
| AdgObjectContentExportComplete | Represents the completion of an ADG object content export. | 9 |
| AdgObjectContentImportComplete | Represents the completion of an ADG object content import. | 10 |
| BasePathToAbsolutePath | Represents the event of converting a base path to an absolute path. | 11 |
| BasePathToRelativePath | Represents the event of converting a base path to a relative path. | 12 |
| BeginReadBases | Represents the beginning of reading base elements. | 13 |
| BeginReadCreateAttr | Represents the beginning of reading create attribute elements. | 14 |
| BeginReadDataAreaDef | Represents the beginning of reading data area definitions. | 15 |
| BeginReadDbfCreateAttr | Represents the beginning of reading DBF create attribute elements. | 16 |
| BeginReadFileDef | Represents the beginning of reading file definitions. | 17 |
| BeginReadRecords | Represents the beginning of reading records. | 18 |
| BeginReadXml | Represents the beginning of reading XML data. | 19 |
| BeginWriteBases | Represents the beginning of writing base elements. | 20 |
| BeginWriteCreateAttr | Represents the beginning of writing create attribute elements. | 21 |
| BeginWriteDataAreaDef | Represents the beginning of writing data area definitions. | 22 |
| BeginWriteDir | Represents the beginning of writing directory elements. | 23 |
| BeginWriteDirContent | Represents the beginning of writing directory content. | 24 |
| BeginWriteFileDef | Represents the beginning of writing file definitions. | 25 |
| BeginWriteMemberRecords | Represents the beginning of writing member records. | 26 |
| BeginWriteMembers | Represents the beginning of writing members. | 27 |
| BeginWriteText | Represents the beginning of writing text elements. | 28 |
| BeginWriteXml | Represents the beginning of writing XML data. | 29 |
| CompletedPath | Represents the completion of a path operation. | 30 |
| CreateDirIfNecessary | Represents the event of creating a directory if necessary. | 31 |
| CreateObject | Represents the event of creating an object. | 32 |
| DataAreaCreationFailure | Represents the event of a failure in creating a data area. | 33 |
| EndReadBases | Represents the end of reading base elements. | 34 |
| EndReadCreateAttr | Represents the end of reading create attribute elements. | 35 |
| EndReadDataAreaContent | Represents the end of reading data area content. | 36 |
| EndReadDataAreaDef | Represents the end of reading data area definitions. | 37 |
| EndReadDirContent | Represents the end of reading directory content. | 38 |
| EndReadFileAttr | Represents the end of reading file attributes. | 39 |
| EndReadFileContent | Represents the end of reading file content. | 40 |
| EndReadFileDef | Represents the end of reading file definitions. | 41 |
| EndReadMemberContent | Represents the end of reading member content. | 42 |
| EndReadObjectAttr | Represents the end of reading object attributes. | 43 |
| EndReadText | Represents the end of reading text elements. | 44 |
| EndReadXml | Represents the end of reading XML data. | 45 |
| EndWriteBases | Represents the end of writing base elements. | 46 |
| EndWriteCreateAttr | Represents the end of writing create attribute elements. | 47 |
| EndWriteDataAreaDef | Represents the end of writing data area definitions. | 48 |
| EndWriteDirContent | Represents the end of writing directory content. | 49 |
| EndWriteFileAttr | Represents the end of writing file attributes. | 50 |
| EndWriteFileContent | Represents the end of writing file content. | 51 |
| EndWriteFileDef | Represents the end of writing file definitions. | 52 |
| EndWriteMember | Represents the end of writing a member. | 53 |
| EndWriteText | Represents the end of writing text elements. | 54 |
| EndWriteXml | Represents the end of writing XML data. | 55 |
| ExceptionWriteDir | Represents an exception that occurred while writing to a directory. | 56 |
| ExportCompleteElementWithPath | Represents the completion of exporting an element with a path. | 57 |
| ExportingElementWithPath | Represents the event of exporting an element with a path. | 58 |
| FileCreationFailure | Represents a failure in file creation. | 59 |
| IgnoreExistingObject | Represents the event of ignoring an existing object. | 60 |
| IgnoreInvalidObjectByName | Represents the event of ignoring an invalid object by name. | 61 |
| ImportingElementWithPath | Represents the event of importing an element with a path. | 62 |
| InvalidDataArea | Represents an invalid data area. | 63 |
| InvalidVersionAttr | Represents an invalid version attribute. | 64 |
| MergeMemberExport | Represents the event of a member export merge. | 93 |
| ObjectCreated | Represents the event of an object being created. | 65 |
| OpCompleteIn | Represents the completion of an operation. | 66 |
| ReadInterimRecordCount | Represents the count of interim records read. | 67 |
| ReadInterimRecordCountClose | Represents the event of closing after reading interim record counts. | 68 |
| ReadInterimRecordCountStall | Represents the event of a stall when reading interim record counts. | 69 |
| ReadRecordCount | Represents the count of records read. | 70 |
| ReadRecordDataError | Represents an error when reading record data. | 71 |
| ReadRecordErrorCount | Represents the count of errors when reading records. | 72 |
| RenamingObject | Represents the event of renaming an object. | 73 |
| SchemaValidationWarning | Represents a warning during schema validation. | 95 |
| SkippingAllMembers | Represents the event of skipping all members. | 74 |
| SkippingDataArea | Represents the event of skipping a data area. | 75 |
| SkippingDir | Represents the event of skipping a directory. | 76 |
| SkippingDirContents | Represents the event of skipping directory contents. | 77 |
| SkippingElementWithPath | Represents the event of skipping an element with a path. | 78 |
| SkippingExistingDir | Represents the event of skipping an existing directory. | 79 |
| SkippingFile | Represents the event of skipping a file. | 80 |
| SkippingMember | Represents the event of skipping a member. | 81 |
| SkippingOnUserRequest | Represents the event of skipping on user request. | 84 |
| SkippingReadText | Represents the event of skipping reading text. | 82 |
| SkippingStarFieldRefFile | Represents the event of skipping the export of a StarFieldRefFile. | 90 |
| SkippingUnknownObject | Represents the event of skipping an unknown object. | 83 |
| StarFileMemberExport | Represents the event of a member export in a StarFile. | 92 |
| StarFirstMemberExport | Represents the event of the first member export in a StarFile. | 91 |
| WriteInterimRecordCount | Represents the count of interim records written. | 85 |
| WriteInterimRecordCountClose | Represents the event of closing after writing interim record counts. | 86 |
| WriteInterimRecordCountStall | Represents the event of a stall when writing interim record counts. | 87 |
| WritingAttr | Represents the event of writing an attribute. | 88 |
| WritingContent | Represents the event of writing content. | 89 |
| zzzLastMsgType | Represents the last message type in the enumeration. | 96 |
