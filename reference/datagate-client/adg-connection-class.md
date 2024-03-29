---
title: AdgConnection Class

---

The <span> **AdgConnection** </span> class controls database connection resources and allows them to be shared among DataGate objects in your program. 

For a list of all members of this type, see [AdgConnection Members](adg-connection-members.html).

[ASNA.DataGate.Client](datagate-client-namespace.html) <br /> **ASNA.DataGate.Client.<span>AdgConnection</span>** 

```cs
public class AdgConnection | System.ICloneable, System.IDisposable
```

## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe. 

A single instance of AdgConnection should not be shared by multiple threads of an application, unless application access to the instance is protected by a mutual exclusion mechanism, or unpredictable results may occur. For example, an ASP.NET application must take special care when using a shared instance of AdgConnection among multiple ASP.NET sessions. As an alternative, consider using a separate instance of AdgConnection (optionally configured for connection pooling via the [ PoolingTimeout](source-profile-class-pooling-timeout-property.html) property of SourceProfile) in each ASP.NET session. Note also that other DG classes with properties and method parameters of type AdgConnection, such as FileAdapter, may employ the non-thread safe members of AdgConnection internally. By association, instance members of these classes are not guaranteed to be thread safe. 
## Remarks

An instance of <span> **AdgConnection** </span> represents a connection to a database server. The connection is initially in the <span>Closed</span> state, as reflected by the [State](adg-connection-class-state-property.html) property. Connection details are described by the [ SourceProfile](adg-connection-class-source-profile-property.html) property. Connection details are set in <span> **AdgConnection** </span> at construction and cannot be changed during the lifetime of the object. 

Several [Open](adg-connection-class-open-method.html) methods are available for transitioning <span> **AdgConnection** </span> to the Open state. When an **AdgConnection** object is in the Open state, the values of certain properties reflect the state of a server-side "job". Some job-oriented operations, such as commitment control, can be effected through **AdgConnection** methods. 

An <span>Open</span> **AdgConnection** object may enter the <span>Closed</span> state via the [Close](adg-connection-class-close-method.html) method. Connections may also be closed via the <span> **IDispose.Dispose** </span> method. Note that it is the responsibility of the programmer to close database connections. If <span> **AdgConnection** </span> objects are garbage-collected in the Open state, the resulting state of the underlying connection resources (including network connections) is non-deterministic.

**<span>AdgConnection</span>** is used by other classes for specific functions such as record access and program call. DataGate objects may hold references to an <span> **AdgConnection** </span> instance, and those objects may assume that the <span> **AdgConnection** </span> object is in the Open state. When in the **Closed** state, the <span> **AdgConnection** </span> object must not be used by any object which references its database connection, or an exception may occur. Care should be taken not to call methods of DataGate objects which reference <span> **AdgConnection** </span> objects in the **Closed** state. 
## Requirements

**Namespace:** [ASNA.DataGate.Client](datagate-client-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[AdgConnection Members](adg-connection-members.html)
      <br />
[ASNA.DataGate.Client Namespace](datagate-client-namespace.html)

