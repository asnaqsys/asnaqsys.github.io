---
title: "Jobs"
description: "Explore the essentials of job management. This guide provides insights into effective strategies, tools, and tips for managing jobs efficiently."
---

### Background
IBM i programs rely on a runtime environment provided in the form of a Job. Jobs on the IBM i represent a schedulable unit of work, they are similar to a process in Windows, Unix and other operating systems, however, Jobs are typically much 'heavier' than processes.

Some of the facilities provided to programs by the Job are:
- Program Call Stack (Invocations)
- Program Instantiation in Activation Groups (Activations)
- A permanent connection to the database
- Library Lists
- File Overrides
- Local Data Area

After the Job has been established, control is passed to the initial program which in turn gets the application going.

IBM i Jobs can generally be classified as being either batch or interactive, where interactive jobs are associated with a workstation. Typical RPG application jobs are started in one of three ways on the IBM i:
1.	A batch job request is submitted by a program running in an existing job or by a user from a command line. When the  request is processed, the batch job is created.
2.	A batch job request is submitted by an automatic job scheduler. When the  request is processed, the batch job is created.
3.	An interactive job is created when a user signs on to a workstation.

## Monarch Jobs

Monarch provides an execution context anchored around the concept of a Job and implemented in its class library. Similar to IBM i Jobs, Monarch Jobs are classified as [Batch](batch-jobs.html) or [Interactive](interactive-jobs.html). 

Monarch Interactive jobs consist of one or more class libraries and are executed in a dedicated thread, colloquially known as _blue_ threads, of a Monarch Application Server process; these Interactive jobs are associated with an ASP.NET Core Session.
Monarch Batch jobs can be run in their own process or on a dedicated thread in the same process of the job that started it. 

Monarch Jobs can be started in one of three ways:
1.	A new batch immediate job is created by a program running in an existing job using one of these methods:[StartBatchJobInProcess](batch-jobs.html#osexec--start-batch-job-in-process), [StartBatchJobOutOfProcess](batch-jobs.html#osexec--start-batch-job-out-of-process) or [OSExecute](batch-jobs.html#osexec--start-submitted-job-immediately).
2.	A batch job request is submitted to a queue and then created by a job dispatcher like the [MBS](batch-jobs.html#monarch-batch-subsystem-mbs).
3.	An interactive job is created when a new ASP.NET Core Session is started.

Additional Job concepts can be found [here](/concepts/architecture/application-architecture.html#application-architectures).
