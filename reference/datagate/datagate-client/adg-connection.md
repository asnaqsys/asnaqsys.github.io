---
title: "AdgConnection class           | QSYS API Reference Guide"
description: "The AdgConnection class controls database connection resources and allows them to be shared among DataGate objects in your program.  "
last_modified_at: 2024-08-09T17:25:07Z
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

## Remarks

An instance of **AdgConnection** represents a connection to a database server. The connection is initially in the Closed state, as reflected by the `State`property. Connection details are described by the `SourceProfile` property. Connection details are set in **AdgConnection** at construction and cannot be changed during the lifetime of the object.  

Several `Open` methods are available for transitioning **AdgConnection** to the Open state. When an **AdgConnection** object is in the Open state, the values of certain properties reflect the state of a server-side "job". Some job-oriented operations, such as commitment control, can be effected through **AdgConnection** methods.

An Open **AdgConnection** object may enter the Closed state via the `Close` method. Connections may also be closed via the **IDispose.Dispose** method. Note that it is the responsibility of the programmer to close database connections. If	 **AdgConnection** objects are garbage-collected in the Open state, the resulting state of the underlying connection resources (including network connections) is non-deterministic.

**AdgConnection** is used by other classes for specific functions such as record access and program call. DataGate objects may hold references to an **AdgConnection** instance, and those objects may assume that the **AdgConnection** object is in the Open state. When in the **Closed** state, the **AdgConnection** object must not be used by any object which references its database connection, or an exception may occur. Care should be taken not to call methods of DataGate objects which reference	 **AdgConnection** objects in the	**Closed**	state.



## Constructors

