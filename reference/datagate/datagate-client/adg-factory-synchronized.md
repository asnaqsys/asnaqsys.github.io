---
title: "AdgFactory.Synchronized Method"
description: "Wraps an in a synchronized (thread-safe) wrapper."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Wraps an in a synchronized (thread-safe) wrapper.

## Overloads

| Signature | Description |
| --- | --- |
| [Synchronized](#iadgobject-synchronized-iadgobject-adgobj)(IAdgObject Synchronized(IAdgObject adgObj)) | Wraps an in a synchronized (thread-safe) wrapper. |
| [Synchronized](#ilibrarylist-synchronized-ilibrarylist-llobj)(ILibraryList Synchronized(ILibraryList llObj)) | Wraps an in a synchronized (thread-safe) wrapper. |

<a id="iadgobject-synchronized-iadgobject-adgobj"></a>
## IAdgObject Synchronized(IAdgObject adgObj)

Wraps an  in a synchronized (thread-safe) wrapper.

#### Remarks
This method checks the type of the  parameter and wraps it in a corresponding synchronized (thread-safe) wrapper.If the object is already a synchronized object, it is returned as is.If the object is an , it is wrapped in a .If the object is an , it is wrapped in a .If the object is an , it is wrapped in a .If the object is an , it is wrapped in a .If the object is none of the above types, it is wrapped in a .

```cs
IAdgObject Synchronized(IAdgObject adgObj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | adgObj | The  to wrap.

#### Returns

| Type | Description
| --- | ---
| [IAdgObject](/reference/datagate/datagate-client/i-adg-object.html) | A thread-safe wrapper around the .

<a id="ilibrarylist-synchronized-ilibrarylist-llobj"></a>
## ILibraryList Synchronized(ILibraryList llObj)

Wraps an  in a synchronized (thread-safe) wrapper.

#### Remarks
This method checks if the  parameter is already a synchronized object. If it is, the method returns the object as is. If it's not, the method wraps it in a  to ensure thread safety.

```cs
ILibraryList Synchronized(ILibraryList llObj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | llObj | The  to wrap.

#### Returns

| Type | Description
| --- | ---
| [ILibraryList](/reference/datagate/datagate-client/i-library-list.html) | A thread-safe wrapper around the .

## See Also
- [AdgFactory class](adg-factory.html)
