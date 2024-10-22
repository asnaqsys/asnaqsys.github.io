---
title: "Datagate Component Suite: An Overview"
description: "This document provides an overview of the ASNA DataGate Client, including its features, how it integrates with various development environments, and guidance on setup and configuration for optimal use."
---

The ASNA DataGate assembly provides managed-code access to data and objects residing in DataGate for IBM i and DataGate for Windows (formerly, Acceler8DB) databases. Leveraging the strength of the .NET Framework, DG for Visual Studio programs can be created using any .NET development language, including ASNA Visual RPG, Visual Basic, C#, and others. Data access mechanisms in DG for Visual Studio support and enhance the System.Data namespace, including the DataSet model, while maintaining traditional DataGate record-level characteristics.

For the first time, DG for Visual Studio provides all of the same interfaces used by the Visual RPG compiler. The same powerful database engine used by Visual RPG is fully under your control for use in any .NET language. Visual RPG for .NET remains the language of choice for creating programs that access DataGate databases. However, with DG for .NET, Visual Basic programmers and others can access data with nearly the same efficiency. Likewise, Visual RPG programmers will appreciate DG for its object management capabilities.

Many common database application functions are facilitated by DG for Visual Studio, including the following:

- Retrieve, display, and update data with a record-level access paradigm.
- Print a report using a DataGate OLE print file.
- Call a stored procedure on the database server.
- Determine if a file’s format has changed prior to opening.
- Compose database network connection parameters on-the-fly.

All of these tasks and more can be accomplished with the help of a few DG objects.
<br />



| Task | Object |
| ---- | ---- |
| [File/data access](usingthe-file-adapter-class.html) | [ASNA.DataGate.Client.FileAdapter](file-adapter-class.html) and [ASNA.DataGate.Client.AdgDataSet](adg-dataset-class.html) classes provide the core functionality. [AdgDataSet](adg-dataset-class.html) inherits <span>System.Data.DataSet</span> and its rich ADO.NET utility. |
| [Manage database connections ](dcsManagingDatabaseConnectionsMain.html) | The [ASNA.DataGate.Client.AdgConnection](adg-connection-class.html) and [ASNA.DataGate.Providers.SourceProfile](source-profile-class.html) classes manage database connections and connection parameters including DataGate database names and transaction processing. |
| [Stored procedure call ](calling-stored-procedures.html) | Functionality provided by: - [ASNA.DataGate.Client.As400Program](as400program-class.html) - [ASNA.DataGate.DataLink.ProgParm](prog-parm-class.html) - [ASNA.DataGate.DataLink.ProgParmType](prog-parm-type-class.html) |



<br />

