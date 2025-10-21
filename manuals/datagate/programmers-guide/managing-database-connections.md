---
title: "Database Connection Management Tips"
description: "Learn how to manage database connections effectively. Our guide covers best practices for stability and performance."
---

[AdgConnection](/reference/datagate/datagate-client/adg-connection.html) objects exist in one of two modes, as reflected by the [State](/reference/datagate/datagate-client/adg-connection.html#properties) property. Initially, <span> **AdgConnection** </span> objects are in the <span>Closed</span> state. After successful execution of the [ Open](/reference/datagate/datagate-client/adg-connection-open.html) method, the **AdgConnection** object is in the <span>Open</span> state. When open, <span> **AdgConnection** </span> objects represent a live connection to the database and can be used with other DG objects and methods to perform access operations.

Prior to calling <span> **Open** </span>, you can use the [ SourceProfile](/reference/datagate/datagate-client/adg-connection.html#properties) property to modify connection parameters. Changes to <span> **SourceProfile** </span> affect subsequent <span> **Open** </span> method calls. The characteristics of the database connection cannot be changed when in the Open state. See the next topic [ Database Name Handling](database-name-handling.html) for a further introduction to <span> **SourceProfile** </span>.
## See Also


[AdgConnection Class](/reference/datagate/datagate-client/adg-connection.html)
      <br />
[Open Method](/reference/datagate/datagate-client/adg-connection-open.html)
      <br />
[SourceProfile Property](/reference/datagate/datagate-client/adg-connection.html#properties)
      <br />
[AdgConnection.State Property](/reference/datagate/datagate-client/adg-connection.html#properties)
      <br />
[Database Name Handling](database-name-handling.html)
      <br />
[Connecting to a Database](connectingtoa-database-main.html)

