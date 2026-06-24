---
title: "Managing Database Connections"
description: "Learn how to manage database connections effectively."
---

[AdgConnection](/reference/datagate/datagate-client/adg-connection.html) objects exist in one of two modes, as reflected by the [State](/reference/datagate/datagate-client/adg-connection.html#properties) property. Initially, **AdgConnection** objects are in the **Closed** state. After successful execution of the [ Open](/reference/datagate/datagate-client/adg-connection-open.html) method, the **AdgConnection** object is in the **Open** state. When open, **AdgConnection** objects represent a live connection to the database and can be used with other DG objects and methods to perform access operations.

Prior to calling **Open**, you can use the [ SourceProfile](/reference/datagate/datagate-client/adg-connection.html#properties) property to modify connection parameters. Changes to  **SourceProfile**  affect subsequent  **Open**  method calls. The characteristics of the database connection cannot be changed when in the Open state. 

See how to [Configuring a Database Name Store](/manuals/configuration/database-names.html) for a further introduction to  **SourceProfile** .
## See Also


[AdgConnection Class](/reference/datagate/datagate-client/adg-connection.html)
      <br />
[Open Method](/reference/datagate/datagate-client/adg-connection-open.html)
      <br />
[SourceProfile Property](/reference/datagate/datagate-client/adg-connection.html#properties)
      <br />
[AdgConnection.State Property](/reference/datagate/datagate-client/adg-connection.html#properties)
      <br />
[Configuring the Database Name Store](/manuals/configuration/database-names.html)
      <br />
[Connecting to a Database](connectingtoa-database-main.html)

