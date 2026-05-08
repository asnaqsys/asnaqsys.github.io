---
title: "Programs"
description: "Dive into how Legacy Programs are migrated. Discover key techniques used to preserve legacy program execution in the new environment,providing better analysis and insights."
---

## Programs in Monarch Base

Here is a [review](/concepts/architecture/monarch-programs.html) of Programs, Service Programs and Modules.

## Program Structure

[Migrated programs](/concepts/architecture/monarch-programs.html) become classes extending the [ASNA.QSys.Runtime.JobSupport.Program](/reference/runtime/qsys-runtime-job-support/program.html) class. The source for a typical program (say MyProgram) is composed of three files:
 * MyProgram.cs - Main C# source with code deriving from the original IBM i program. 
 * MyProgram.io.xfu - An XML file stating the File Usage or 'Externally Defined Files' of the the original IBM i program.
 * MyProgram.io.cs - C# Code derived from the external definition of files in the original IBM i program. This code declares the fields defined in externally described files and data structures as well as helper methods to populate the fields and buffer of the files used by the program. 

## .cs - Main C# Source Code
The Main C# source code structure resembles the structure of the original IBM i program with some additional elements injected at translation time (shown in bold below). The final sequence is:
 1. File declarations
 2. **Class constructor**
 3. Field and data structure declarations
 4. ```StarEntry``` main program method (derived from main C-Specs of migrated RPG programs)
 5. Other methods derived from Procedures and Subroutines in original migrated program
 6. **Properties for File Information Data Structures**
 7. **```__Entry``` method**
 8. **```_Entry``` static method**
 9. **```_instanceInit``` method**

 The constructor and ```inistanceInit``` method take care of initializing the program and opening the files that were marked as _implicitly opened_.

 The [entry methods](program-entry.html) are used in the process of [Calling a Program](call-program.html).


## .io.xfu - Externally Described File Usage
An XML file stating which of the ‘Externally Described Files’ of the original IBM i program are used in the program and how they are used. This XML file describes field renames, excludes ignored records, and other items vital to the correct functioning of the External file in the program.

## .io.cs - Externally Described Data
C# Code generated automatically out of the MyProgram.io.xfu descriptions. This code contains the declarations for those fields defined in externally described files as well as helper methods to move data between the file buffer and the program fields. It also contains field and method declarations for supporting externally described data structures.


