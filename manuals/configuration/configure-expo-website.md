---
title: "Configuring the Expo Website"
description: "Effortlessly configure your Expo website with our guide. Ideal for developers looking to launch or improve their Expo project's web presence."
---

## Application Settings

ASP.NET Core websites can have [many sources](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration) that control their configuration. 

Monarch produced sites use the `appsettings.json` file to control some of the specific configuration values affecting the behavior of the ASNA.QSys.Expo libraries.

While this document will refer to these configuration values in the `appseting.json` file, other configuration sources may be used as described in the [ASP.NET Core configuration documentation](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/configuration), with the notable exception of the `MonaJobConfig` [section](#monajobconfig).


## `appsettings.json` File
The following shows the typical `appsettings.json`  file produced by Monarch Cocoon:

```json
{
    "Logging": {
        "LogLevel": {
            "Default": "Warning"
        }
    },
    "AllowedHosts": "*",
    "MonaServer": {
        "HostName": "*InProcess",
        "Port": 5555,
        "TraceOption": 1
        "JobIdleTimeout": 20,
        "AssemblyList": [
            ".\\binLogic\\Acme.ERCAP.RUNCI.dll",
            ".\\binLogic\\Acme.PMP.CUST.dll"
        ]
    },
    "MonaJobConfig": {
        "OutputQueueRootPath": "C:/MonarchQueues/OutputQueues",
        "DefaultOutputQueue": "QPRINT",
        "IFSRootPath": "//MyServer/MyShare",
        "DlsRootName": "QDLS",
        "JobQueueBaseQueuesPath": "C:/MonarchQueues/JobQueues",
        "MessageFilePath": "../../../../MessageFiles",
        "BatchHostPath": "C:/Path/To/The/ASNA.QSys.BatchHost/Folder/"
    },
    "JobDescriptor": {
        "Class": "Acme.ERCAP.RUNCI_Job.MyJob",
        "Name": "MyJobName"
    },
    "DisplayPages": {
        "MultiJobOnBrowser": "true",
        "FakeDataType": "None",
        "FakeDataDirectory": ""
    }
}
```
The following sections describe the Expo related values.
 - `MonaServer`
 - `MonaJobConfig`
 - `JobDescriptor`
 - `DisplayPages` 

### MonaServer
The Monarch Server is responsible for loading and executing the migrated programs. The MonaServer section describes configuration options for executing
or locating a running instance of the Monarch Server.

`MonaServer` contains:
 - `HostName` - Monarch Server location. For the different location options, see [Interactive Job Architecture](/concepts/architecture/application-architecture.html#interactive-job-architecture).
 - `Port` - Port where Monarch Server is taking requests.
 - `TraceOption` - Verbosity of Monarch Server tracing. Valid values 0 or 1.
 - `JobIdleTimeout` - The timeout in minutes after which Monarch Server will terminate an idle Job.
 - `AssemblyList` - A list of paths for all the assemblies that compose the application. The assemblies in this list will be searched to locate programs used in [CALLD](/concepts/program-structure/qsys-program.html#calling-programs-and-procedures).

 The [AssemblyList](/manuals/programming/programs-and-procedures/call-program.html#assembly-list) paths can be given as absolute or relative paths, relative paths begin at the website location (where the website's .exe is located). The paths can also contain wildcards to refer to similarly named assemblies. 

Communication between the Website and the Monarch Server is done via TCP/IP. 

The HostName value contains the location of the Server, this value can be either a DNS name or an IP address. Additionally, the special value `*InProcess` indicates that the server is to be run in the same process as the Website.

When the Hostname is `*InProcess`, the Website will start the Monarch Server as part of website initiation. See the `Startup.cs` class.  

When the Monarch Server runs out of process, it becomes the responsibility of the Operator to ensure that the Server is started prior to the Website initiation.

### MonaJobConfig
Starting with version `4.0.22` of `ASNA.QSys.Runtime`, certain attributes of batch jobs can be described in the `MonaJobConfig` section of the website's `appsettings.json`. The main aspects that can be established in the `MonaJobConfig` section relates to directory locations for queues, the IFS and message files.

When the Monarch Server is running in process, it reads its settings from the `MonaJobConfig` found in the `appsettings.json` file of the web site. 

> The MonaJobConfig configuration must be given in the appsettings.json file, other ASP.NET Core configurations methods (like environmental variables) are not supported.

Here is an example of the `MonaJobConfig` section:
```json
{
  . . .
    "MonaJobConfig": {
        "OutputQueueRootPath": "C:/MonarchQueues/OutputQueues",
        "DefaultOutputQueue": "QPRINT",
        "IFSRootPath": "//MyServer/MyShare",
        "DlsRootName": "QDLS",
        "JobQueueBaseQueuesPath": "C:/MonarchQueues/JobQueues",
        "MessageFilePath": "C:/Path/To/The/MessageFiles",
        "BatchHostPath": "C:/Path/To/The/ASNA.QSys.BatchHost/Folder"
    }
  . . .
}
```

These are the `MonaJobConfig` values and their meaning:

| Type | Name | Description 
| ---  | ---  | --- 
| String | BatchHostPath | The directory path where the ASNA.QSys.BatchHost.exe is located. | 
| String | DefaultOutputQueue | The name of the default Output Queue. Defaults to "QPRINT" | 
| String | DlsRootName | The name of the directory, located within the IFSRootPath, where the Document Library Objects are located. Defaults to "QDLS" | 
| String | IFSRootPath | The directory path where the IFS objects are located in the system. | 
| String | JobQueueBaseQueuesPath | The directory path where the Job Queues are located in the system. | 
| String | MessageFilePath | The directory path where the Message Files are located in the system. | 
| String | OutputQueueRootPath | The directory path where the Output Queues are located in the system. | 


### JobDescriptor
The JobDescriptor section provides the parameters to the location of the entry point into the application.  It is composed of the valuing values:
 - `Class`
 - `Name`

The Class value is the fully qualified name of the interactive job class within the
application that represents the Job. This class should extend the [ASNA.QSys.Runtime.JobSupport.InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html). 

When a new user connect to the server, a new instance of the interactive job class will be
created and the [ExecuteStartupProgram](/reference/runtime/qsys-runtime-job-support/interactive-job.html)
method will be invoked.

Finally, the Name value provides the initial Job Name.  

### DisplayPages
The `DisplayPages` section of the configuration provides the ability to control the relationship of the website Display Pages and their corresponding Jobs. The two aspects that can be managed are the ability to run multiple jobs from a single browser and the usage of fake data.  

The section has three properties:
 - `MultiJobOnBrowser` - Valid values: `true`, `false`
 - `FakeDataType` - Valid values: `None`, `Output`, `Input`
 - `FakeDataDirectory` - Directory where Fake data files are located.

#### Multiple Jobs per Browser
Enabling the MultiJobOnBrowser property allows a user to employ a single browser to start [multiple jobs in different tabs](multiple-jobs-one-browser.html).  When the property is disabled (set to false), all the tabs on the user browser will display the state of the single job started on the first browser tab.

#### Fake Data
Fake data is utilized when particular pages of the website are to be displayed but the user does not wish to navigate the application all the way to the page.  The feature of [using fake data](using-fake-data.html) can be utilized by a developer to provide a set of files to another developer working purely in the look and feel of the website.



