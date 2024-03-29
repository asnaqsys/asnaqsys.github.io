---
title: SourceProfile.GetNames Method

---

## <span style="font-color:red">Deprecated</span>
Replaced by [DatabaseName.GetNames](database-name-class-get-names-method.html)

Returns the currently registered database names available for use in a program.

```cs
 public static string[] GetNames( bool publicDbs );
```


## Parameters



 *publicDbs* 

: The public database.
					


## Returns

String. The currently registered database names available for use in a program.
## Examples 


```cs 
  /* This code will fill a combo box with all of the available database
   * names. */
  foreach(string name in SourceProfile.GetNames(true)) /* Get *PUBLIC 
            databases. */
      cbDbName.Items.Add(name); /* NOTE: The names 
            appear without the "*PUBLIC/" prefix. */
  foreach(string name in SourceProfile.GetNames(false)) /* Get non public 
            databases. */
      cbDbName.Items.Add(name);
```

## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
## See Also


      <span>
[SourceProfile Class](source-profile-class.html) <br />[
						SourceProfile Class Members](source-profile-members.html)<br />[
						Register Method](source-profile-class-register-method.html)<br />[Unregister 
						Method](source-profile-class-unregister-method.html)<br />[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)</span>  

