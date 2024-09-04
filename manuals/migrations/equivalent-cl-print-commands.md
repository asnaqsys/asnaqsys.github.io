---
title: "Equivalent CL Print Commands Guide"
description: "Discover the equivalent CL print commands in the migrated target platform, understanding their functionalities and differences."
---

The following tables lists the CL commands migrated by Monarch and the keywords supported by each command. The Output Queue and Spooled File commands are implemented in the `ASNA.Monarch.Spooler` class.

### Output Queue Commands

In the following commands, the OUTQ keyword can receive the name of an unqualified queue.

| **Command** | **Keywords** | **Implementation** | **Purpose** |
| --- | --- | --- | --- |
| CLROUTQ | OUTQ | `Spooler.ClearQueue` | **Clear Output Queue** |
| CRTOUTQ | OUTQ | `Spooler.CreateQueue` | **Create Output Queue** |
| DLTOUTQ | OUTQ | `Spooler.DeleteQueue` | **Delete Output Queue** |
| HLDOUTQ | OUTQ | `Spooler.HoldQueue` | **Hold Output Queue** |
| RLSOUTQ | OUTQ | `Spooler.ReleaseQueue` | **Release Output Queue** |
| WRKOUTQ | OUTQ <br/>OUTPUT(\*PRINT) | Spooler.PrintQueue | **Work with Output Queue** <br />The only supported OUTPUT value is \*PRINT. |

### Spooled File Commands

In the following commands, the keywords FILE, JOB & SPLNBR identify the spool file acted on by the command.

| **Command** | **Keywords** | **Implementation** | **Purpose** |
| --- | --- | --- | --- |
| CHGSPLFA | FILE, JOB & SPLNBR <br />OUTQ <br />FORMTYPE <br />SAVE <br />USRDTA | `Spooler.Move` <br />`FileSpooler.SetFileFormType` <br />`Spooler.SetFileSaveAfter` <br />`Spooler.SetFileUserData` | **Change Spooled File Attributes** |
| CPYSPLF | FILE, JOB & SPLNBR <br />TOFILE <br />TOMBR <br />MBROPT <br />CTLCHAR | `Spooler.CopyFileToDatabaseFile` | **Copy Spooled File** |
| DLTSPLF | FILE, JOB & SPLNBR | `Spooler.DeleteFile` | **Delete Spooled File** <br /> For the FILE keyword, a name must be provided, \*SELECT is not supported. |
| HLDSPLF | FILE, JOB & SPLNBR | `Spooler.HoldFile` | **Hold Spooled File** <br />For the FILE keyword, a name must be provided, \*SELECT is not supported. |
| RLSSPLF | FILE, JOB & SPLNBR | `Spooler.ReleaseFile` | **Release Spooled File** <br />For the FILE keyword, a name must be provided, \*SELECT is not supported. |

### Printer File Command

The Override File command is implemented in the ASNA.Monarch.CLProgram class.

| **Command** | **Keywords** | **Implementation** | **Purpose** |
| --- | --- | --- | --- |
| OVRPRTF | FILE <br />TOFILE <br />**OUTQ** <br />**FORMTYPE** <br /> FORMNAME <br />COPIES <br />**HOLD** <br />**SAVE** <br />**USRDTA** <br />SHARE | `CLProgram.OverrideFile` | **Override with Printer File** |

### Job Properties Related to Printing

The `Monarch.Job` class has two properties pertaining to printing:

- `OutputQueuesRoot` – Specifies the root folder where the Output Queues are located in the system.
- `OutputQueue` – This property specifies the queue where the spooled file will be created for all printer files unless there is an outstanding OVRPRTF for a printer file directing the spooled file to a different queue via the OUTQ parameter.

The Change Job command allows setting of the OutputQueue property.

| **Command** | **Keywords** | **Implementation** | **Purpose** |
| --- | --- | --- | --- |
| CHGJOB | JOB('\*')<br/>OUTQ | `Job.OutputQueue` | **Change Job** <br />The OUTQ keyword specifies the output queue used for spooled files by setting the Monarch.Job's OutputQueue property. |
