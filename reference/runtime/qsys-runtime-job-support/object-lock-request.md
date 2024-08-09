---
title: "ObjectLockRequest class       | QSYS API Reference Guide"
description: "Provides facilities to Allocate and De-Allocate object related. "
last_modified_at: 2024-08-09T17:25:29Z
---

Provides facilities to Allocate and De-Allocate object related.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [ObjectLockRequest](#objectlockrequestadgconnection)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Initializes a new instance of the ObjectLockRequest.

### ObjectLockRequest([AdgConnection](/reference/datagate/datagate-client/adg-connection.html))

Initializes a new instance of the ObjectLockRequest.

```cs
ObjectLockRequest(AdgConnection)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the objects to be allocate.

## Methods

| Signature | Description |
| --- | --- |
| [AddDataArea](#void-adddataareastring-dataareapath-sharetypes-sharetype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Adds a data area to the list of objects to allocate.
| [AddFile](#void-addfilestring-filepath-sharetypes-sharetype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Adds a file to the list of objects to allocate.
| [AddLibrary](#void-addlibrarystring-libraryname-sharetypes-sharetype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Adds a library to the list of objects to allocate.
| [AddMember](#void-addmemberstring-filepath-string-member-sharetypes-sharetype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Adds a file member to the list of objects to allocate.
| [AllocateDataArea](#void-allocatedataareaadgconnection-connection-string-pathname-sharetypes-sharetype-waitoptions-waitoption-short-waittime)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Allocates an individual Data Area.
| [AllocateFile](#void-allocatefileadgconnection-connection-string-pathname-sharetypes-sharetype-waitoptions-waitoption-short-waittime)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Allocates an individual File.
| [AllocateLibrary](#void-allocatelibraryadgconnection-connection-string-pathname-sharetypes-sharetype-waitoptions-waitoption-short-waittime)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Allocates an individual Library.
| [AllocateMember](#void-allocatememberadgconnection-connection-string-pathname-sharetypes-sharetype-waitoptions-waitoption-short-waittime)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html), [WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Allocates an individual file Member.
| [AllocateObjects](#void-allocateobjectswaitoptions-waitoption-short-waittime)([WaitOptions](/reference/datagate/datagate-common/wait-options.html), [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16)) | Allocate the objects in the list.
| [DeallocateDataArea](#void-deallocatedataareaadgconnection-connection-string-pathname-sharetypes-sharetype)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Deallocates an individual Data Area.
| [DeallocateFile](#void-deallocatefileadgconnection-connection-string-pathname-sharetypes-sharetype)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Deallocates an individual File.
| [DeallocateLibrary](#void-deallocatelibraryadgconnection-connection-string-pathname-sharetypes-sharetype)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Deallocates an individual Library.
| [DeallocateMember](#void-deallocatememberadgconnection-connection-string-pathname-sharetypes-sharetype)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [ShareTypes](/reference/datagate/datagate-common/share-types.html)) | Deallocates an individual file Member.
| [DeallocateObjects()](#void-deallocateobjects) | Deallocate all objects held in the list.

### void AddDataArea([string dataAreaPath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Adds a data area to the list of objects to allocate.

```cs
void AddDataArea(string dataAreaPath, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dataAreaPath | Path of the data area to include in the allocation list.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.

### void AddFile([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Adds a file to the list of objects to allocate.

```cs
void AddFile(string filePath, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path of the file to include in the allocation list.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.

### void AddLibrary([string libraryName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Adds a library to the list of objects to allocate.

```cs
void AddLibrary(string libraryName, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | libraryName | Library to include in the allocation list.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.

### void AddMember([string filePath](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string member](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Adds a file member to the list of objects to allocate.

```cs
void AddMember(string filePath, string member, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | filePath | Path of the member's parent file.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | member | Name of member to include in the allocation list.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.

### void AllocateDataArea([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html), [WaitOptions waitOption](/reference/datagate/datagate-common/wait-options.html), [short waitTime](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Allocates an individual Data Area.

```cs
void AllocateDataArea(AdgConnection connection, string pathName, ShareTypes shareType, WaitOptions waitOption, short waitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be allocate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the data area to allocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | waitOption | One of enumeration values that specifies how to wait for the object allocation.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | waitTime | Maximum number of seconds to wait for the object to be allocated.

### void AllocateFile([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html), [WaitOptions waitOption](/reference/datagate/datagate-common/wait-options.html), [short waitTime](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Allocates an individual File.

```cs
void AllocateFile(AdgConnection connection, string pathName, ShareTypes shareType, WaitOptions waitOption, short waitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be allocate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the file to allocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | waitOption | One of enumeration values that specifies how to wait for the object allocation.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | waitTime | Maximum number of seconds to wait for the object to be allocated.

### void AllocateLibrary([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html), [WaitOptions waitOption](/reference/datagate/datagate-common/wait-options.html), [short waitTime](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Allocates an individual Library.

```cs
void AllocateLibrary(AdgConnection connection, string pathName, ShareTypes shareType, WaitOptions waitOption, short waitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be allocate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the library to allocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | waitOption | One of enumeration values that specifies how to wait for the object allocation.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | waitTime | Maximum number of seconds to wait for the object to be allocated.

### void AllocateMember([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html), [WaitOptions waitOption](/reference/datagate/datagate-common/wait-options.html), [short waitTime](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Allocates an individual file Member.

```cs
void AllocateMember(AdgConnection connection, string pathName, ShareTypes shareType, WaitOptions waitOption, short waitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be allocate.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the member (library/file/member) to allocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share to request.
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | waitOption | One of enumeration values that specifies how to wait for the object allocation.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | waitTime | Maximum number of seconds to wait for the object to be allocated.

### void AllocateObjects([WaitOptions waitOption](/reference/datagate/datagate-common/wait-options.html), [short waitTime](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Allocate the objects in the list.

```cs
void AllocateObjects(WaitOptions waitOption, short waitTime)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [WaitOptions](/reference/datagate/datagate-common/wait-options.html) | waitOption | One of enumeration values that specifies how to wait for each object allocation.
| [Int16](https://docs.microsoft.com/en-us/dotnet/api/system.int16) | waitTime | Maximum number of seconds to wait for each object to be allocated.

### void DeallocateDataArea([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Deallocates an individual Data Area.

```cs
void DeallocateDataArea(AdgConnection connection, string pathName, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be released.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the data area to deallocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share used to originally allocate the object.

### void DeallocateFile([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Deallocates an individual File.

```cs
void DeallocateFile(AdgConnection connection, string pathName, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be released.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the file to deallocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share used to originally allocate the object.

### void DeallocateLibrary([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Deallocates an individual Library.

```cs
void DeallocateLibrary(AdgConnection connection, string pathName, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be released.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the library to deallocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share used to originally allocate the object.

### void DeallocateMember([AdgConnection connection](/reference/datagate/datagate-client/adg-connection.html), [string pathName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [ShareTypes shareType](/reference/datagate/datagate-common/share-types.html))

Deallocates an individual file Member.

```cs
void DeallocateMember(AdgConnection connection, string pathName, ShareTypes shareType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | connection | The connection to the database holding the object to be released.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pathName | Path of the member to deallocate.
| [ShareTypes](/reference/datagate/datagate-common/share-types.html) | shareType | Type of share used to originally allocate the object.

### void DeallocateObjects()

Deallocate all objects held in the list.

```cs
void DeallocateObjects()
```
