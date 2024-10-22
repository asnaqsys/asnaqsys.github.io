---
title: "Essential Developer Tools for Monarch Apps"
description: "Explore the must-have developer tools for Monarch Apps. Enhance your productivity and project quality with these essential utilities."
---

There are processes in Application development where trivial repetitive segments of code are need to be produced or maintained in sync with external resources. For the purposes of the contents of this chapter, we will call these segments `boilerplate` code.

*Boilerplate code* is often [hidden from the view](/concepts/program-structure/rpg-language-files.html) and made part of the syntax in *Special Purpose* programming languages such as RPG.

When a migration results in classes written in C#, which is a [General Purpose Programming Language](https://en.wikipedia.org/wiki/General-purpose_programming_language),  these *Boilerplate code* segments become explicit and visible.

One technique to *Encapsulate Boilerplate code* in General Purpose Object-Oriented Programming Languages is to allow a class definition to be split into multiple files, separating the Application code from *Boilerplate code*. C# allows such technique with the language support for [Partial classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods). Other terms given to this technique are: "*Code behind*" and "*Code besides*".

Each `QSys Program` is architected to have two files of *Code besides*, namely:

```
program.cs
    pragram.io.xfu
        pragram.io.cs
```

| Source file Extension | Description                                               | Usage                |
| --------------------- | --------------------------------------------------------- | -------------------- |
| `.cs`                 | Application Program C# code.                              | User code.           |
| `.io.xfu`             | External File Usage *metadata* in XML format                 | Initially generated. User maintained as changes are made. |
| `.io.cs`              | Partial C# class with External File's *Boilerplate* Code. | Tool-generated (from cache and xfu file). |


> The Monarch Base Dev Tool also produces a **cache** folder that contains *External File Definitions* for all the database, printer and display page files used by all the programs in a particular Project. This folder has *hidden* attributes to keep the folder structure simple for the Application developer.

## Integration with Visual Studio&reg;

Visual Studio&reg; Projects have a collection of files, where each file can have associated properties.

Typically, `.cs` C# source files will have:

| Property                 | Value         |
| ------------------------ | ------------- | 
| Build Action             | C# Compiler   |
| Copy to Output Directory | Do not copy   |
| Custom Tool              | (blank)       |

`.io.xfu` source files are set to have:

| Property                 | Value                    |
| ------------------------ | ------------------------ |  
| Build Action             | None                     |
| Copy to Output Directory | Do not copy              |
| Custom Tool              | AdgFileUsageGenerator    |

When a C# Project is built, the different source files are checked for changes. When source file changes, the actions and/or Custom Tools associated with each file run.

Additionally, Visual Studio is tracking changes for files with a *Custom Tool*. As soon as the changes are **saved**, the *Custom Tool* runs.

Sometimes it is desirable to *force* run the **Custom Tool** on files that have such association. For example, when user-interface fields are added to a Model (controlling a Display Page), the developer should make sure that the new fields are part of the communication *DataSet*, such that the program using a *Workstation* file for the Display Page can read and write the new fields. After making changes to the Model's properties (for those decorated with *DataSet* field attributes), the application developer should force run the **Custom Tool** on any Program using the Display Page, by selecting the **xfu** file, invoking the context Menu (right-click menu) and run the option : "Run Custom Tool". Doing so, will generate a new implementation for the *I/O* partial class with the proper C# field/type definitions.

<br>

### AdgFileUsageGenerator (ASNA.DataGate.FileUsageGenerator.dll)

The `AdgFileUsageGenerator` custom tool takes as **input**:

1. The `.io.xfu` XML specification - Program file references (workstation, database and printfile), Data Structures (based on file fields) and their field declaration directives.
2. External Database Definition *cache* (for any files referred to by `.io.xfu`).
3. Display Page **Model** field definitions expressed as C# properties - with particular field decoration attributes - (for all the workstation files referred to by `.io.xfu`).

> To parse the Display Page C# Model classes, ASNA *AdgFileUsageGenerator* uses another internal Tool named *ModelToWrf* (described below).

The `AdgFileUsageGenerator` custom tool produces as **output**: The `.io.cs` C# partial class, containing:

1. External field declarations as C# [Fixed Types](https://asnaqsys.github.io/concepts/program-structure/qsys-fixedtypes.html).
2. An explicit copy of the bytes representing the *Record format ID* for all files to be used by the *Open* method to implement *run-time* [Level checking](https://www.ibm.com/docs/en/i/7.2?topic=files-level-checking).
3. Implementation of methods for every file to populate fields in/out of the shared *DataSet*.

<br>

> Please abstain from adding user-code to the partial class directly. You may loose your changes.

## "Refresh XFU" Visual Studio context menu option.

The `.io.xfu` file associated with the QSys Program Application source, is initially generated when the Migration process that generated the C# code.

The purpose of `.io.xfu` is to:

1. List all references to all externally described files use by the program (workstation, database and printfiles).
2. Provide a means to the Developer to specify *Directives* on all records for all the files, to drive the generation of QSys Program partial class.

This XML file is also the selection node for Visual Studio to show the *context menu*, that will give the Developer access to the two Tools.

> ASNA.QSys runtime support will throw an exception when attempting to open files that had their schema out-of-sync with respect to the current partial class I/O implementation.

## ModelToWrf Tool (ASNA.ModelToWrf.dll)

Although an internal tool (used by `AdgFileUsageGenerator`), it may be useful to understand that when a Model is compiled into an .NET assembly, it can be loaded and its public declarations can be discovered using *reflection*.

> The importance of this fact is to understand that Model field definitions need to be complete and the C# compiler can be used as verifier. Do not attempt to run `.io.xfu` Custom Tool on programs using workstation files, whose Page Model is incomplete or produces syntax errors.