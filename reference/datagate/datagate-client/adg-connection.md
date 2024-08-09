---
title: "AdgConnection class           | QSYS API Reference Guide"
description: "The AdgConnection class controls database connection resources and allows them to be shared among DataGate objects in your program.  "
last_modified_at: 2024-08-09T16:18:40Z
---

The AdgConnection class controls database connection resources and allows them to be shared among DataGate objects in your program. 

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. 

Any instance members are not guaranteed to be thread safe. 

A single instance of AdgConnection should not be shared by multiple threads of an application, unless application access to the instance is protected by a mutual exclusion mechanism, or unpredictable results may occur. 

For example, an ASP.NET application must take special care when using a shared instance of AdgConnection among multiple ASP.NET sessions. 

As an alternative, consider using a separate instance of AdgConnection (optionally configured for connection pooling via the [PoolingTimeout](/reference/datagate/datagate-providers/source-profile.html#properties) property of SourceProfile) in each ASP.NET session. Note also that other DG classes with properties and method parameters of type AdgConnection, such as FileAdapter, may employ the non-thread safe members of AdgConnection internally. By association, instance members of these classes are not guaranteed to be thread safe. 



## Constructors

| Name | Description |
| --- | --- |
| [AdgConnection](#adgconnectionsourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the AdgConnection class with the specified SourceProfile.
| [AdgConnection](#adgconnectionsourceprofile-iexchange5250)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html)) | Initializes a new instance of the AdgConnection class with the specified SourceProfile and IExchange5250.

### AdgConnection([SourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Initializes a new instance of the AdgConnection class with the specified SourceProfile.

```cs
AdgConnection(SourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The SourceProfile to be used for the connection.

### AdgConnection([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html))

Initializes a new instance of the AdgConnection class with the specified SourceProfile and IExchange5250.

```cs
AdgConnection(SourceProfile, IExchange5250)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | The SourceProfile to be used for the connection.
| [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html) | exchange5250 | The IExchange5250 to be used for the connection.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | Canceler | Gets or sets the cancellation token for the connection. |
| [IChannelSecurity](/reference/datagate/datagate-client/i-channel-security.html) | ChannelInfo | Gets the channel security information of the connection. |
| [ProtoLevel](https://learn.microsoft.com/en-us/dotnet/api/) | CurrentProtocolVersion | Gets the current protocol version. |
| [Decoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.decoder?view=net-8.0) | Decoder | Gets the Decoder of the connection. |
| [Encoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.encoder?view=net-8.0) | Encoder | Gets the Encoder of the connection. |
| [IMonitor](/reference/datagate/datagate-client/i-monitor.html) | Monitor | Gets the Monitor of the connection. |
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | SourceProfile | A copy of the SourceProfile object passed to the constructor. |
| [ConnectionState](https://learn.microsoft.com/en-us/dotnet/api/system.data.connectionstate?view=net-8.0) | State | Gets the state of the connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | TerminalDeviceName | Gets or sets the TerminalDeviceName property. |

## Methods

| Signature | Description |
| --- | --- |
| [BeginAutoTransaction](#iadgtransaction-beginautotransactiontransactionlevel-tl-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level and options.
| [BeginAutoTransaction](#iadgtransaction-beginautotransactionstring-name-string-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified name and options.
| [BeginAutoTransaction](#iadgtransaction-beginautotransactiontransactionlevel-tl-string-name-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level, name, and options.
| [BeginTransaction](#iadgtransaction-begintransactiontransactionlevel-tl)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html)) | Begins a transaction with the specified transaction level.
| [BeginTransaction](#iadgtransaction-begintransactionstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified name.
| [BeginTransaction](#iadgtransaction-begintransactiontransactionlevel-tl-string-name)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level and name.
| [BeginTransaction](#iadgtransaction-begintransactiontransactionlevel-tl-string-name-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level, name, and options.
| [Clone()](#object-clone) | Creates a new AdgConnection that is a copy of the current instance.
| [Close()](#void-close) | Closes the connection to the database.
| [Dispose()](#void-dispose) | Releases all resources used by the AdgConnection.
| [Dispose](#void-disposebool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the AdgConnection.
| [Equals](#bool-equalsobject-obj)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the current AdgConnection instance is equal to the specified object.
| [GetDatabaseAttributes()](#databaseattributes-getdatabaseattributes) | Gets the attributes of the database.
| [GetDeviceCodePageID()](#int-getdevicecodepageid) | Gets the device code page ID.
| [GetHashCode()](#int-gethashcode) | Serves as the default hash function.
| [GetPeerAltCodePageID()](#int-getpeeraltcodepageid) | Gets the peer alternative code page ID.
| [GetPeerVersion()](#protolevel-getpeerversion) | Gets the protocol level of the peer.
| [GetSourceProfileCopy()](#sourceprofile-getsourceprofilecopy) | Return a deep-copy of the current value of .
| [GetSupportsMultiMember()](#bool-getsupportsmultimember) | Gets a value indicating whether the connection supports multi-member files.
| [IsCanceledException](#bool-iscanceledexceptionexception-e)([Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Determines whether the specified exception is due to a cancellation request.
| [op_Equality](#bool-op-equalityadgconnection-x-adgconnection-y)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Determines whether two AdgConnection instances are equal.
| [op_Inequality](#bool-op-inequalityadgconnection-x-adgconnection-y)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Determines whether two AdgConnection instances are not equal.
| [Open](#void-opencancellationtoken-ct)([CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the database with default options.
| [Open](#void-openopenoptions-openoptions-cancellationtoken-ct)([OpenOptions](/reference/datagate/datagate-providers/open-options.html), [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the database with the specified options.
| [Synchronized](#adgconnection-synchronizedadgconnection-cn)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Returns a synchronized (thread-safe) wrapper for the AdgConnection.

### IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified transaction level and options.


#### Remarks
This method begins a new automatic transaction with the specified transaction level and options.An automatic transaction is a transaction that is automatically committed or rolled back by the system.The transaction level determines the isolation level of the transaction.The options parameter can be used to specify additional options for the transaction.This method calls the BeginAutoTransaction method with an empty string for the name parameter, meaning the transaction will not have a name.

```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### IAdgTransaction BeginAutoTransaction([string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified name and options.


#### Remarks
This method begins a new automatic transaction with the specified name and options.An automatic transaction is a transaction that is automatically committed or rolled back by the system.The transaction level for this method is set to Medium by default.The name parameter can be used to specify a name for the transaction.The options parameter can be used to specify additional options for the transaction.

```cs
IAdgTransaction BeginAutoTransaction(string Name, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified transaction level, name, and options.


#### Remarks
This method begins a new automatic transaction with the specified transaction level, name, and options.An automatic transaction is a transaction that is automatically committed or rolled back by the system.The transaction level determines the isolation level of the transaction.The name parameter can be used to specify a name for the transaction.The options parameter can be used to specify additional options for the transaction.The transaction attributes are set to CommitAndRestart and RollbackAndRestart, meaning that if the transaction is committed or rolled back, it will automatically restart.

```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Name, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html))

Begins a transaction with the specified transaction level.


#### Remarks
This method begins a new transaction with the specified transaction level.The transaction level determines the isolation level of the transaction.This method calls the BeginTransaction method with an empty string for the name parameter, meaning the transaction will not have a name.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### IAdgTransaction BeginTransaction([string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins a transaction with the specified name.


#### Remarks
This method begins a new transaction with the specified name.The transaction level for this method is set to Medium by default.The name parameter can be used to specify a name for the transaction.

```cs
IAdgTransaction BeginTransaction(string Name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins a transaction with the specified transaction level and name.


#### Remarks
This method begins a new transaction with the specified transaction level and name.The transaction level determines the isolation level of the transaction.The name parameter can be used to specify a name for the transaction.This method calls the BeginTransaction method with an empty string for the options parameter, meaning the transaction will not have any additional options.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl, string Name)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Name](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins a transaction with the specified transaction level, name, and options.


#### Remarks
This method begins a new transaction with the specified transaction level, name, and options.The transaction level determines the isolation level of the transaction.The name parameter can be used to specify a name for the transaction.The options parameter can be used to specify additional options for the transaction.The transaction attributes are set to None, meaning that the transaction will not automatically restart if it is committed or rolled back.A new AdgTransaction object is created with the specified parameters and returned.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl, string Name, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | The transaction level for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Name | The name for the new transaction.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | The options for the new transaction.

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | A new IAdgTransaction representing the transaction.

### object Clone()

Creates a new AdgConnection that is a copy of the current instance.


#### Remarks
This method creates a new AdgConnection that is a copy of the current instance.It first gets a copy of the SourceProfile of the current connection.Then it creates a new AdgConnection with the copied SourceProfile.If the current connection is open, it also opens the new connection.The new connection is then returned.

```cs
object Clone()
```

### void Close()

Closes the connection to the database.


#### Remarks
This method closes the connection by calling the Dispose method. The Dispose method releases all resources used by the AdgConnection, including the underlying database connection. After the connection is closed, it cannot be reopened. To open a new connection, you need to create a new AdgConnection instance.

```cs
void Close()
```

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
This method is called by the public Dispose() method and the Finalize method. Dispose() invokes the protected Dispose() method with the isDisposing parameter set to true. Finalize invokes Dispose with isDisposing set to false.When the isDisposing parameter is true, this method releases all resources held by any managed objects that this AdgConnection references. This method invokes the Dispose() method of each referenced object.The method first checks if the connection is open and if certain conditions are met (SourceProfile.PoolingTimeout is not zero, m_exchange5250 is null, and SourceProfile is not an SQL client platform). If these conditions are met, it logs the closure and disconnects the connection from the ConnectionPooler instance.If the SourceProvider is not null, it logs the permanent disconnection and closes the SourceProvider. Finally, it sets the SourceProvider to null.Note: Because the Dispose method is called twice (once by the public Dispose method and once by the finalizer), this method checks the isDisposing parameter to make sure it doesn't execute certain code twice.

```cs
void Dispose(bool isDisposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | isDisposing | A boolean value that indicates whether the method call comes from a Dispose method (its value is true) or from a finalizer (its value is false).

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the current AdgConnection instance is equal to the specified object.


#### Remarks
This method checks if the specified object is an AdgConnection and if its SourceProfile is equal to the SourceProfile of the current instance.The SourceProfile is a property that contains the configuration settings for the connection, such as the database name, server name, and other connection parameters.If the specified object is not an AdgConnection or if its SourceProfile is different from the SourceProfile of the current instance, the method returns false.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | The object to compare with the current instance.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified object is an AdgConnection and its SourceProfile is equal to the SourceProfile of the current instance; otherwise, false.

### DatabaseAttributes GetDatabaseAttributes()

Gets the attributes of the database.


#### Remarks
This method retrieves the attributes of the database from the SourceProvider if the connection is open.The attributes include information about the database such as its name, version, and other metadata.If the connection is not open, it throws an ApplicationException.

```cs
DatabaseAttributes GetDatabaseAttributes()
```

### int GetDeviceCodePageID()

Gets the device code page ID.


#### Remarks
This method retrieves the device code page ID from the DataLinkSource if the connection is open.The device code page ID is used to determine the character encoding for the connection.If the connection is not open, it throws an ApplicationException.

```cs
int GetDeviceCodePageID()
```

### int GetHashCode()

Serves as the default hash function.


#### Remarks
This method overrides the base GetHashCode method and provides a hash code for the current AdgConnection instance.The hash code is obtained from the SourceProfile of the current instance.The SourceProfile is a property that contains the configuration settings for the connection, such as the database name, server name, and other connection parameters.

```cs
int GetHashCode()
```

### int GetPeerAltCodePageID()

Gets the peer alternative code page ID.


#### Remarks
This method retrieves the peer alternative code page ID from the DataLinkSource if the connection is open.The peer alternative code page ID is used to determine the character encoding for the connection.If the connection is not open, it throws an ApplicationException.

```cs
int GetPeerAltCodePageID()
```

### ProtoLevel GetPeerVersion()

Gets the protocol level of the peer.


#### Remarks
This method retrieves the protocol level of the peer from the DataLinkSource if the connection is open.The protocol level is used to determine the version of the protocol used for communication.If the connection is not open, it throws an ApplicationException.If the SourceProvider is not a DataLinkSource, it returns the current protocol version.

```cs
ProtoLevel GetPeerVersion()
```

### SourceProfile GetSourceProfileCopy()

Return a deep-copy of the current value of .


#### Remarks
Since the returned object is a copy, modifications to it have no effect on this AdgConnection instance.  

```cs
SourceProfile GetSourceProfileCopy()
```

### bool GetSupportsMultiMember()

Gets a value indicating whether the connection supports multi-member files.


#### Remarks
This method checks if the connection supports multi-member files. It first checks if the value is cached (m_supportsMultimember). If it is, it returns the cached value.If the value is not cached, it calls the GetSupportsMultiMemberFromProvider method to get the value from the provider and caches it.The value is cached to avoid unnecessary calls to the provider, improving performance.

```cs
bool GetSupportsMultiMember()
```

### bool IsCanceledException([Exception e](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Determines whether the specified exception is due to a cancellation request.


#### Remarks
This method checks if the cancellation token for the connection is CancellationToken.None.If it is, it returns false, because a cancellation request could not have been made.If the cancellation token is not CancellationToken.None, it calls the IsCanceledExceptionInternal method to check if the specified exception is due to a cancellation request.

```cs
bool IsCanceledException(Exception e)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | The exception to check.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the specified exception is due to a cancellation request; otherwise, false.

### bool op_Equality([AdgConnection x](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection y](/reference/datagate/datagate-client/adg-connection.html))

Determines whether two AdgConnection instances are equal.


#### Remarks
This operator checks if the two AdgConnection instances are the same instance, or if they are both null, in which case it returns true.If only one of them is null, it returns false.If neither of them is null, it calls the Equals method to determine if they are equal.

```cs
bool op_Equality(AdgConnection x, AdgConnection y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | x | The first AdgConnection to compare.
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | y | The second AdgConnection to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the two AdgConnection instances are equal; otherwise, false.

### bool op_Inequality([AdgConnection x](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection y](/reference/datagate/datagate-client/adg-connection.html))

Determines whether two AdgConnection instances are not equal.


#### Remarks
This operator checks if the two AdgConnection instances are not equal.It does this by using the equality operator (==) to check if the instances are equal, and then returns the opposite result.

```cs
bool op_Inequality(AdgConnection x, AdgConnection y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | x | The first AdgConnection to compare.
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | y | The second AdgConnection to compare.

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | true if the two AdgConnection instances are not equal; otherwise, false.

### void Open([CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens a connection to the database with default options.


#### Remarks
This method opens a connection to the database with default options.If the connection is already open, it returns immediately.It calls the Open method with the OpenOptions.Default parameter, meaning the connection will be opened with the default options.The ct parameter can be used to request cancellation of the operation. If the operation is canceled, it throws an OperationCanceledException.

```cs
void Open(CancellationToken ct)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | ct | A cancellation token that can be used to cancel the operation.

### void Open([OpenOptions openOptions](/reference/datagate/datagate-providers/open-options.html), [CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens a connection to the database with the specified options.


#### Remarks
This method opens a connection to the database with the specified options.If the connection is already open, it returns immediately.If the SourceProfile indicates that connection pooling is disabled, or if the SourceProfile is for an SQL client platform, or if there is an existing 5250 exchange or OpenAccess RPG session, or if the connection cannot be pooled, it creates a new SourceProvider and opens it with the specified options.If the connection is not pooled, it sets up the user portion of the library list if specified in the SourceProfile.If the connection is pooled, it retrieves the connection from the pool.After the connection is opened, it logs the operation and completes the opening of any existing 5250 exchange.

```cs
void Open(OpenOptions openOptions, CancellationToken ct)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [OpenOptions](/reference/datagate/datagate-providers/open-options.html) | openOptions | The options for opening the connection.
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | ct | A cancellation token that can be used to cancel the operation.

### AdgConnection Synchronized([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html))

Returns a synchronized (thread-safe) wrapper for the AdgConnection.


#### Remarks
This method checks if the provided AdgConnection is already a SyncConnection. If it is, it returns the connection as is. If it's not, it creates a new SyncConnection with the provided connection and returns it.If the provided connection is in the open state, it also opens the new SyncConnection.The SyncConnection is a thread-safe wrapper for the AdgConnection. It ensures that only one thread can access the AdgConnection at a time, which is necessary when multiple threads are working with the same connection.

```cs
AdgConnection Synchronized(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | The AdgConnection to synchronize.

#### Returns

| Type | Description
| --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | A thread-safe wrapper for the AdgConnection.

## Example 1. Constructor example.

```cs 
  try
  {
      AdgConnection dataBase = new AdgConnection("*Public/DG NET IBM i");
  }
  catch(dgException e)
  {
      //At this point, dataBase will be set to null.  Do error handling here.
      System.Windows.Forms.MessageBox.Show(e.Message, "Unable to create connection.");
  }
```

## Example 2. Use of ConnctionState Property.

```cs 
  /* Here we need to use an AdgConnection "dataBase" to open
     a file.  We first check to make sure that the AdgConnection has 
     been initialized and that the connection has been made to
     avoid throwing an exception. */
  FileAdapter dbFile =  null;
  AdgDataSet dataSet = null;
  if (dataBase != null &amp;&amp; dataBase.State == ConnectionState.Open)
  {
     dbFile = new FileAdapter(dataBase);
     dbFile.OpenNewAdgDataSet(out dataSet);
  }
  else
  { 
     //If the AdgConnection was not ready, you cannot immediately
     //open the file, so take alternative action here.
  }
```

## Example 3. Use of SourceProfile Property.


```cs 
  AdgConnection Cx;
  Cx = new AdgConnection("*Public/DG NET IBM i");
  MessageBox.Show("The database name \"*Public/DG NET IBM i\" refers to a connection to "
           + Cx.SourceProfile.Server + " on port " + Cx.SourceProfile.Port.ToString());
```

## Example 4. Use of Open method.

```cs 
  try
  {
      AdgConnection dataBase = new AdgConnection("*Public/DG NET IBM i");
      dataBase.Open();
  }
  catch(dgException e)
  {
      System.Windows.Forms.MessageBox.Show(e.Message, "Error establishing connection to database.");
  }
```

## Example 5. Use of Close method.

```cs 
  //Disconnects from the dataBase by closing the connection.
  adg.Close();
```
