---
title: "Hosting Interactive Applications: A Guide"
description: "Learn how to host interactive applications effectively. This guide covers essential tips for seamless user engagement and performance."
---

There are several ways in which systems can be setup to run migrated applications.  This article discusses the typical environment where the ‘application server’ and the ‘website’ are both hosted on the same system and as noted in the overview of a Monarch [application architecture](/concepts/architecture/application-architecture.html#interactive-job-architecture), in its simplest configuration, the migrated code along with the website can be run in a single process. 

![Interactive Job in process MAS](/concepts/architecture/images/mas-in-process.svg)

_Application Logic running in process on the Web Server_

 
## Infrastructure
The Web & Application Server should have the following standard products/components.

### Components
 - Windows Server 2019 or 2022
 - IIS
 - .NET 6 or 8
 - ASP.NET Core

## Application Website
Running the *`dotnet publish`* command for the website packages all of the components below except for the Message Files.

### Components
 - Assemblies produced by Website proper (including all Razor Pages Areas)
 - Assemblies installed from Website dependency Packages (ASNA.QSys.Expo, …) and Frameworks (Microsoft.NETCore.App, …)
 - Configuration files:
   + appsettings.json
   + libman.json
   + Generated web.config
   + …
 - The *`wwwroot`* folder containing the *`css`*, *`js`* and *`lib`* subfolders
 - Message Files (files with extension *`.amfx`*)

## Application Logic
Migrated CL and RPG programs are grouped into Visual Studio Projects; these Projects produce Logic Assemblies (.dll).  These assemblies are typically not statically referenced by the website (so dotnet publish doesn’t pick them up) but rather, they are found via values on the [appsettings.json MonaServer](/manuals/configuration/configure-expo-website.html#monaserver) entry and loaded dynamically at runtime.

### Components
 - Logic Assemblies should be placed in the server's file system and their  location set on the website's appsettings.json [MonaServer:AssemblyList](/manuals/programming/programs-and-procedures/call-program.html#assembly-list) entry.

## Monarch Operation Managment Subsystems
In addition to the assemblies that the ASNA.QSys.xxx NuGet Packages will add to the application website, it may be necessary to add two *subsystems* to the server, namely: Printing Support and Batch Processing Support.

See the following articles for discussions on the [Monarch Batch Subsystem (MBS)](/manuals/programming/jobs/batch-jobs.html#monarch-batch-subsystem-mbs) and [Reporting in a Monarch Application](/concepts/printing/printing-introduction.html)

The sources to build these subsystems can be obtained from ASNA repositories in GitHub:
 - [BatchDispatch Repository](https://github.com/asnaqsys/ASNA.QSys.BatchDispatch).
 - [BatchHost source](https://github.com/asnaqsys/ASNA.QSys.MonaServer/tree/main/src/ASNA.QSys.BatchHost) is in the MonaServer Repository.
 - [PrinterWriter Repository](https://github.com/asnaqsys/ASNA.QSys.PrinterWriter)
 - [Renderer Repository](https://github.com/asnaqsys/ASNA.QSys.Renderer) which includes the Open.Renderer executable and the Open.PrintControls.

There are two options to use the Renderer and the Print Controls: Install the ones distrubuted by ASNA or build them from rhe [Renderer Repository](https://github.com/asnaqsys/ASNA.QSys.Renderer). The first option  does not have to get built as it is installed with many ASNA products as part of the ‘DataGate’ infrastructure; this version is  **.NET Framework** only; The [other option](/manuals/hosting/mom/manuscript-renderer.html) is ‘open sourced’ for customers that do not **install** DataGate products and can be found in the [Renderer Repository](https://github.com/asnaqsys/ASNA.QSys.Renderer); this option includes projects for Windows **.NET Framework** only and projects for the creation of PDF files on any .NET platform like Windows and Linux.

The DataGate version of the Print Controls is installed in the GAC, however the open-source versions can be located anywhere in the file system.

### Components
 - ASNA.QSys.BatchDispatch
 - ASNA.QSys.BatchHost
 - ASNA.QSys.PrinterWriter
 - One of the Renderers (DataGate version or one of the other [ASNA.QSys.Renderer options](/manuals/hosting/mom/manuscript-renderer.html))

