---
title: AdgConnection class
---

DataGate connection.

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

As an alternative, consider using a separate instance of AdgConnection (optionally configured for connection pooling via the [PoolingTimeout](/reference/datagate/data-gate-providers/source-profile.html#properties) property of SourceProfile) in each ASP.NET session. Note also that other DG classes with properties and method parameters of type AdgConnection, such as FileAdapter, may employ the non-thread safe members of AdgConnection internally. By association, instance members of these classes are not guaranteed to be thread safe. 


## Constructors

| Name | Description |
| --- | --- |
| [AdgConnection](#adgconnection-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes AdgConnection instance.
| [AdgConnection](#adgconnection-string-iexchange5250-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html)) | Initializes AdgConnection instance.
| [AdgConnection](#adgconnection-sourceprofile-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the  class with the specified .
| [AdgConnection](#adgconnection-sourceprofile-iexchange5250-)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html)) | Initializes a new instance of the  class with the specified .

### AdgConnection([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes AdgConnection instance.

```cs
AdgConnection(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dbName | 

### AdgConnection([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html))

Initializes AdgConnection instance.

```cs
AdgConnection(String, IExchange5250)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | dbName | 
| [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html) | exchange5250 | 

### AdgConnection([SourceProfile](/reference/datagate/datagate-providers/source-profile.html))

Initializes a new instance of the  class with the specified .

```cs
AdgConnection(SourceProfile)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | 

### AdgConnection([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html))

Initializes a new instance of the  class with the specified .

```cs
AdgConnection(SourceProfile, IExchange5250)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | sp | 
| [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html) | exchange5250 | 

## Properties

| Type | Name | Description
| --- | --- | --- 
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | Canceler | Gets the canceler cancellation token instance. |
| [IChannelSecurity](/reference/datagate/datagate-client/i-channel-security.html) | ChannelInfo | Gets the channel security information associated with the AdgConnection. |
| [ProtoLevel](/reference/datagate/datagate-data-link/proto-level.html) | CurrentProtocolVersion | Gets the current protocol version. |
| [Decoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.decoder?view=net-8.0) | Decoder | Gets the decoder associated with the AdgConnection. |
| [Encoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.encoder?view=net-8.0) | Encoder | Gets the encoder associated with the AdgConnection. |
| [IMonitor](/reference/datagate/datagate-client/i-monitor.html) | Monitor | Gets the monitor associated with the AdgConnection. |
| [OpenAccessRpg](/reference/datagate/datagate-data-link/open-access-rpg.html) | OpenAccessRpg | Gets or sets the OpenAccessRpg object associated with the AdgConnection. |
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | SourceProfile | A reference to the SourceProfile object representing the liveconnection parameters.  At AdgConnection construction, the valueof this property is initialized by the parameters of theconstructor.  Modifications to the instance have no effect untilthe connection is opened (or re-opened).  A deep-copy of the valueof this property is available via the GetSourceProfileCopy method. |
| [ConnectionState](https://learn.microsoft.com/en-us/dotnet/api/system.data.connectionstate?view=net-8.0) | State | Gets the current state of the AdgConnection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | TerminalDeviceName | Gets or sets the terminal device name associated with the AdgConnection. |

## Methods

| Signature | Description |
| --- | --- |
| [GetSourceProfileCopy()](#getsourceprofilecopy-) | Return a deep-copy of the SourceProfile associated with thisconnection.  Since the returned object is a copy, modifications toit have no effect on the AdgConnection instance.  
| [GetDeviceCodePageID()](#getdevicecodepageid-) | Gets the device code page ID associated with the AdgConnection.
| [GetPeerAltCodePageID()](#getpeeraltcodepageid-) | Gets the Peer Alt Code Page ID associated with the AdgConnection.
| [GetSupportsMultiMember()](#getsupportsmultimember-) | Gets the value indicating whether the connection supports multi-member.
| [GetPeerVersion()](#getpeerversion-) | Gets the protocol version of the connected peer.
| [Close()](#close-) | Closes the connection and disposes the AdgConnection instance.
| [Dispose()](#dispose-) | Disposes the AdgConnection instance.
| [Dispose](#dispose-boolean-)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Disposes the AdgConnection instance.
| [BeginAutoTransaction](#beginautotransaction-transactionlevel-string-)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begin auto transaction
| [BeginAutoTransaction](#beginautotransaction-string-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | 
| [BeginAutoTransaction](#beginautotransaction-transactionlevel-string-string-)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level, name, and options.
| [BeginTransaction](#begintransaction-transactionlevel-)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html)) | Begins an automatic transaction with the specified transaction level
| [BeginTransaction](#begintransaction-string-)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level, name, and options.
| [BeginTransaction](#begintransaction-transactionlevel-string-)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level, name, and options.
| [BeginTransaction](#begintransaction-transactionlevel-string-string-)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level, name, and options.
| [GetDatabaseAttributes()](#getdatabaseattributes-) | Gets the database attributes of the connected database.
| [Open](#open-cancellationtoken-)([CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens the connection using a cancelation token.
| [Open](#open-openoptions-cancellationtoken-)([OpenOptions](/reference/datagate/datagate-providers/open-options.html), [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens the connection using optios and cancelation token.
| [Clone()](#clone-) | Clones the AdgConnection instance.
| [op_Equality](#op_equality-adgconnection-adgconnection-)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Determines whether two AdgConnection instances are equal.
| [op_Inequality](#op_inequality-adgconnection-adgconnection-)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Determines whether two AdgConnection instances are different.
| [Equals](#equals-object-)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the passed in connection is equal to the current connection instance.
| [GetHashCode()](#gethashcode-) | Get connection instance hash code.
| [Synchronized](#synchronized-adgconnection-)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Synchronizes the given AdgConnection instance.
| [IsCanceledException](#iscanceledexception-exception-)([Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Determines if the exception given has been cancelled.

### SourceProfile GetSourceProfileCopy()

Return a deep-copy of the SourceProfile associated with thisconnection.  Since the returned object is a copy, modifications toit have no effect on the AdgConnection instance.  

```cs
SourceProfile GetSourceProfileCopy()
```

### int GetDeviceCodePageID()

Gets the device code page ID associated with the AdgConnection.

```cs
int GetDeviceCodePageID()
```

### int GetPeerAltCodePageID()

Gets the Peer Alt Code Page ID associated with the AdgConnection.

```cs
int GetPeerAltCodePageID()
```

### bool GetSupportsMultiMember()

Gets the value indicating whether the connection supports multi-member.

```cs
bool GetSupportsMultiMember()
```

### ProtoLevel GetPeerVersion()

Gets the protocol version of the connected peer.

```cs
ProtoLevel GetPeerVersion()
```

### void Close()

Closes the connection and disposes the AdgConnection instance.

```cs
void Close()
```

### void Dispose()

Disposes the AdgConnection instance.

```cs
void Dispose()
```

### void Dispose()

Disposes the AdgConnection instance.

```cs
void Dispose()
```

### IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begin auto transaction

```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | 

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | Transaction reference

### IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))



```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Options)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | Name | 
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | Options | 

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | 

### IAdgTransaction BeginAutoTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html), [string Options](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Begins an automatic transaction with the specified transaction level, name, and options.

```cs
IAdgTransaction BeginAutoTransaction(TransactionLevel tl, string Options)
```

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html))

Begins an automatic transaction with the specified transaction level

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | tl | 

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | The  representing the transaction.

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html))

Begins an automatic transaction with the specified transaction level, name, and options.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [TransactionLevel](/reference/datagate/datagate-common/transaction-level.html) | Name | 

#### Returns

| Type | Description
| --- | ---
| [IAdgTransaction](/reference/datagate/datagate-client/i-adg-transaction.html) | The  representing the transaction.

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html))

Begins a transaction with the specified transaction level, name, and options.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl)
```

### IAdgTransaction BeginTransaction([TransactionLevel tl](/reference/datagate/datagate-common/transaction-level.html))

Begins an automatic transaction with the specified transaction level, name, and options.

```cs
IAdgTransaction BeginTransaction(TransactionLevel tl)
```

### DatabaseAttributes GetDatabaseAttributes()

Gets the database attributes of the connected database.

```cs
DatabaseAttributes GetDatabaseAttributes()
```

### void Open([CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens the connection using a cancelation token.

```cs
void Open(CancellationToken ct)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | ct | 

### void Open([CancellationToken ct](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0))

Opens the connection using optios and cancelation token.

```cs
void Open(CancellationToken ct)
```

### object Clone()

Clones the AdgConnection instance.

```cs
object Clone()
```

### bool op_Equality([AdgConnection x](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection y](/reference/datagate/datagate-client/adg-connection.html))

Determines whether two AdgConnection instances are equal.

```cs
bool op_Equality(AdgConnection x, AdgConnection y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | x | 
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | y | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the instances are equal, otherwise false.

### bool op_Inequality([AdgConnection x](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection y](/reference/datagate/datagate-client/adg-connection.html))

Determines whether two AdgConnection instances are different.

```cs
bool op_Inequality(AdgConnection x, AdgConnection y)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | x | 
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | y | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the instances are different, otherwise false.

### bool Equals([object obj](https://docs.microsoft.com/en-us/dotnet/api/system.object))

Determines whether the passed in connection is equal to the current connection instance.

```cs
bool Equals(object obj)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) | obj | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the instances are equal, otherwise false.

### int GetHashCode()

Get connection instance hash code.

```cs
int GetHashCode()
```

### AdgConnection Synchronized([AdgConnection cn](/reference/datagate/datagate-client/adg-connection.html))

Synchronizes the given AdgConnection instance.

```cs
AdgConnection Synchronized(AdgConnection cn)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | cn | 

#### Returns

| Type | Description
| --- | ---
| [AdgConnection](/reference/datagate/datagate-client/adg-connection.html) | A synchronized AdgConnection instance.

### bool IsCanceledException([Exception e](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Determines if the exception given has been cancelled.

```cs
bool IsCanceledException(Exception e)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | 

#### Returns

| Type | Description
| --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | True if the exception has been cancelled, False otherwise.