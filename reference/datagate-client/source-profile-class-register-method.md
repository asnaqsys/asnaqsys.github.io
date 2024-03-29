---
title: SourceProfile.Register Method

---

## <span style="font-color:red">Deprecated</span>
Replaced by [DatabaseName.Register](database-name-class-register-method.html)

Saves the contents of the **SourceProfile** object to the system registry as a database name.
<span style="MARGIN-BOTTOM: 0.8em" />

```cs
 public void Register();
```


## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| dgException | See table below. |



ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property. 
<br />



| Value of dgException.Error | Condition |
| ---- | ---- |
| dgEINVARG | The database name string (specified by the SourceProfile constructor) contains an invalid character. Path delimiter characters ('/' and '\') are not permitted in database names, unless used with "*PUBLIC"; for example "*PUBLIC/MyDB" is a valid database name, but "Copyof/MyDB" is not. |



Example <p>The following example retrieves a database name called "Asna 400 db" (in the process of constructing the SourceProfile object), changes the user and password, and then saves the changes by calling Register. 

```cs 
  /* When we specify false with this constructor, we're
   * telling Datagate not to get information from the
   * registry. Thus we can use it to create an entirely
   * new database name. */
  SourceProfile newDbProfile = new SourceProfile("New database", false);
  newDbProfile.Server = "valid ip address";
  newDbProfile.User = "User1";
  newDbProfile.Password = "password"; /* Note- not very secure. */
  newDbProfile.Port = 5047;
  newDbProfile.PoolingTimeout = 0;
  newDbProfile.PlatformAttribute = "*DATALINK";
  newDbProfile.Text = "New database at valid ip address, on port 5047.";
  /* Register the database name. */
  newDbProfile.Register();
```

## Requirements

**Namespace: [ ASNA.DataGate.Providers](datagate-providers-namespace.html)** 

**Assembly:** ASNA DataGate Client 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[SourceProfile Class](source-profile-class.html)
      <br />
[SourceProfile Class Members](source-profile-members.html)
      <br />
[Unregister Method](source-profile-class-unregister-method.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

