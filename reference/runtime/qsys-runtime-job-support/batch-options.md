---
title: "BatchOptions class            | QSYS API Reference Guide"
description: "Defines the options for a batch job. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines the options for a batch job.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AccountingCode | Gets or sets the accounting code for the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ADO_ConnectionString | Gets or sets the connection string for the ADO connection of the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AssemblyList | Gets or sets the comma separated list of assemblies or patterns. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | AssemblyListProfile | Gets or sets the name of the Profile to select from the configured dictionary of Assembly Lists. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DBName | Gets or sets the Database Name to be used for data by the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | DBNamePrint | Gets or sets the Database Name to be used for printer files by the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobName | Gets or sets the name of the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | JobOutputQueue | Gets or sets the output queue for the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | LDA | Gets or sets the initial value of the Local Data Area for the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | NamespaceList | Gets or sets the comma separated Namespace List for dynamic program calls. |
| [String\[\]](https://docs.microsoft.com/en-us/dotnet/api/system.string) | NameStoreConfigFiles | Gets or sets the configuration files used for the database names store used by the batch job. |
| [Nullable\<NameStoreOptions\>](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/nullable-value-types) | NameStoreOptions | Gets or sets the options for the database names store used by the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PsdsJobUser | Gets or sets the initial value of the user name reported in the PSDS for the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Switches | Gets or sets the initial value for the switches of the batch job. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | UserLibraryList | Gets or sets the user portion of the library list. The list is comma separated. |
