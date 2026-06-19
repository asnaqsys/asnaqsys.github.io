---
title: "As400Program.Dispose Method"
description: "Releases all resources used by the current instance of the class."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Releases all resources used by the current instance of the class.

## Overloads

| Signature | Description |
| --- | --- |
| [Dispose](#void-dispose)(void Dispose()) | Releases all resources used by the current instance of the class. |
| [Dispose](#void-dispose-bool-isdisposing)(void Dispose(bool isDisposing)) | Releases the unmanaged resources used by the and optionally releases the managed resources. |

<a id="void-dispose"></a>
## void Dispose()

Releases all resources used by the current instance of the  class.

#### Remarks
This method calls the Dispose method with the isDisposing parameter set to true, indicating that the method has been called directly or indirectly by a user's code. Then it requests that the common language runtime not call the finalizer for the specified object.

```cs
void Dispose()
```

<a id="void-dispose-bool-isdisposing"></a>
## void Dispose(bool isDisposing)

Releases the unmanaged resources used by the  and optionally releases the managed resources.

#### Remarks
This method is called by the public Dispose() method and the Finalize method. Dispose() invokes the protected Dispose() method with the isDisposing parameter set to true. Finalize invokes Dispose with isDisposing set to false.When the isDisposing parameter is true, this method releases all resources held by any managed objects that this As400Program references. This method invokes the Dispose() method of each referenced object.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | True to release both managed and unmanaged resources; false to release only unmanaged resources.

## See Also
- [As400Program class](as400-program.html)
