---
title: "AdgConnection.Dispose Method"
description: "Releases all resources used by the AdgConnection."
---

## Definition

**Namespace:** ASNA.DataGate.Client<br/>
**Assembly:** ASNA.QSys.DataGate.Client.dll

Releases all resources used by the AdgConnection.


## Overloads

| Signature | Description |
| --- | --- |
| [Dispose()](#void-dispose) | Releases all resources used by the AdgConnection.
| [Dispose](#void-disposebool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the AdgConnection.

 
This method sets the `State` property of the **AdgConnection** object to Closed .  Additionally, if the current value of State is Open , the connection to the database provider is released, along with any unmanaged resources associated with that connection. 

 
Note that you must explicitly call either the [Close](adg-connection-close.html) or **Dispose** methods on **AdgConnection** objects in the Open state before the objects are finalized. This releases unmanaged resources associated with their database connections.  If unmanaged resources are not released prior to object finalization, unexpected results can occur, including program termination and loss of data.



### void Dispose()

Releases all resources used by the AdgConnection.


#### Remarks
This method disposes the AdgConnection by calling the Dispose method with the argument true. The Dispose method releases all resources used by the AdgConnection, including the underlying database connection. After the connection is disposed, it cannot be used again. The GC.SuppressFinalize(this) call prevents the garbage collector from calling the finalizer if it was overridden, which could have also disposed the object. This is done for performance reasons, since the object has already been disposed.

```cs
void Dispose()
```

### void Dispose([bool isDisposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the resources used by the AdgConnection.


#### Remarks
This method is called by the public Dispose() method and the Finalize method. Dispose() invokes the protected Dispose() method with the isDisposing parameter set to true. Finalize invokes Dispose with isDisposing set to false.When the isDisposing parameter is true, this method releases all resources held by any managed objects that this AdgConnection references. 

This method invokes the Dispose() method of each referenced object.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | A boolean value that indicates whether the method call comes from a Dispose method (its value is true) or from a finalizer (its value is false).


## See Also

[AdgConnection Class](adg-connection.html)