| Name | Description |
| --- | --- |
| [AdgConnection](adg-connection-ctor.html#adgconnectionsourceprofile)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html)) | Initializes a new instance of the AdgConnection class with the specified SourceProfile.
| [AdgConnection](adg-connection-ctor.html#adgconnectionsourceprofile-iexchange5250)([SourceProfile](/reference/datagate/datagate-providers/source-profile.html), [IExchange5250](/reference/datagate/datagate-providers/i-exchange5250.html)) | Initializes a new instance of the AdgConnection class with the specified SourceProfile and IExchange5250.


## Properties

| Type | Name | Description
| --- | --- | --- 
| [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0) | Canceler | Gets or sets the cancellation token for the connection. |
| [IChannelSecurity](/reference/datagate/datagate-client/i-channel-security.html) | ChannelInfo | Gets the channel security information of the connection. |
| [ProtoLevel](https://learn.microsoft.com/en-us/dotnet/api/) | CurrentProtocolVersion | Gets the current protocol version. |
| [Decoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.decoder?view=net-8.0) | Decoder | Gets the Decoder of the connection. |
| [Encoder](https://learn.microsoft.com/en-us/dotnet/api/system.text.encoder?view=net-8.0) | Encoder | Gets the Encoder of the connection. |
| [IMonitor](/reference/datagate/datagate-client/i-monitor.html) | Monitor | Gets the Monitor of the connection. |
| [SourceProfile](/reference/datagate/datagate-providers/source-profile.html) | SourceProfile | A copy of the SourceProfile object passed to the constructor. <br> The `Open` method utilizes this property to establish a database connection with specific characteristics as required by the user.  The property can be set explicitly, or via the `AdgConnection constructor.`<br/> Note that changing the value of this property, or changing the object referenced by this property, has no effect on the current database connection (if `State` indicates Open).  The database connection is only influenced by this property via the `AdgConnection.Open` method.|
| [ConnectionState](https://learn.microsoft.com/en-us/dotnet/api/system.data.connectionstate?view=net-8.0) | State | Gets the state of the connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | TerminalDeviceName | Gets or sets the TerminalDeviceName property. |

## Methods

| Signature | Description |
| --- | --- |
| [BeginAutoTransaction](adg-connection-begin-auto-transaction.html#iadgtransaction-beginautotransactiontransactionlevel-tl-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level and options.
| [BeginAutoTransaction](adg-connection-begin-auto-transaction.html#iadgtransaction-beginautotransactionstring-name-string-options)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified name and options.
| [BeginAutoTransaction](adg-connection-begin-auto-transaction.html#iadgtransaction-beginautotransactiontransactionlevel-tl-string-name-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins an automatic transaction with the specified transaction level, name, and options.
| [BeginTransaction](adg-connection-begin-transaction.html#iadgtransaction-begintransactiontransactionlevel-tl)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html)) | Begins a transaction with the specified transaction level.
| [BeginTransaction](adg-connection-begin-transaction.html#iadgtransaction-begintransactionstring-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified name.
| [BeginTransaction](adg-connection-begin-transaction.html#iadgtransaction-begintransactiontransactionlevel-tl-string-name)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level and name.
| [BeginTransaction](adg-connection-begin-transaction.html#iadgtransaction-begintransactiontransactionlevel-tl-string-name-string-options)([TransactionLevel](/reference/datagate/datagate-common/transaction-level.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Begins a transaction with the specified transaction level, name, and options.
| [Clone()](adg-connection-clone.html) | Creates a new AdgConnection that is a copy of the current instance.
| [Close()](adg-connection-close.html) | Closes the connection to the database.
| [Dispose()](adg-connection-dispose.html#void-dispose) | Releases all resources used by the AdgConnection.
| [Dispose](adg-connection-dispose.html#void-disposebool-isdisposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the AdgConnection.
| [Equals](adg-connection-equals.html)([Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Determines whether the current AdgConnection instance is equal to the specified object.
| [GetDatabaseAttributes()](adg-connection-get-database-attributes.html) | Gets the attributes of the database.
| [GetDeviceCodePageID()](adg-connection-get-device-code-page-id.html) | Gets the device code page ID.
| GetHashCode() | Serves as the default hash function.
| [GetPeerAltCodePageID()](adg-connection-get-peer-alt-code-page-id.html) | Gets the peer alternative code page ID.
| [GetPeerVersion()](adg-connection-get-peer-version.html) | Gets the protocol level of the peer.
| [GetSourceProfileCopy()](adg-connection-get-source-profile-copy.html) | Return a deep-copy of the current value of the connection's source profile.
| [GetSupportsMultiMember()](#bool-getsupportsmultimember.html) | Gets a value indicating whether the connection supports multi-member files.
| [IsCanceledException](adg-connection-is-canceled-exception.html)([Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Determines whether the specified exception is due to a cancellation request.
| [op_Equality](adg-connection-operator-equals.html)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Determines whether two AdgConnection instances are equal.
| [op_Inequality](adg-connection-operator-not-equal.html)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html), [AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Determines whether two AdgConnection instances are not equal.
| [Open](adg-connection-open.html#void-opencancellationtoken-ct)([CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the database with default options.
| [Open](adg-connection-open.html#void-openopenoptions-openoptions-cancellationtoken-ct)([OpenOptions](/reference/datagate/datagate-providers/open-options.html), [CancellationToken](https://learn.microsoft.com/en-us/dotnet/api/system.threading.cancellationtoken?view=net-8.0)) | Opens a connection to the database with the specified options.
| [Synchronized](adg-connection-synchronized.html)([AdgConnection](/reference/datagate/datagate-client/adg-connection.html)) | Returns a synchronized (thread-safe) wrapper for the AdgConnection.



## Examples

### Create an AdgConnection

Shows how to `new` an `AdgConnection` using a Database Source Profile Name.

```cs 

    IDataGateConfig dgConfig;

    public void PrepareStore(params string[] configJsonFiles) 
    {
        ConfigurationBuilder builder = new ConfigurationBuilder();
        builder.AddJsonFile(AsnaConfigHelper.DefaultConfigFilePath);
        foreach (var configFile in configJsonFiles)
            builder.AddJsonFile(configFile);
        IAsnaConfig config = new AsnaConfig(builder.Build());
        dgConfig = config.DataGate;
    }

    private AdgConnection createAdgConnection(string dbName)
    {
        SourceProfile sourceProfile = dgConfig.ResolveSourceName(dbName);
        AdgConnection dbConnection = new AdgConnection(sourceProfile);
        return dbConnection;
    }


    public void start()
    {
        PrepareStore(AsnaConfigHelper.DefaultConfigFilePath, "./appsetting.json");
        . . . 
        AdgConnection dbConnection = createAdgConnection("MyDatabaseName");
        dbConnection.Open();
        . . .
        . . .
        //Disconnects from the dataBase by closing the connection.
        dbConnection.Close();
    }

```

### Open a Database File

See [Create an AdgConnection](#create-an-adgconnection)

```cs 

    private FileAdapter openCustomerFile(AdgConnection dbConnection, out AdgDataSet dataSet)
    {
        /* Here we need to use an AdgConnection to open the Customer File.
          We first check to make sure that the AdgConnection has 
          been initialized and that the connection has been made to
          avoid throwing an exception. */

        FileAdapter dbFile =  null;
        dataSet = null;
        if (dbConnection != null && dbConnection.State == ConnectionState.Open)
        {
          dbFile = new FileAdapter(dbConnection, "MyLibrary/CustMast");
          dbFile.OpenAttributes.FileLocks = FileLocks.Auto;
          dbFile.AccessMode = AccessMode.RWCD;
          dbFile.OpenNewAdgDataSet(out dataSet);
          return dbFile;
        }

        //If the AdgConnection was not ready, you cannot immediately
        //open the file, so take alternative action here.
        . . . 
    }

    public void start()
    {
        PrepareStore(AsnaConfigHelper.DefaultConfigFilePath, "./appsetting.json");
        . . . 
        AdgConnection dbConnection = createAdgConnection("MyDatabaseName");
        dbConnection.Open();

        AdgDataSet dataSet;       
        FileAdapter dbFile = openCustomerFile(dbConnection, out dataSet);
        . . .
        . . .
        dbFile.Close();

        //Disconnects from the dataBase by closing the connection.
        dbConnection.Close();
    }

```
