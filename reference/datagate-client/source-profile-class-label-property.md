---
title: SourceProfile.Label Property

---

For server platforms that support multiple databases, the label of the database to connect to. 

```cs
 public string Label { get; set; }
```


## Property Value

String. Returns or sets a string containing the label of the database to connect to.
## Remarks

The **Label** property specifies a particular database instance on the server platform for database engines that allow more than one server instance, such as DataGate Windows Server and SQL Server.

For single-instance platforms, such as the iSeries, the **Label** property is ignored.
## Examples


```cs 
  /* Register the database name "My Local" to specify the local database.
   * Because the local database is a Windows DataGate server, 
   * you need to include a valid label as well. */
  SourceProfile newDbProfile = new SourceProfile("My Local", false);
  newDbProfile.Server = "*LOCAL";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Label = "DG 7 Database";
  newDbProfile.PoolingTimeout = 0;
  /* Specify *DATALINK since we're connecting to the datagate engine. */
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();
```

## Requirements

**Namespace:** [ASNA.DataGate.Providers](datagate-providers-namespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8, Windows 8.1, Windows 10</span> 
## See Also


[SourceProfile Class](source-profile-class.html)
      <br />
[SourceProfile Class Members](source-profile-members.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

