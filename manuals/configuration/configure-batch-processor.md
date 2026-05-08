---
title: "Configure Batch Processor"
description: "Learn how to configure your batch processor efficiently with our easy-to-follow guide. Perfect for optimizing your data processing tasks."
---

Monarch provides these two programs to assist in the processing of Batch Jobs:
 - `ASNA.QSys.BatchDispatch.exe` (*BatchDispatch*)
 - `ASNA.QSys.BatchHost.exe` (*BatchHost*)


*BatchDispatch* is a console program that ‘watches’ a job queue and creates a system process to run the program stated in the job queue entry.  The new process uses the console program *BatchHost* as the the entry point for the new job.

Read more about [Batch Jobs](/manuals/programming/jobs/batch-jobs.html).

## Configuring BatchDispatch

See [Batch Dispatch](/manuals/hosting/mom/batch-dispatch.html).


## Configuring BatchHost

The majority of the configuration parameters of the Batch Job comes directly from the job that submitted or started it.  However some of the characteristics of the process hosting the batch job can be, or should be, estblished directly on BatchHost. The configuration of BatchHost is done via an `appsettings.json` file stored in the working directory of the process.

## `appsettings.json` File

### MonaJobConfig Section
Starting with version `4.0.22` of `ASNA.QSys.Runtime`, certain attributes of batch jobs can be described in the `MonaJobConfig` section of the BatchHost `appsettings.json`. The main aspects that can be established in the `MonaJobConfig` section relates to directory locations for queues, the IFS and message files.

Here is an example of the `MonaJobConfig` section:
```json
{
  "MonaJobConfig": {
    "OutputQueueRootPath": "C:/MonarchQueues/OutputQueues",
    "DefaultOutputQueue": "QPRINT",
    "IFSRootPath": "//MyServer/MyShare",
    "DlsRootName": "QDLS",
    "JobQueueBaseQueuesPath": "C:/MonarchQueues/JobQueues",
    "MessageFilePath": "./MessageFiles"
  },
  . . .
}
```

These are the `MonaJobConfig` values and their meaning:

| Type | Name | Description 
| ---  | ---  | --- 
| String | DefaultOutputQueue | The name of the default Output Queue. Defaults to "QPRINT" | 
| String | DlsRootName | The name of the directory, located within the IFSRootPath, where the Document Library Objects are located. Defaults to "QDLS" | 
| String | IFSRootPath | The directory path where the IFS objects are located in the system. | 
| String | JobQueueBaseQueuesPath | The directory path where the Job Queues are located in the system. | 
| String | MessageFilePath | The directory path where the Message Files are located in the system. | 
| String | OutputQueueRootPath | The directory path where the Output Queues are located in the system. | 

If the `appsettings.json` file does not have these values set, then the batch job will inherit those found in the parent job. 

A similar `MonaJobConfig` section can be [set for websites](/manuals/configuration/configure-expo-website.html#monajobconfig).

### AssemblyListProfiles Section

The `appsettings.json` file can also have a section called `AssemblyListProfiles`. The assembly list profiles section is a dictionary of [Assembly Lists](/manuals/programming/programs-and-procedures/call-program.html#namespace-list-and-assembly-list). Each list may have one or more directory or file paths pointing to the location of the .NET Assemblies containing  the programs used by the batch job.  When a batch job is being established, the parent job may set the Profile that should be used when the child batch job is started by providing a value to the [`MatchOptions.AssemblyListProfile`](/reference/runtime/qsys-runtime-job-support/batch-options.html#properties) property. If a profile is not set then the profile from the parent job is inherited and if it does not have one either, then the actual assembly list of the (ASP.NET Core or Batch) process is used.

The example below shows two profiles, `*Default` and `REPORTS`, each with different AssemblyList.

```json
{
  . . . 
  "AssemblyListProfiles": {
    "*Default": [
      "C:/SomeFolder/SubA/Acme.Lib.Utils.dll",
      "C:/SomeFolder/Acme*.dll"
    ],
    "REPORTS": [
      "C:/OtherFolder/ReportAssemblies/Acme*.dll",
      "C:/OtherFolder/DynamicAssemblies/Acme*.dll"
    ]
  }
}
```


