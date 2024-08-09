---
title: "XmlOptions enum               | QSYS API Reference Guide"
description: "Enumerate the possible options for an XML operation. "
last_modified_at: 2024-08-09T16:18:40Z
---

Enumerate the possible options for an XML operation.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| CreateObjects | Read option to create root object and specified sub-objects to the database as read. | 65536 |
| Default | Default option. | 0 |
| DontValidate | Read option to prevent validation step if the XmlReader provided is not an instance of XmlValidatingReader. | 524288 |
| IgnoreDuplicateDirs | Read option to ignore if a library to be created in the database already exists there. | 2097152 |
| IgnoreDuplicates | Read option to ignore if an object to be created in the database already exists there. | 262144 |
| MergeMembers | Write option to merge the data of all members into the exported member (note that the merge ignores any data constraints defined by the file). Ignored unless OnlyOneMember is set. If not set, only data of the member of the same name as the file OR *first is exported. | 134217728 |
| OnlyOneMember | Write option to create file export suitable for DSS import by only exporting one member per file, as specified by the MergeMembers option. The exported member will have the same name as the file. Ignored unless WithMembers is set. | 67108864 |
| RelativeBasePaths | Write option to give path of a base object relative to the root path if it is contained by the root object. | 16777216 |
| RemoveFieldReferenceInfo | Read option to remove field reference file info from the file def prior to creation of a physical file. | 1048576 |
| RetainObjectTree | Read option where IAdgObject containers are populated with read objects. | 131072 |
| SkipBadData | Write option to handle FormatException internally if WithData and FormatException is found. | 33554432 |
| UseStarFileForMbrData | Read option for DSS databases to only add member data when the source member has the same name as the file (otherwise, use *FIRST). | 4194304 |
| WithDataAreas | Option to include data areas. | 256 |
| WithDirectories | Option to include directories. | 32 |
| WithFiles | Option to include files. | 92 |
| WithLogicalData | Option to include logical data. | 128 |
| WithLogicalFiles | Option to include logical files. | 8 |
| WithMembers | Option to include members. | 2 |
| WithNetPrintFiles | Option to include network print files. | 64 |
| WithOlePrintFiles | Option to include OLE print files. | 16 |
| WithPhysicalData | Option to include physical data. | 1 |
| WithPhysicalFiles | Option to include physical files. | 4 |
| WithPrintFiles | Option to include print files. | 80 |
| WithSubObjects | Option to include sub-objects. | 65535 |
