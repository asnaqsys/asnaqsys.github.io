---
title: SourceProfile(string, SourceProfile)

---

## <span style="font-color:red">Deprecated</span>
Replaced by [DatabaseName.ToSourceProfile(String, Bool)](database-name-class-to_source-profile-method2.html)

Constructs an instance of [SourceProfile](source-profile-class.html) that is an exact copy of the given SourceProfile, with the exception of the [DatabaseName](source-profile-class-database-name-property.html) property.

```cs
 public SourceProfile( string NewName, SourceProfile sp );
```


## Parameters



 *NewName* 

: String.  Sets the value of the **DatabaseName**  property. 
						

 *sp* 

: 
[SourceProfile](source-profile-class.html). The **SourceProfile** 
								to be copied by the constructed object.
							


## Exceptions



| Exception Type | Condition |
| ---- | ---- |
| NullReferenceException | *sp* or *NewName* is a null reference. |



## Remarks

All public properties of the constructed object have the same value as the copied **SourceProfile** *sp* , except for **DatabaseName** , which is assigned the value of *NewName* .

This constructor is useful for creating an object capable of registering database name information under a different name, via the [ Register](source-profile-class-register-method.html) method. 
## Examples


```cs 
  /* This creates a brand new database name using the
   * old source profile.*/
  SourceProfile newDbProfile2 = new SourceProfile("Brand New DB Name", sp);
```

## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
## See Also


[SourceProfile Class](source-profile-class.html)
      <br />
[SourceProfile Class Members](source-profile-members.html)
      <br />
[DatabaseName Property](source-profile-class-database-name-property.html)
      <br />
[Register Method](source-profile-class-register-method.html)
      <br />
[ASNA.DataGate.Providers Namespace](datagate-providers-namespace.html)

