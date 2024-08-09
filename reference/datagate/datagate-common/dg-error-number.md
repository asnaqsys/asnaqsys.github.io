---
title: "dgErrorNumber enum            | QSYS API Reference Guide"
description: "Represents the different error numbers generated as a result of Acceler8DB or Datagate/400 server errors. These errors occur programmatically on the s"
last_modified_at: 2024-08-09T16:18:40Z
---

Represents the different error numbers generated as a result of Acceler8DB or Datagate/400 server errors. These errors occur programmatically on the server computer to indicate a condition.  In general, these are "true errors", and only in a few cases do they signify a normal condition.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| dgALTXLAT | Represents alternate encoding text translation support errors. | 1700 |
| dgEaBADACCESS | Represents a bad access error. | 110 |
| dgEaBADFARM | Represents a bad farm error. | 132 |
| dgEaBADFD | Represents a bad file descriptor error. | 109 |
| dgEaBADFRMT | Represents an invalid format error. | 125 |
| dgEaBADFRMTID | Represents a bad format ID error. | 123 |
| dgEaBADGROVE | Represents a bad grove error. | 112 |
| dgEaBADIDX | Represents a bad index error. | 131 |
| dgEaBADREC | Represents a bad record error. | 105 |
| dgEaBUSYFILE | Represents a file is busy error. | 107 |
| dgEaBUSYREC | Represents a record is busy error. | 108 |
| dgEACCESS | Represents access errors. | 100 |
| dgEaCORRFARM | Represents an error where the data file is corrupted (File Length not multiple of Record Length). | 138 |
| dgEaCORRNODE | Represents a corrupted node encounter error. | 135 |
| dgEaDEADLOCK | Represents a deadlock error. | 114 |
| dgEaDUPKEY | Represents a duplicate key error. | 101 |
| dgEaEOF | Represents an end of file error. | 106 |
| dgEaIDXFNOTFND | Represents an index file not found error. | 134 |
| dgEaIDXNOTFND | Represents an index not found error. | 113 |
| dgEaINTERRUPT | Represents an interrupt received error. | 120 |
| dgEaINVARG | Represents an invalid access argument error. | 111 |
| dgEaINVBFOPEN | Represents a blocking factor attribute not allowed with files opened for output error. | 133 |
| dgEaINVDATETIMEDATA | Represents an error where the contents of date/time field has invalid data format. | 142 |
| dgEaINVDMOP | Represents an invalid operation on database open exclusively for monitoring error. | 136 |
| dgEaINVFTOP | Represents an invalid operation for file type error. | 130 |
| dgEaINVINST | Represents an invalid instruction error. | 129 |
| dgEaINVJOINCURSOR | Represents an error where an invalid ServerCursor was selected for Join File in SQL Server. | 147 |
| dgEaINVLOCKTOGGLE | Represents an error where it's not possible to toggle Lock/NoLock record on sequential read in SQL Server. | 146 |
| dgEaINVMANLOCKS | Represents an error where DG on SQL Server does not support opening files with Manual Locks, use Automatic Locks. | 145 |
| dgEaINVMODE | Represents an invalid mode error. | 122 |
| dgEaINVNOLOCK | Represents an error where NoLock reads on update files are not supported in SQL Server. | 141 |
| dgEaINVNUMERICDATA | Represents an error where the contents of numeric field has invalid data format. | 143 |
| dgEaINVTYPE | Represents an invalid type error. | 102 |
| dgEaIOERROR | Represents an I/O error. | 117 |
| dgEaKEYNOTFND | Represents an error where the key field is not found. | 139 |
| dgEaMAXFILES | Represents a maximum files opened error. | 119 |
| dgEaNEEDFRMT | Represents a need format for this operation error. | 126 |
| dgEaNOCURR | Represents a no current record error. | 116 |
| dgEaNOFILE | Represents a file not found error. | 118 |
| dgEaNOLOCK | Represents a record not locked by caller error. | 115 |
| dgEaNOSPACE | Represents a no space available error. | 121 |
| dgEaNOTFND | Represents a not found error. | 103 |
| dgEaNOTINDEX | Represents a not open for index access error. | 124 |
| dgEaNOTINDEXED | Represents an error where an attempt was made to open a non-indexed file for index processing. | 140 |
| dgEaNOTUPD | Represents an error where the file is not open for update operations. | 144 |
| dgEAPPC | Represents APPC Errors. | 800 |
| dgEaRECDEL | Represents a record deleted error. | 104 |
| dgEaRECPREVLCK | Represents an error where the record is already locked to this job. | 137 |
| dgEaSTKOVF | Represents a stack overflow error. | 127 |
| dgEaSTKUNF | Represents a stack underflow error. | 128 |
| dgEbINVALIDFACT | Represents an error where the configured alternate text translation provider is invalid. | 1703 |
| dgEbMISSFACT | Represents an error where the configured alternate text translation provider type is not found. | 1702 |
| dgEbNOFACTORY | Represents an error where there is a configured alternate text translation provider loading error. | 1701 |
| dgEcADDIDX | Represents an error adding an index. | 407 |
| dgECALLPARM | Represents call/parameter errors. | 700 |
| dgECATALOG | Represents a catalog error. | 50 |
| dgEcBADREFFILE | Represents an error where the field reference file must be a physical file. | 430 |
| dgEcBADSRC | Represents a bad source error. | 401 |
| dgEccIOERR | Represents an error where an unrecoverable I/O error occurred in commit/rollback operation. | 1402 |
| dgEccIORECERR | Represents an error where a recoverable I/O error occurred in commit/rollback operation. | 1401 |
| dgEcCLONEDFORMAT | Represents an error where the format has a fixed set of fields, those of the base file. | 428 |
| dgEcCRTACF | Represents an error creating an access file. | 406 |
| dgEcCRTACP | Represents an error creating an access program. | 418 |
| dgEcFLDEXISTS | Represents an error where a field already exists in the format. | 419 |
| dgEcFLDINVDEC | Represents an invalid field decimal error. | 416 |
| dgEcFLDINVFMT | Represents an invalid field format error. | 422 |
| dgEcFLDINVINT | Represents an invalid field integral error. | 417 |
| dgEcFLDINVLEN | Represents an invalid field length error. | 415 |
| dgEcFLDNOTFND | Represents a field not found error. | 414 |
| dgEcFLDTYPENONNULL | Represents an error where the field type is not null capable. | 433 |
| dgEcFORMATEXISTS | Represents an error where a format already exists in the file. | 421 |
| dgEcFORMATNOTFND | Represents a format not found error. | 420 |
| dgECHANBUSY | Represents a channel busy error. | 10 |
| dgEcINVCONCAT | Represents an invalid CONCAT definition error. | 440 |
| dgEcINVCONST | Represents an invalid constant error. | 408 |
| dgEcINVCONSTLEN | Represents an invalid constant length error. | 409 |
| dgEcINVDER | Represents an invalid derivation error. | 423 |
| dgEcINVDERDBCS | Represents an invalid derivation, base field length invalid error. | 427 |
| dgEcINVDERDEC | Represents an invalid derivation, decimals not 0 error. | 425 |
| dgEcINVDERSIZ | Represents an invalid derivation, sizes don't match error. | 424 |
| dgEcINVFILETYPE | Represents an error where the file type is not recognized as valid. | 439 |
| dgEcINVFLDREMAP | Represents an error where a field cannot be remapped in the file description. | 441 |
| dgEcINVINST | Represents an invalid instruction error. | 404 |
| dgEcINVJOINLEN | Represents an error where fields in join definition exceed key length supported by the platform. | 435 |
| dgEcINVKEYFORFILE | Represents an error where the key usage is invalid for this file type. | 432 |
| dgEcINVKEYLEN | Represents an error where the key length is longer than supported by the platform. | 434 |
| dgEcINVKEYREMAP | Represents an error where a key cannot be remapped in the file description. | 442 |
| dgEcINVOPTYPE | Represents an invalid operation for field type error. | 426 |
| dgEcNEWVERSION | Represents an error where the file definition version is newer than supported by this release. | 431 |
| dgEcNONULLSUPPORT | Represents an error where null fields are not supported by the server. | 437 |
| dgEcNOREFFILE | Represents a field reference file not found error. | 429 |
| dgEcNOTALL | Represents an error where not all fields could be processed. | 436 |
| dgEcNOVARLENSUPPORT | Represents an error where variable length fields are not supported by the server. | 438 |
| dgEcNUMEXP | Represents an error where a number was expected. | 402 |
| dgECOMMAND | Represents command errors. | 1100 |
| dgECOMMITCTL | Represents commitment control errors. | 1400 |
| dgECOMPILER | Represents compiler errors. | 400 |
| dgEcOPEREXP | Represents an error where an operand was expected. | 411 |
| dgEcOPNACF | Represents an error opening an access file. | 405 |
| dgEcOPNTYPE | Represents an operand type error. | 403 |
| dgEcQUOTEXP | Represents an error where a quotation was expected. | 412 |
| dgEcRPAREXP | Represents an error where a ')' was expected. | 410 |
| dgEcSQL400FILE | Represents an error where SQL logical files are not supported. | 443 |
| dgEcSQLROFIELD | Represents an error where SQL table read-only fields are only supported for 0-decimal numeric types. | 444 |
| dgEcVAREXP | Represents an error where a variable was expected. | 413 |
| dgEdbBADLIBL | Represents an error where the library list has a bad format. | 1027 |
| dgEdbCONVUNAVAIL | Represents an error where CCSID conversion is unavailable. | 1012 |
| dgEdbDGMEMSRV | Represents an error where the dgmemsrv process could not be created. | 1004 |
| dgEdbDUPDB | Represents an error where a duplicate database was found. | 1013 |
| dgEdbDUPLIBLE | Represents an error where a duplicate library list entry was found. | 1022 |
| dgEdbEXCLUSIVE | Represents an error where the database is locked for exclusive use. | 1020 |
| dgEdbLIMIT | Represents an error where too many databases are registered. | 1003 |
| dgEdbMAPCREATE | Represents an error where the registry shared memory file creation failed. | 1007 |
| dgEdbMAPOPEN | Represents an error where the registry shared memory open operation failed. | 1006 |
| dgEdbMAPVIEW | Represents an error where the registry shared memory view mapping failed. | 1008 |
| dgEdbMAXLIBL | Represents an error where the library list reached its maximum capacity. | 1023 |
| dgEdbMUTEXNOTFOUND | Represents an error where the system mutex object was not found. | 1001 |
| dgEdbMUTEXWAIT | Represents an error where the database startup procedure failed due to a system mutex wait error. | 1002 |
| dgEdbNODBCSSUPP | Represents an error where DBCS is unsupported in this version. | 1011 |
| dgEdbNODBNAME | Represents an error where the database name was not found. | 1019 |
| dgEdbNOINITLIBL | Represents an error where the initial library list was not set. | 1021 |
| dgEdbNOLABEL | Represents an error where the requested database label doesn't exist. | 1016 |
| dgEdbNOLIBL | Represents an error where the library list was not found. | 1026 |
| dgEdbNOQCCSID | Represents an error where the QCCSID system value could not be retrieved. | 1010 |
| dgEdbNOREPAIR | Represents an error where dgFixDB wouldn't start. | 1015 |
| dgEdbNOTALLLIBL | Represents an error where at least one library was not set in the library list. | 1025 |
| dgEdbNOTINLIBL | Represents an error where a library was not found in the library list. | 1024 |
| dgEdbREGCREATE | Represents a system error creating the database label. | 1014 |
| dgEdbREGDELETEDB | Represents an error where the operation did not complete; the registry entries could not be removed. | 1017 |
| dgEdbREGDENIED | Represents an error where there are insufficient access permissions on the registry. | 1018 |
| dgEdbREGFILEDIR | Represents an error where the registration file directory was not found. | 1005 |
| dgEdbSYNC | Represents an error where unprotected registry access is not allowed. | 1009 |
| dgEDELERROR | Represents a delete error. | 3 |
| dgEDEVICENAME | Represents an error where the device name is not available. | 20 |
| dgEEXCEPTION | Represents an unexpected exception error. | 9 |
| dgEEXPANDFS | Represents an expand file system error. | 5 |
| dgEfirstError | Represents the first error.  | 0 |
| dgEgBADAP | Represents a bad access program stream error. | 53 |
| dgEgBADATTR | Represents a bad creation attribute stream error. | 59 |
| dgEgBADAUTH | Represents an error where the authorization record is bad. | 77 |
| dgEgBADDEPEND | Represents a bad dependency stream error. | 67 |
| dgEgBADEXT | Represents a bad extension stream error. | 69 |
| dgEgBADFARM | Represents a bad farm stream error. | 65 |
| dgEgBADFDEF | Represents a bad file definition stream error. | 55 |
| dgEgBADGROVE | Represents a bad grove stream error. | 63 |
| dgEgBADMATTER | Represents a bad matter stream error. | 61 |
| dgEgBADPP | Represents a bad path program stream error. | 57 |
| dgEgBADREL | Represents a bad relations stream error. | 51 |
| dgEgBADTEXT | Represents a bad text stream error. | 71 |
| dgEgCANTAUTH | Represents an error where the system could not add a security record. | 76 |
| dgEgCORRFDEFC | Represents an error where the file definition cache member is corrupt. | 84 |
| dgEgINVVOLPATH | Represents an error where the volume directory path is invalid. | 81 |
| dgEgNEWDB | Represents an error where the database is newer than supported by this version. | 74 |
| dgEgNOAP | Represents an error where no access program stream exists. | 54 |
| dgEgNOATTR | Represents an error where no creation attribute stream exists. | 60 |
| dgEgNOAUTHLOCK | Represents an error where the system could not lock the security record. | 79 |
| dgEgNOCATALOG | Represents an error where the database's catalog could not be opened. | 75 |
| dgEgNODBAUTH | Represents an error where the user is not authorized to the database. | 80 |
| dgEgNODEPEND | Represents an error where no dependency stream exists. | 68 |
| dgEgNOEXT | Represents an error where no extension stream exists. | 70 |
| dgEgNOFARM | Represents an error where no farm stream exists. | 66 |
| dgEgNOFDEF | Represents an error where no file definition stream exists. | 56 |
| dgEgNOGROVE | Represents an error where no grove stream exists. | 64 |
| dgEgNOMATTER | Represents an error where no matter stream exists. | 62 |
| dgEgNONSECUREDB | Represents an error where the database is not secure. | 78 |
| dgEgNOPP | Represents an error where no path program stream exists. | 58 |
| dgEgNOREL | Represents an error where no relations exist. | 52 |
| dgEgNOTEXT | Represents an error where no text stream exists. | 72 |
| dgEgOLDDB | Represents an error where the database is older than supported by this version. | 73 |
| dgEgOSNOTSECURE | Represents an error where a secure database was attempted to be opened from an insecure operating system. | 83 |
| dgEgVOLNOTSECURE | Represents an error where the volume's file system is not secure capable. | 82 |
| dgEiCONNLOST | Represents an error where the TCP/IP Connection was terminated unexpectedly. The Server was probably shut down. | 913 |
| dgEiDG8START | Represents an error where the Datagate job could not be started; check DG8SVCPRF job spooled-file output and user profile settings. | 914 |
| dgEiHOSTNOTFND | Represents an error where the remote TCP/IP host was not found. | 908 |
| dgEiNETDOWN | Represents an error where the TCP/IP Network subsystem has failed. | 910 |
| dgEiNETUNREACH | Represents an error where the TCP/IP network could not be reached from this machine. | 911 |
| dgEiNOBIND | Represents an error where a socket cannot be bound. | 902 |
| dgEiNORESPONSE | Represents an error where the Server Machine or the ADB/DG Service did not respond. | 912 |
| dgEiNORMTTCPIPSUPPORT | Represents an error where connecting to a remote database with TCP/IP is not supported on this platform. | 906 |
| dgEiNOSERVER | Represents an error where a connection to the database server cannot be established. | 903 |
| dgEiNOSOCKET | Represents an error where a socket cannot be obtained. | 901 |
| dgEINTERNAL | Represents an internal error. | 7 |
| dgEINVARG | Represents an invalid argument error. | 8 |
| dgEINVHANDLE | Represents an invalid handle error. | 6 |
| dgEINVPLATFORM | Represents an error where the platform SQL Server is not supported with this version. | 18 |
| dgEiRESOLVER | Represents a TCP/IP resolver error. | 909 |
| dgEiSERVERSTART | Represents an error where the database server process could not be started. | 905 |
| dgEiSOCKETIO | Represents a socket I/O error. | 904 |
| dgEiTCPDOWN | Represents an error where the TCP/IP subsystem is not currently available. | 907 |
| dgEiTLNTCNCT | Represents an error where a connection to the DataGate/400 host's TELNET server could not be established. | 915 |
| dgEiTLNTPORT | Represents an error where the port of the connected TELNET socket could not be obtained. | 916 |
| dgELastError | Represents the last error. | 1906 |
| dgELICENSE | Represents license management errors. | 1200 |
| dgEm400OBJNAMELEN | Represents an error where object names on this database server may not exceed 10 characters in length. | 672 |
| dgEmANOTFND | Represents an error where the access path was not found. | 605 |
| dgEmARCCHKSUMWRONG | Represents an error where the archive checksum is wrong, indicating the archive is corrupted. | 651 |
| dgEmARCFAILI | Represents an error where data could not be restored due to an input error. | 649 |
| dgEmARCFAILO | Represents an error where data could not be saved due to an output error. | 650 |
| dgEmBADARCHTYPE | Represents an error where the Archive Type is not supported. | 674 |
| dgEmBADCAT | Represents an error where the catalog is broken. | 634 |
| dgEmBADFRMTID | Represents an error where the base file has an invalid format ID. | 637 |
| dgEmBASENOTPH | Represents an error where the base file is not physical. | 638 |
| dgEmBUSYOBJ | Represents an error where the Object is Busy. | 681 |
| dgEmCANCEL | Represents an error where the operation was canceled by the user. | 673 |
| dgEmCLIENTNOTFND | Represents an error where the Client was not found. | 679 |
| dgEmCORRDATFIL | Represents an error where corrupted system data was encountered in a member. Retry after using ADB Database Manager's Fix Index tool. | 648 |
| dgEmCORRENV | Represents an error where the environment is corrupted. | 612 |
| dgEmCRTSHM | Represents an error creating the Shared Memory File. | 668 |
| dgEmCRTSHMLOCK | Represents an error where the Shared Memory File cannot be created because it is locked by another program. | 666 |
| dgEmCRTSHMMAP | Represents an error creating the Shared Memory File Mapping. | 669 |
| dgEmCRTSHMPATH | Represents an error where the Shared Memory File cannot be created because the path to the database doesn't exist. | 667 |
| dgEmDIRNOTEMPTY | Represents an error where the directory is not empty. | 644 |
| dgEmDIRTYENV | Represents an error where the environment is dirty. | 611 |
| dgEmDNOTFND | Represents an error where the directory was not found. | 602 |
| dgEmDUPINDEX | Represents an error where the index is a duplicate. | 623 |
| dgEmDUPNOTFND | Represents an error where the duplicate base was not found. | 636 |
| dgEmDUPOBJ | Represents an error where the object is a duplicate. | 606 |
| dgEmEMPTYARC | Represents an error where an empty archive unit cannot be saved. | 687 |
| dgEmENVEXISTS | Represents an error where the environment already exists. | 609 |
| dgEmEOFSAVEREST | Represents an error where the end of the save/restore file has been reached. | 615 |
| dgEmERRAUTH | Represents an error found when dealing with authority. | 662 |
| dgEmFILENOTOPEN | Represents an error where the File is not open. | 680 |
| dgEmFNOTFND | Represents an error where the file was not found. | 603 |
| dgEMGTOBJ | Represents object management errors. | 600 |
| dgEmHASDEPEND | Represents an error where the object has dependents. | 614 |
| dgEmINCOMPLETE | Represents an error where the operation did not complete. | 622 |
| dgEmINUSEBYYOU | Represents an error where the object is in use by the current user. | 675 |
| dgEmINV400OP | Represents an invalid operation against AS/400 server. | 645 |
| dgEmINVBASECOUNT | Represents an error where the number of bases is invalid. | 625 |
| dgEmINVDIRNAME | Represents an error where the directory name is invalid. | 641 |
| dgEmINVFILENAME | Represents an error where the file name is invalid. | 642 |
| dgEmINVFOP | Represents an error where the file operation is invalid. | 639 |
| dgEmINVMEMBNAME | Represents an error where the member name is invalid. | 640 |
| dgEmINVOBJ | Represents an error where the object is invalid. | 607 |
| dgEmINVOBJNAME | Represents an error where the object name is invalid. | 643 |
| dgEmINVOTYPE | Represents an error where the object type is invalid. | 608 |
| dgEmINVOWNER | Represents an error where the owner is invalid. This account may not be assigned as the owner of this object. | 661 |
| dgEmINVPRTFILE | Represents an error where the file is not a valid Acceler8DB print file. | 652 |
| dgEmINVSQLOP | Represents an invalid operation against SQL Server. | 646 |
| dgEmINVTAROBJNAME | Represents an error where the target object name is invalid. | 626 |
| dgEmINVUSER | Represents an error where the user account is invalid. | 660 |
| dgEmLCKNOTFND | Represents an error where the Object Lock was not found. | 678 |
| dgEmLIBLTARGET | Represents an error where *LIBL can't be the target directory. | 686 |
| dgEmMAPSHM | Represents an error mapping view of the Shared Memory File. | 670 |
| dgEmMAXMEM | Represents an error where the maximum number of members has been reached. | 624 |
| dgEmMAXMERGE | Represents an error where the maximum number of merged members over a physical has been reached. | 632 |
| dgEmMISSMATCHBASE | Represents an error where the base member's file does not match the file's base. | 647 |
| dgEmMNOTFND | Represents an error where the member was not found. | 604 |
| dgEmNOBASEAUTH | Represents an error where the user is not authorized to the base object for this operation. | 663 |
| dgEmNODIRADD | Represents an error where the user is not authorized to add objects to the directory. | 656 |
| dgEmNODIRDEL | Represents an error where the user is not authorized to delete objects from the directory. | 657 |
| dgEmNODIRREAD | Represents an error where the user is not authorized to read objects in the directory. | 655 |
| dgEmNOENV | Represents an error where the environment doesn't exist. | 610 |
| dgEmNOLOCK | Represents an error where the Object is not locked by the caller. | 682 |
| dgEmNOMEMADD | Represents an error where the user is not authorized to add members to the file. | 664 |
| dgEmNOMEMDEL | Represents an error where the user is not authorized to delete members from the file. | 665 |
| dgEmNONEXISTAUTH | Represents an error where the user cannot revoke non-existing authorities. | 659 |
| dgEmNOOBJAUTH | Represents an error where the user is not authorized to the object for this operation. | 654 |
| dgEmNOPARENTUPD | Represents an error where the user is not authorized to update objects in the parent directory. | 658 |
| dgEmNOPATHAUTH | Represents an error where the user is not authorized to the path. | 653 |
| dgEmNOPERMINTEMP | Represents an error where a permanent object can't reside in a temporary directory. | 677 |
| dgEmNOSEMS | Represents an error where the requested number of semaphores cannot be obtained. | 627 |
| dgEmNOTEMPTY | Represents an error where the directory is not empty. | 613 |
| dgEmNOTFND | Represents an error where the object was not found. | 601 |
| dgEmNOTONQTEMP | Represents an error where the operation is not valid on QTemp. | 676 |
| dgEmNOTSAME | Represents an error where the device or file system is not the same. | 633 |
| dgEmOPENSHM | Represents an error opening the Shared Memory File. | 671 |
| dgEmPROCACTIVE | Represents an error where the process is active. | 631 |
| dgEmPROCNOTFND | Represents an error where the process was not found. | 630 |
| dgEmQUSCRTUQ | Represents an error where the QUSCRTUQ create user queue OS/400 api failed. | 683 |
| dgEmRMGSHM | Represents an error where the global shared memory cannot be removed. | 629 |
| dgEmRMSEM | Represents an error where the semaphore ID cannot be removed. | 628 |
| dgEmRNOBJUSRQ | Represents an error where the RNMOBJ OBJTYPE(*USRQ) failed to rename the user queue. | 684 |
| dgEmROOTDIR | Represents an error where an invalid operation was performed on the root directory. | 635 |
| dgEmRSLVSPUSRQ | Represents an error where the RSLVSP(_Usrq) failed to get the user queue pointer. | 685 |
| dgEmSRCORRDATA | Represents an error where the save/restore data is corrupted. | 618 |
| dgEmSRINVMODE | Represents an error where the save/restore mode is invalid. | 617 |
| dgEmSRINVORD | Represents an error where the block order is invalid. | 620 |
| dgEmSRINVSYS | Represents an error where the source or target machine is incompatible. | 621 |
| dgEmSRINVVER | Represents an error where the save/restore version is invalid. | 619 |
| dgEmSRNOTCOMP | Represents an error where the save/restore is not complete. | 616 |
| dgEnAddingMember | Represents an error adding a member. | 1109 |
| dgEnAddingRecord | Represents an error adding a record. | 1116 |
| dgEnCantCreateLF | Represents an error where logical files cannot be created using CopyData; Use Copy Logical File instead. | 1131 |
| dgEnCDNOCOMMONFLDS | Represents an error where source and destination files must have at least one common field name. | 1127 |
| dgEnCDNODROPFLDS | Represents an error where source and destination files have different field names and the 'Drop Fields' option was not set. | 1128 |
| dgEnCDSRCNOTPHY | Represents an error where a source file must be physical when mapping fields. | 1126 |
| dgEnCharExpected | Represents an error where a character was expected. | 1114 |
| dgEnCopyToSelf | Represents an error where a copy to self operation was attempted. | 1121 |
| dgEnDateExpected | Represents an error where a date value was expected. | 1123 |
| dgEnDelimeterExpected | Represents an error where a delimiter was expected. | 1112 |
| dgEnDifferentFrmtId | Represents an error where source and destination files have different Format IDs. | 1132 |
| dgENEGOAUTHEXC | Represents a client-initiated negotiate security authentication failure. Further details in inner exception and target server logs. | 23 |
| dgENEGOHANDSHK | Represents a negotiate handshake error. Code: %d, Status: %ul, Facility: %s. | 22 |
| dgENEGOINVOKE | Represents a negotiate initialization error. Code: %d, Status: %ul, Facility: %s. | 21 |
| dgEnEndOfArchiveUnit | Represents an error at the end of an archive unit. | 1120 |
| dgEnFromFileNotFnd | Represents an error where the from-file was not found. | 1117 |
| dgEnHexExpected | Represents an error where a hexadecimal value was expected. | 1122 |
| dgEnInDefinition | Represents an error in the definition. | 1104 |
| dgEnInvalidFieldType | Represents an error with an invalid field type. | 1106 |
| dgEnInvalidFromFileType | Represents an error with an invalid from-file type. | 1133 |
| dgEnInvalidToFileType | Represents an error with an invalid to-file type. | 1134 |
| dgEnMultiFormat | Represents an error with multiple formats. | 1103 |
| dgEnNoMemory | Represents an error where there is no memory available. | 1105 |
| dgEnNumberExpected | Represents an error where a number was expected. | 1113 |
| dgENOATLASCTX | Represents an internal error with no Atlas context. | 15 |
| dgENODATAAREAS | Represents an error where data area access is not supported by this database. | 19 |
| dgENOMEM | Represents a no memory available error or database memory exhausted. Try increasing the memory size in the 'Work with Databases' dialog in Database Manager. | 4 |
| dgENONPRVSERVER | Represents a server account not privileged error. Security context not established. | 12 |
| dgEnOpenFileDef | Represents an error opening the file definition. | 1102 |
| dgEnOpeningFile | Represents an error opening a file. | 1108 |
| dgEnOpeningFromFile | Represents an error opening the from-file. | 1135 |
| dgEnOpeningToFile | Represents an error opening the to-file. | 1136 |
| dgENOTEMPFILE | Represents an error where a temporary file could not be created for an internal operation. | 16 |
| dgENOTIMPL | Represents a not implemented error. | 2 |
| dgENOTSECURE | Represents an invalid user/password error. Security context not established. | 11 |
| dgEnReadingNext | Represents an error reading the next item. | 1110 |
| dgEnReadingRecord | Represents an error reading a record. | 1115 |
| dgEnRemoveBaseFile | Represents an error where a base file cannot be replaced. | 1129 |
| dgEnRemoveLogicalFile | Represents an error where a logical file cannot be replaced. | 1130 |
| dgEnSeparatorExpected | Represents an error where a separator was expected. | 1111 |
| dgEnTextFile | Represents an error with a text file. | 1107 |
| dgEnTimeExpected | Represents an error where a time value was expected. | 1124 |
| dgEnTimestampExpected | Represents an error where a time-stamp value was expected. | 1125 |
| dgEnToFileNotCrt | Represents an error where the to-file was not created. | 1119 |
| dgEnToFileNotFnd | Represents an error where the to-file was not found. | 1118 |
| dgEnUnknown | Represents an unknown error. | 1101 |
| dgEOBSOLETE | Represents an error where a facility was deprecated several releases ago, and is not supported anymore. | 17 |
| dgEOK | Not really an error, operation went OK. | -1 |
| dgEOLDSERVER | Represents an operation not supported on an old server error. | 14 |
| dgEpAPXEXTERN | Represents an error where the Apx Externalize method failed. | 759 |
| dgEpAPXGETPROP | Represents an error where the Apx GetProp method failed. | 761 |
| dgEpAPXMATER | Represents an error where the Apx Materialize method failed. | 758 |
| dgEpAPXMETHOD | Represents an error where the Apx method failed. | 757 |
| dgEpAPXPRINT | Represents an error where the Apx Print method failed. | 762 |
| dgEpAPXSETPROP | Represents an error where the Apx SetProp method failed. | 760 |
| dgEpBADPARMDIR | Represents an error where an invalid Parameter Direction was provided. | 709 |
| dgEpCRTDC | Represents an error where the print DC creation failed. | 753 |
| dgEpINITAPXFAILED | Represents an error where InitApx failed. | 756 |
| dgEpINITAPXNOTFND | Represents an error where InitApx was not found. | 755 |
| dgEpINVPARMCOUNT | Represents an error where an invalid parameter count was supplied on a Remote Program Call. | 705 |
| dgEpINVPARMTYPE | Represents an error where an invalid parameter type was supplied on a Remote Program Call. | 703 |
| dgEpLIBNOTFND | Represents an error where the Apx library was not found. | 754 |
| dgEpMEMEXCEPTION | Represents an error where a memory exception occurred in a Remote Program Call, possibly due to a parameter mismatch. | 708 |
| dgEpOPENPRINT | Represents an error where opening the printer failed. | 774 |
| dgEpOPENSPLVIEWER | Represents an error where opening the print previewer failed. | 775 |
| dgEpPARMTYPENOTSUP | Represents an error where the parameter type is not supported on a Remote Program Call. | 704 |
| dgEpPGMERR | Represents an error where the program encountered an error. | 702 |
| dgEpPGMNOTFND | Represents an error where the program was not found. | 701 |
| dgEpPRINTNOTFND | Represents an error where the printer was not found. | 751 |
| dgEpPROMPTCANCEL | Represents an error where the print prompter was canceled. | 763 |
| dgEpPROMPTFAILED | Represents an error where the print prompter failed. | 752 |
| dgEPRINT | Represents print errors. | 750 |
| dgEpSERVERTOOOLD | Represents an error where the print file's version is newer than the server; an updated server is required for access. | 764 |
| dgEpSPOOLBADPAGE | Represents an error where the spool file is corrupted and has an invalid spool page format. | 773 |
| dgEpSPOOLCREATE | Represents an error where the spool file could not be created. | 765 |
| dgEpSPOOLNODM | Represents an error where the spool file is corrupted and has no device mode. | 769 |
| dgEpSPOOLNOHEAD | Represents an error where the spool file is corrupted and has no header. | 768 |
| dgEpSPOOLNOPAGE | Represents an error where the spool file is corrupted and has no full page. | 772 |
| dgEpSPOOLNOSD | Represents an error where the spool file is corrupted and has no start of document. | 770 |
| dgEpSPOOLNOSP | Represents an error where the spool file is corrupted and has no start of page. | 771 |
| dgEpSPOOLREOPEN | Represents an error where reopening the spool file failed. | 767 |
| dgEpSPOOLWRITE | Represents an error where writing to the spool file failed. | 766 |
| dgEpTOOFEWPARMS | Represents an error where not enough parameters were provided on a Remote Program Call. | 706 |
| dgEpTOOMANYPARMS | Represents an error where too many parameters were provided on a Remote Program Call. | 707 |
| dgEqBLOCKDIRCHNG | Represents an error where SQL Server does not support changing sequential read direction while employing network blocks. | 1524 |
| dgEqCOLLSYSVAL | Represents an error where the "New Column Collation" system value does not correspond to an available collation. | 1530 |
| dgEqCONNECTION | Represents an error where the connection to SQL Server cannot be restored. | 1509 |
| dgEqDMOERROR | Represents a DMO Error received from MS SQL Server. | 1518 |
| dgEqDUPOWNOBJ | Represents an error where an object by that owner already exists. | 1511 |
| dgEqEXECUTION | Represents a query execution error or an inaccessible database. | 1508 |
| dgEqINVALIDOBJECT | Represents an error where DMO: OLE object is not (or is no longer) valid in SQLDMO. | 1502 |
| dgEqINVALIDOBJECTDEFINITION | Represents an error where an attempt was made to create an object but its definition were incomplete or inconsistent. | 1503 |
| dgEqINVALIDPARAMETER | Represents an error where an invalid parameter passed to a method or property, or other unexpected condition. | 1504 |
| dgEqINVALIDPLATFORM | Represents an error where the connected SQL Server or Client are of an invalid version, or no SQL-DMO server support. | 1505 |
| dgEqINVHASHCONFIG | Represents an error where the "# Prefix Substitution" system value is invalid; use a string that does not begin with the '#' character. | 1531 |
| dgEqINVMMCONV | Represents an error where a file with a single member cannot be converted to one supporting multiple members. | 1528 |
| dgEqINVMMVAL | Represents an error where the specified maximum member value is not valid because the file already contains more members. | 1529 |
| dgEqINVMULTMBR | Represents an error where with the DSS multi-member feature enabled, Join Logical file definitions only support the 'maximum members=1' attribute. | 1527 |
| dgEqINVOPFIELDREF | Represents an error where an invalid operation against special file '*FIELDREF' was attempted. | 1513 |
| dgEqINVORDERBYIDX | Represents an error where SELECT statements with the ORDER BY clause are not allowed in INDEXED logical files. | 1525 |
| dgEqINVSQLSYN | Represents an error where there is incorrect syntax in internally generated SQL statement. | 1514 |
| dgEqINVSQLVER | Represents an error where an invalid SQL Server version is used. SQL Server 2000 or above required. | 1523 |
| dgEqINVUSRSQLSYN | Represents an error where there is incorrect syntax in user provided SQL statement. | 1515 |
| dgEqINVUSRTYPE | Represents an error where one or more *FIELDREF fields could not be created as user defined types. | 1526 |
| dgEqITEMNOTFOUND | Represents an error where the named object was not found. | 1506 |
| dgEqKEYNAMENOTINBASE | Represents an error where a key field must be based on a physical field with the same name. | 1516 |
| dgEqMAXCOLS | Represents an error where SQL Server supports a maximum of 1024 columns (fields). | 1520 |
| dgEqMAXKEYS | Represents an error where SQL Server supports a maximum of 32 key fields per index. | 1521 |
| dgEqNOCONVERSION | Represents an error where a field type is not supported. Ensure there is no 'Image' or 'Text' columns, if any, build a logical without them. | 1522 |
| dgEqNOMULTIFMT | Represents an error where SQL Server does not support multi-format files. | 1519 |
| dgEqNOSQLSERVER | Represents an error where SQL Server does not exist or access is denied. | 1501 |
| dgEqOLEDBERROR | Represents an OLE DB Error received from MS SQL Server. | 1517 |
| dgEqRESOURCE | Represents an error where there are insufficient resources either locally or on the server. | 1510 |
| dgEqSQLUNKNOWN | Represents uninterpreted SQL Server errors. | 1512 |
| dgEqUNPRIVILEGEDLOGIN | Represents an error where the current login does not have sufficient privilege to perform the requested operation. | 1507 |
| dgEr2FEWJOINS | Represents an error where there are too few JoinDefs. | 516 |
| dgEr2MANYFLDS | Represents an error where too many fields are in the JoinDef. | 506 |
| dgErADENOTFND | Represents an error where the active dictionary entry was not found. | 519 |
| dgErBADSRC | Represents an error with a bad base field, format or file. | 501 |
| dgErBASFILENOTFND | Represents an error where the base file was not found. | 524 |
| dgErBASMBRNOTFND | Represents an error where the base source member was not found. | 522 |
| dgErCRTADE | Represents an error creating an active dictionary entry. | 518 |
| dgEREPOSITORY | Represents repository access errors. | 500 |
| dgErFDNOCHG | Represents an error where the FileDef cannot be changed. | 517 |
| dgErINVDUPFLD | Represents an error where the duplicate field was not found in the format. | 512 |
| dgErINVSECFLD | Represents an error where the secondary field was not found in the format. | 511 |
| dgErINVSELFLD | Represents an error where the selector field was not found in the format. | 510 |
| dgErINVTYPE | Represents an error with an invalid type. | 502 |
| dgErJFLDCONFL | Represents an error with conflicting join field types. | 521 |
| dgErJOINNOSTATIC | Represents an error where join files can't have static select/omits. | 520 |
| dgErJSECKEY | Represents an error with an invalid key for join file, the key field used is from a secondary file. | 523 |
| dgErNODUPNAME | Represents an error where no duplicate field name was specified. | 509 |
| dgErNOSECNAME | Represents an error where no secondary field name was specified. | 508 |
| dgErNOSELFLDS | Represents an error where no selector fields were specified. | 505 |
| dgErNOSELNAME | Represents an error where no selector field name was specified. | 507 |
| dgErNOSEQJOIN | Represents an error where the JoinDef is out of sequence. | 514 |
| dgErNOTJOINED | Represents an error where the file is not joined. | 515 |
| dgErSECNOTDEF | Represents an error where the secondary file is not defined. | 504 |
| dgErSELNOTDEF | Represents an error where the selector file is not defined yet. | 503 |
| dgErTYPECONFL | Represents an error with conflicting field types. | 513 |
| dgEsADOPCODE | Represents an error where there is an invalid or missing *SQLCLIENT license key. | 1229 |
| dgEsADOTRLEXP | Represents an error where the *SQCLIENT license has expired. | 1230 |
| dgEsALLOCERRCONVTYP | Represents an allocate error for a conversation type. | 837 |
| dgEsALLOCERRNORETRY | Represents an allocate error with no retry. | 831 |
| dgEsALLOCERRPGMNOTAVAILNR | Represents an allocate error where the program is not available with no retry. | 833 |
| dgEsALLOCERRPGMNOTAVAILR | Represents an allocate error where the program is not available with retry. | 835 |
| dgEsALLOCERRPIPNOTALLOWED | Represents an allocate error where the PIP is not allowed. | 838 |
| dgEsALLOCERRPIPNOTCORRECT | Represents an allocate error where the PIP is not correct. | 839 |
| dgEsALLOCERRRETRY | Represents an allocate error with retry. | 832 |
| dgEsALLOCERRSECNOTVALID | Represents an allocate error where the sec is not valid. | 836 |
| dgEsALLOCERRSYNCHLEVEL | Represents an allocate error for a sync level. | 840 |
| dgEsALLOCERRTPNNOTRECOG | Represents an allocate error where the transaction program is not recognized. | 834 |
| dgEsAPPCBUSY | Represents an APPC Busy status. | 809 |
| dgEsAS400ERROR | Represents an error where the error text is contained in extended error info. | 1301 |
| dgEscBADFRAME | Represents an error where there is an NTLM protected message error. See server logs for details. | 1902 |
| dgEscBINDPWDDA | Represents an error where the EIM Simple Bind password data area is not accessible; cannot map client to a User Profile. | 1904 |
| dgEscEIMSSLCONFIG | Represents an error where the EIM SSL data area is not accessible; cannot map client to a User Profile. | 1905 |
| dgEsCONVTABLEFULL | Represents an error where the conversation table is full. | 845 |
| dgEscSSO | Represents next-gen *DOMAIN support. | 1900 |
| dgEscSSPIQUERY | Represents an error where Windows Security Support Provider query fails. Check server logs. | 1901 |
| dgEsDEALLOCABENDPROGRAM | Represents a deallocate error where the program abnormally ends. | 841 |
| dgEsDEALLOCNORMAL | Represents a normal deallocation status. | 802 |
| dgEsDUPSTRM | Represents a duplicate stream error. | 301 |
| dgESERVEXCEPTION | Represents an unexpected exception on the server error. | 13 |
| dgEsHDRCORRUPT | Represents an error where the header in the APPC packet is corrupted. | 854 |
| dgEsINSUFFICIENTMEMORY | Represents an error where there is insufficient memory. | 842 |
| dgEsINVALIDCREDS | Represents an error where the database logon credentials are invalid. | 855 |
| dgEsINVALIDLUNAME | Represents an error where the LU name is invalid. | 852 |
| dgEsINVALIDPASSWORDLEN | Represents an error where the password length is invalid. | 851 |
| dgEsINVALIDREQ | Represents an error where an invalid request 1 was received by the license manager. | 1206 |
| dgEsINVALIDSUR | Represents an error where an invalid request 2 was received by the license manager. | 1207 |
| dgEsINVALIDUSERIDLEN | Represents an error where the user ID length is invalid. | 850 |
| dgEsINVSRLNBR | Represents an invalid serial number error. | 1203 |
| dgEsLICSRVRFAIL | Represents an error where a DSS License cannot be obtained: Server execution failed. | 1227 |
| dgEsLMERR01 | Represents a license manager recovery error 1. | 1212 |
| dgEsLMERR02 | Represents a license manager database error 2. | 1213 |
| dgEsLMERR03 | Represents a license manager recovery error 3. | 1214 |
| dgEsLMERR04 | Represents a license manager recovery error 4. | 1215 |
| dgEsLMERR05 | Represents a license manager recovery error 5. | 1216 |
| dgEsLMERR06 | Represents a license manager recovery error 6. | 1217 |
| dgEsLMERR07 | Represents a license manager error 7. | 1218 |
| dgEsLMERR08 | Represents a license manager error 8. | 1219 |
| dgEsLMMUTEX | Represents an error where the license manager service is not accessible. | 1208 |
| dgEsLMPID | Represents an error where the license manager service is not started. | 1211 |
| dgEsLMSTART | Represents an error where the license manager service is not synchronized. | 1210 |
| dgEsLMSYNCDQ | Represents an error where the license manager service sync object creation failed. | 1209 |
| dgEsLMSYNCDQD | Represents an error where the license manager PID data area could not be deleted. | 1223 |
| dgEsMEMORYALLOCERROR | Represents a memory allocation error. | 843 |
| dgEsMTSFAILHT | Represents an error where the CPU count is not available on this system. | 1228 |
| dgEsMTSPCODE | Represents an error where there is an invalid or missing ADB multi-tier license. | 1220 |
| dgEsMTSPRCCNT | Represents an error where the ADB multi-tier license processor count is exceeded. | 1222 |
| dgEsMTSTRLEXP | Represents an error where the ADB multi-tier license has expired. | 1221 |
| dgEsNLSCODEPAGE | Represents an error where the registry cannot be accessed to determine platform character encoding. | 1303 |
| dgEsNOCODEPAGE | Represents an error where the server is not configured for the requested character set. | 1304 |
| dgEsNODBCSCONV | Represents an error where DBCS translation is not supported for given CCSIDs. | 1302 |
| dgEsNOLICDLL | Represents an error where the license DLL is not registered or missing. | 1224 |
| dgEsNOLICSRVR | Represents an error where a connection to the database server cannot be established. The server may be shut down, there may be a network hardware problem, there may be no common transports, or the server may not exist. | 1225 |
| dgEsNOPRODUCT | Represents an error where the specified licensed product is not available. | 1226 |
| dgEsOK | Represents a status of OK. | 801 |
| dgEsPARMCHKBADDEALLOCTYPE | Represents a parameter check error for a bad deallocate type. | 820 |
| dgEsPARMCHKBADFILLTYPE | Represents a parameter check error for a bad fill type. | 822 |
| dgEsPARMCHKBADPARTNERNAME | Represents a parameter check error for a bad partner name. | 818 |
| dgEsPARMCHKBADRETURNCTRL | Represents a parameter check error for a bad return control. | 816 |
| dgEsPARMCHKBADSYNCLVLALLOC | Represents a parameter check error for a bad sync level allocated. | 815 |
| dgEsPARMCHKBUFFERCROSSSEG | Represents a parameter check error where the buffer crosses a segment. | 812 |
| dgEsPARMCHKCONFNOTALLOWED | Represents a parameter check error where the configuration is not allowed. | 819 |
| dgEsPARMCHKINVALIDCONVERID | Represents a parameter check error for an invalid conversation Id. | 811 |
| dgEsPARMCHKINVALIDVERB | Represents a parameter check error for an invalid verb. | 810 |
| dgEsPARMCHKINVCONVERTYPE | Represents a parameter check error for an invalid conversation type. | 814 |
| dgEsPARMCHKPIPTOOLONG | Represents a parameter check error where the PIP is too long. | 817 |
| dgEsPARMCHKPREPTORCVTYPE | Represents a parameter check error for a prepare to receive type. | 821 |
| dgEsPARMCHKRECMAXLEN | Represents a parameter check error for a record maximum length. | 823 |
| dgEsPARMCHKRESFLDNOTZERO | Represents a parameter check error where the result field is not zero. | 825 |
| dgEsPARMCHKTPNAMELENGTH | Represents a parameter check error for a transaction program name length. | 813 |
| dgEsPARMCHKUNKNOWNSECTYPE | Represents a parameter check error for an unknown sec type. | 824 |
| dgEsPCODE | Represents an error where there is an invalid or missing ADB server license. Use Registration Assistant to verify/install a valid license key. | 1205 |
| dgEsPCSWINNOTLOADED | Represents an error where PCSWIN is not loaded. | 848 |
| dgEsPCSWINOUTOFMEMORY | Represents an error where PCSWIN is out of memory. | 849 |
| dgEsPROGRAMERRNOTRUNCATION | Represents a program error with no truncation. | 803 |
| dgEsPROGRAMERRPURGING | Represents a program error with purging. | 805 |
| dgEsPROGRAMERRTRUNCATION | Represents a program error with truncation. | 804 |
| dgESQLSERVER | Represents SQL Server native errors. | 1500 |
| dgEsRESOURCEFAILURENORETRY | Represents a resource failure with no retry. | 807 |
| dgEsRESOURCEFAILURERETRY | Represents a resource failure with retry. | 806 |
| dgEsROUTERNOTINSTALLED | Represents an error where the router is not installed. | 846 |
| dgEsROUTERWRONGLEVEL | Represents an error where the router is at the wrong level. | 847 |
| dgEssCERTAUTHORITY | Represents an error where a certificate authority chain error occurred. | 1814 |
| dgEssCERTREVOKED | Represents an error where chain contains one or more revoked certificate errors. | 1815 |
| dgEssCERTSTOREDA | Represents an error where the certificate store configuration data areas are not found or are invalid. | 1812 |
| dgEssCERTSTOREPW | Represents an error where it cannot open the certificate store credential evidence object. | 1813 |
| dgEssDNSFAIL | Represents an error where DNS query failed during SSL connection verification of server hostname. | 1811 |
| dgEssDOWNLVLCLIENT | Represents an error where server requirements for secure connection (SSL) are not met by this connection. | 1801 |
| dgEssDOWNLVLSERVER | Represents an error where the server does not meet requirements for requested secure connection (SSL). | 1802 |
| dgEssINVALIDOPTS | Represents an error where for secure connections, either "request" or "require" options must be specified. | 1805 |
| dgESSL | Represents SSL support errors. | 1800 |
| dgEssNOCERTIFICATE | Represents an error where an SSL connection was initiated, but the server did not provide a valid certificate. | 1810 |
| dgEssNOCLEARTEXT | Represents an error where this connection configuration does not permit access to servers that allow non-secure connections (SSL). | 1803 |
| dgEssNODNSMATCH | Represents an error where the server's SSL certificate subject name does not match the server's DNS host name. | 1808 |
| dgEssNOLOCALCERT | Represents an error where no certificate exists in the user's local store corresponding to the server's SSL certificate. | 1807 |
| dgEssNONAMEMATCH | Represents an error where the server's SSL certificate subject name does not match the name specified in the connection options. | 1809 |
| dgEssSCHANNELNEG | Represents an error where the Schannel security provider SSL negotiation failed. Check DataGate Server logs for details. | 1806 |
| dgEsSTATECHKNOTINCONFSTAT | Represents a state check error where it's not in configuration stat. | 826 |
| dgEsSTATECHKNOTINRECEIVE | Represents a state check error where it's not in receive. | 827 |
| dgEsSTATECHKREQSNDBADSTAT | Represents a state check error where the request to send is in a bad state. | 828 |
| dgEsSTATECHKSNDERRBADSTAT | Represents a state check error where send error is in a bad state. | 830 |
| dgEsSTATECHKSNDINBADSTATE | Represents a state check error where send is in a bad state. | 829 |
| dgEsSTRMNOTOPEN | Represents an error where the stream is not open. | 302 |
| dgEssUKNOWNLEVEL | Represents an error where the server's connection security level (SSL) is higher than supported by this version of DataGate. | 1804 |
| dgEsTOOMANYCONVERSATIONS | Represents an error where there are too many conversations. | 844 |
| dgESTREAM | Represents stream errors. | 300 |
| dgEsTRLEXP | Represents an error where the ADB server license has expired. | 1201 |
| dgEsUNDEFINED | Represents an undefined error. | 853 |
| dgEsUNSUCCESSFUL | Represents an unsuccessful status. | 808 |
| dgESUPERVISOR | Represents supervisor errors. | 1000 |
| dgEsUSRCNT | Represents an error where the user count is exceeded. | 1204 |
| dgESYSTEM | Represents system dependent errors. | 1300 |
| dgETCPIP | Represents TCP/IP errors. | 900 |
| dgEUNKNOWN | Represents an unknown error. | 1 |
| dgExDENIED | Represents an error where access to this function is denied by exit program security; permission may be obtained from your database system administrator. | 1602 |
| dgExINVLIC | Represents an error where the exit point support license is not found or invalid. | 1603 |
| dgEXITPROG | Represents AS/400 exit points. | 1600 |
| dgExMISSING | Represents an error where the registered exit program is not found. | 1601 |

## Example. Showing more details when opening a file fails due to Member or File not found.

```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
          //Exit procedure here.
  }

  /* Do some action here. */

  dbFile.Close();
  db.Close();
```
