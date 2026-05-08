---
title: "Support for IFS and DLO"
description: "Dive into the essentials of Integrated File System (IFS) and Document Library Objects (DLO). Learn their roles, differences, and how to the new implementation works."
---

## IFS - Integrated File System

The Integrated File System (IFS) is a part of the IBM® i operating system that supports stream input/output and storage management similar to personal computer and UNIX operating systems.

The IFS is a hierarchical organization of stream files on the computer. The branches of the structure are directories while the leaves are directories and files.

The property `IFSRoot` of the `Monarch.Job` holds the Window's folder where the job will find the 'root' of the IFS structure.

For more details on the IFS, please see these IBM links:

[Integrated File System](https://www.ibm.com/docs/en/i/7.3?topic=systems-integrated-file-system)

[File system comparison](https://www.ibm.com/docs/en/i/7.3?topic=systems-file-system-comparison)

## DLO – Document Library Objects

The IBM i also provides a facility called Document Library Objects (DLO) which contents behave similar to IFS files in that they both are stream files instead of the structured files that the database on the IBM i provides. A nomenclature difference is that DLO calls Directories, Folders and knows Files as Documents.

On the IBM i, the DLO objects can be accessed via the Document Library Services File System reachable in the IFS at the /QDLS link. In Monarch programs, the DLO objects can be found via the property QDLSRoot which resolves to the concatenation of the IFSRoot property and the literal "/QDLS".

According to IBM,

>QDLS is an old file system, dating from the System/36 and System/38 days. It is maintained mostly for backward compatibility. Some applications are hard-coded to store and access PC files in the QDLS file system. Companies using those applications will be required to use the QDLS file system, to upgrade to a newer version of the current application software (one that supports the use of the "root" file system), or to migrate to a different application.

And also:

>Document Library Objects (DLOs) object types include DOC and FLR. They are found within the QDLS file system. Although the objects themselves are stored in library QDOC (in the QSYS.LIB file system), they should never be accessed through the QDOC library. They are not typical iSeries objects and should always be accessed by means of the QDLS file system.

For more details on the QDLS, please see these IBM links:

[QDLS](https://www.ibm.com/docs/en/i/7.3?topic=systems-document-library-services-file-system-qdls)

[Comparison of the QDLS and "Root" File Systems for Storing User Documents and Other PC Files](https://www.ibm.com/;www-01.ibm.com/support/docview.wss?uid=nas8N1015584)

## IFS Related Commands

The following IFS commands are recognized and migrated by Monarch. Only a subset of keywords and special values are supported as noted on the next table.

### Directory Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CRTDIR or <br/> MD or <br/> MKDIR | DIR | | **Create Directory** <br/> Adds a new directory to the system. |
| RMVDIR or <br/> RD or <br/> RMDIR | DIR <br/> SUBTREE <br/> RMVLNK |  | **Remove Directory** <br/> Removes a specified directory from the system after all objects in the directory have been unlinked and the directory is no longer in use. If a directory to be removed contains objects, this command optionally unlinks all of the objects and then deletes the directory. |
| CHGCURDIR or <br/> CD or <br/> CHDDIR | DIR |  | **Change Current Directory** <br/> Designates a directory to be the Current directory. The current directory, set with this command, affects only the IFS commands (listed on this table). |
| DSPCURDIR | OUTPUT(\*PRINT) |  | **Display Current Directory** <br/> Prints the current working directory onto the default output queue on a QSYSPRT file. |

### Object Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CPY or <br/> COPY | OBJ <br/> TODIR <br/> TOOBJ <br/> SUBTREE <br/> REPLACE | | **Copy Object** <br/> Copies a single object or a group of objects specified by an object name pattern.The copy command can also be used to copy a directory tree where the specified directory, its contents, and the contents of all of its subdirectories are copied. If SUBTREE(\*ALL) is specified, the command will attempt to copy as many objects as possible within the subtree. |
|RNM or <br/> REN | OBJ <br/> NEWOBJ | | **Rename Object** <br/> Changes the name of a single object in a directory. |
| MOV or <br/> MOVE | OBJ <br/> TODIR <br/> TOOBJ <br/> DTAFMT |  | **Move Object** <br/> Moves an object from the directory it is into a different directory. |


### Import / Export Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CPYFRMSTMF | FROMSTMF <br/> TOMBRMBROPT <br/> ENDLINFMT <br/> TABEXPN | | **Copy From Stream File** <br/> Copies the data in a stream file to a database file member with potential reformatting. |
| CPYTOSTMF | FROMMBR <br/> TOSTMF <br/> STMFOPT <br/> ENDLINFMT |  | **Copy To Stream File** <br/> Copies a database file member to a stream file. The data can be reformatted as part of the copy. |
| CPYFRMIMPF | FROMSTMF <br/> TOFILE <br/> MBROPT <br/> STMFLEN <br/> RCDDLM <br/> DTAFMT <br/> STRDLM <br/> STRESCCHR <br/> RMVBLANK <br/> FLDDLM <br/> FLDDFNFILE <br/> DECPNT <br/> DATEFMT <br/> DATSEP <br/> TIMFMT <br/> TIMSEP <br/> FROMRCD |  | **Copy From Import File** <br/> Copies all or part of a stream file to a database file member. The stream file is an import file originally created for the purpose of copying data between heterogeneous databases. |
| CPYTOIMPF | FROMFILE <br/> TOSTMF <br/> MBROPT <br/> RCDDLM <br/> DTAFMT <br/> STRDLM <br/> STRESCCHR <br/> RMVBLANK <br/> FLDDLM <br/> DECPNT <br/> DATEFMT <br/> TIMFMT |  | **Copy To Import File** <br/> Copies a database file member to a stream file. The stream file is an 'import file' created for the purpose of copying data between heterogeneous databases. |

## DLO Related Commands

The following DLO commands are recognized and migrated by Monarch. Only a subset of keywords and special values are supported as noted on the next table.

### Document Library Object Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CHKDLO | DLOFLR | DLO.Check IN PROGRESS | **Check Document Library Object** Verifies that an object exists and that a user has authority to the object before trying to access it. |
| DLTDLO | DLO (Name or \*ALL)FLR | | **Delete Document Library Object** Allows you to delete a document or a folder. |
| RNMDLO | DLO <br/> NEWDLO <br/> FLR | DLO.Rename | **Rename Document Library Object** Changes the name of a document or folder. |

### Document Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CPYDOC | FROMDOC <br/> FROMFLR <br/> TODOC <br/> TOFLR <br/> REPLACE | | **Copy Document** Allows you to copy a document from one folder into another folder or to copy a document that is not in a folder into a folder. |
| MOVDOC | FROMDOC <br/> FROMFLR <br/> TOFLR <br/> RENAME | DLO.Move | **Move Document** Move the document to a new folder and can rename the document in the process |

### Folder Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CRTFLR | FLR <br/> INFLR | DLO.CreateFolder | **Create Folder** <br/> Creates a Folder in another folder. |
| DSPFLR | FLR <br/> TYPE <br/> OUTPUT(\*PRINT or \*OUTFILE) <br/> LEVEL <br/> OUTFILE <br/> OUTMBR <br/> OUTFILFMT | | **Display Folder** <br/> Allows you to print a list of folders and documents, or to create an output file that contains the list of folders or documents. |

### Import / Export Commands

| **Command** | **Keywords** | **Implementation** | **Notes** |
| --- | --- | --- | --- |
| CPYFRMPCD | FROMFLR <br/> TOFILE <br/> FROMDOC <br/> TOMBR <br/> MBROPT <br/> TRNFMT | | **Copy From PC Document**  <br/> Copies the data in a document to a database file. |
| CPYTOPCD | FROMFILE <br/> TOFLRF <br/> ROMMBR <br/> TODOC <br/> REPLACE <br/> TRNFMT | | **Copy to PC Document**  <br/> Copies a database file member to a document in a folder. |
