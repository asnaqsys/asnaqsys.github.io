---
title: "How to Disconnect from a Database Safely"
description: "Learn the best practices for safely disconnecting from a database, ensuring data integrity and system stability."
---

After database connection and access are complete, applications *must* disconnect from the database to properly release un-managed resources. These un-managed resources are provided to DG by the <span>Common Language Runtime (CLR)</span> for network access. In general, DG and the CLR will not release these un-managed resources for you, and if not released, unexpected results, including loss of data, can occur. You must explicitly release un-managed resources associated with **AdgConnection** objects using the [ AdgConnection.Close](adg-connection-class-close-method.html) or [AdgConnection.Dispose](adg-connection-class-dispose-method.html) methods. You should call one of these methods before the **AdgConnection** variable loses scope or is reassigned.

```cs 
  Cx.Close();
  Cx = null;
```

Whether you use <span> **AdgConnection.Close** </span> or <span> **AdgConnection.Dispose** </span> is a matter of preference since they perform the same task of disconnecting the database and releasing un-managed resources. Note that <span> **AdgConnection.Dispose** </span> implements the conventional <span> **System.IDisposable** </span> interface for **AdgConnection**. 

## See Also
[AdgConnection Class](adg-connection-class.html) <br />
[AdgConnection.Close Method](adg-connection-class-close-method.html) <br />
[AdgConnection.Dispose Method](adg-connection-class-dispose-method.html) <br />
[Connecting to a Database](connectingtoa-database.html)

