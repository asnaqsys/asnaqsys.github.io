---
title: "Migration of CL Programs: A Step-by-Step Guide"
description: "Learn the essentials of migrating CL programs to a new environment, ensuring compatibility and performance optimization."
---

## CL Programs

A CL Program has the capability of using over a thousand commands provided by OS/400, plus any number of user-created commands.  Usage of CL can be divided into two major categories: **System Administration** and **Application Coordination**.

The administration of the **system** involves operations like the creation of user profiles and the save/restore procedures. These activities are not considered part of the application itself and Monarch does not attempt to facilitate such activities.  Normal Windows techniques must be employed to affect these kinds of activities.

In its other personality, CL is used to set up the environment for RPG programs to run. Typical functions done by CL in this context are:

- Set up the Library List
- Override database file
- Select a different File or Member to be used by the RPG 'F' spec
- Establish a Query File
- Maintain application parameters in data area
- Allocate objects
- Control the Program Message Queue

These actions affect the OS/400 Job where programs are running and have an effect on all programs on the same job. Monarch Base provides these facilities through a set of classes that supplement .NET.

The migration of CL Programs supports [Built-In functions](#built-in-functions) and [Commands](#commands-listed-alphabetically).

## Built-In Functions

These are the functions supported by the migration process.

```
%INK
%LOWER
%SCAN
%SST
%SUBSTRING
%SWITCH
%TRIM
%TRIML
%TRIMR
%UPPER
```

When a call to the `QCLSCAN` command is found, it is treated as a 'built-in' function.


## Commands Listed Alphabetically

The following list of commands is supported by Monarch, please note that not all keywords are supported on all of the commands listed.

```
ADDLFM
ADDLIBLE
ADDPFM
ALCOBJ
CALL
CALLPRC
CALLSUBR
CHGACGCDE
CHGCURDIR / CD /CHDDIR 
CHGDTAARA
CHGJOB
CHGLFM
CHGLIBL
CHGPFM
CHGSPLFA
CHGVAR
CHKDLO 
CHKOBJ
CLOF
CLROUTQ
CLRPFM
CLRSPLF
COMMIT
CPY / COPY 
CPYDOC 
CPYFRMIMPF 
CPYFRMPCD 
CPYFRMSTMF 
CPYSPLF
CPYTOIMPF 
CPYTOPCD
CPYTOSTMF 
CRTDIR /  MD / MKDIR 
CRTDTAARA
CRTDUPOBJ
CRTFLR 
CRTOUTQ
CVTDAT
DCL
DCLF
DLCOBJ
DLTDLO 
DLTDTAARA
DLTF
DLTOUTQ
DLTOVR
DLTSPLF
DLYJOB
DO
DOUNTIL
DOWHILE
DSPCURDIR 
DSPFLR 
ELSE
ENDCMTCTL
ENDDO
ENDPGM
ENDSELECT
ENDSUBR
GO
GOTO
HLDOUTQ
HLDSPLF
IF
INZPFM
ITERATE
LEAVE
MONMSG
MOV / MOVE 
MOVDOC 
OPNQRYF
OTHERWISE
OVRDBF
OVRDSPF
OVRMSGF
OVRPRTF
PGM
POSDBF
RCLACTGRP
RCLRSC
RCVF
RCVMSG
RETURN
RLSOUTQ
RLSSPLF
RMVDIR / RD / RMDIR 
RMVLIBLE
RMVM
RMVMSG
RNM / REN 
RNMDLO 
RNMM
RNMOBJ
ROLLBACK
RTNSUBR
RTVDTAARA
RTVJOBA
RTVMBRD
RTVMSG
RTVNETA
RTVSYSVAL
RTVUSRPRF
SBMJOB
SELECT
SETATNPGM
SNDF
SNDPGMMSG
SNDRCVF
STRCMTCTL
SUBR
WHEN
WRKOUTQ
```

## Commands Listed by Group

The following lists group related commands.

### Calls
```
CALL
CALLPRC
CALLSUBR
RETURN
RTNSUBR
```

### Control Flow
```
DO
DOUNTIL
DOWHILE
ELSE
END
ENDDO
GO
GOTO
IF
ITERATE
LEAVE
OTHERWISE
SELECT
WHEN
```

### Commitment Control
```
COMMIT
ENDCMTCTL
STRCMTCTL
ROLLBACK
```

### Dates
```
CVTDAT
```

### Exception Handling
```
MONMSG
```

### Files
```
ADDPFM
ADDLFM
CHGLFM
CHGPFM
DCLF
CLRPFM
CLOF
DLTF
INZPFM
RCVF
OPNQRYF
POSDBF
SNDF
SNDRCVF
```

### Integrated File System
```
CHGCURDIR / CD /CHDDIR 
CPY / COPY 
CPYFRMIMPF 
CPYFRMSTMF 
CPYTOIMPF 
CPYTOSTMF 
DSPCURDIR 
CRTDIR /  MD / MKDIR 
MOV / MOVE 
RMVDIR / RD / RMDIR 
RNM / REN 
```

### Document Library Object
```
CHKDLO 
CPYDOC 
CPYFRMPCD 
CPYTOPCD
CRTFLR 
DLTDLO 
DSPFLR 
MOVDOC 
RNMDLO 
```

### Job Related
```
CHGACGCDE
CHGJOB
DLTOVR
DLYJOB
OVRDBF
OVRDSPF
OVRMSGF
OVRPRTF
RCLACTGRP
RTVJOBA
SBMJOB
```

### Library List
```
ADDLIBLE
CHGLIBL
RMVLIBLE
```

### Messages
```
RCVMSG
RMVM
RMVMSG
RNMM
SNDPGMMSG
RTVMSG
```

### Object Management
```
ALCOBJ
CHGDTAARA
CHKOBJ
CRTDUPOBJ
CRTDTAARA
DLCOBJ
DLTDTAARA
RCLRSC
RNMOBJ
RTVDTAARA
RTVMBRD
```

### Output Queues
```
CLROUTQ
CRTOUTQ
DLTOUTQ
HLDOUTQ
WRKOUTQ
RLSOUTQ
```

### Program Structure Definition
```
ENDPGM
PGM
ENDSUBR
SUBR
```

### Spoolfiles
```
CLRSPLF
CPYSPLF
CHGSPLFA
DLTSPLF
HLDSPLF
RLSSPLF
```

### System
```
RTVSYSVAL
RTVUSRPRF
RTVNETA
```

### Variables
```
DCL
CHGVAR
```

### Other
```
SETATNPGM
```

----



