---
title: SourceProfile Class

---

The <span>SourceProfile</span> class objects encapsulate the information required to create a database connection.

For a list of all members of this type, see [SourceProfile Members](source-profile-members.html).

[ASNA.DataGate.Providers](datagate-providers-namespace.html) <br /> ASNA.DataGate.Providers.<span>SourceProfile</span>
<pre class="syntax" >
        <span>&lt;Serializable&gt;</span>
 **Public Class SourceProfile** 
      </pre>

## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
## Remarks

An instance of **SourceProfile** is an in-memory representation of the information stored in the Windows registry for a DataGate "database name", as used by the DataGate Database Manager tool. **SourceProfile** provides methods to read and write registered database names from and to the registry on Windows platforms. [AdgConnection](adg-connection-class.html) objects require the information provided by **SourceProfile** to open database connections to the data provider. Through the **SourceProfile** object, **AdgConnection** is not dependent upon the Windows registry for connecting to a database provider.


**AdgConnection's** 

[ SourceProfile](adg-connection-class-source-profile-property.html) property is set by it is constructor in one of two ways. A valid **SourceProfile** object can be passed as a reference in the **AdgConnection** [constructor](adg-connection-constructors-main.html). Alternately, **AdgConnection** can be constructed with a valid database name string, in which case a **SourceProfile** object is created to import the registered database name information. Thus, the application programmer can use **SourceProfile** to directly manipulate database connection information or to interface with registered database names.


**SourceProfile** can be constructed in one of the following three ways:

- **With default values.**   After this construction, the 
					application must set the value of all relevant properties before the **SourceProfile** 
					can be used with **AdgConnection** 
				to connect to a database provider.
- **By database name** .  This construction imports 
				connection information stored in the Windows registry by the given name.
- **By copying** .  Connection information is copied from a 
					given **SourceProfile**  instance and the value of the **DatabaseName** 
					property is optionally reset.

**SourceProfile** can create or update a registered database name with the [Register](source-profile-class-register-method.html) method. To delete database name information from the Windows registry, the [ Unregister](source-profile-class-unregister-method.html) method is used. To retrieve a list of currently registered database names, use the [ GetNames](source-profile-class-get-names-method.html) method.

The [DatabaseName](source-profile-class-database-name-property.html) read-only property is the "database name" of the connection parameters. It can only be set by the constructor of **SourceProfile** , and it is the string used to reference registered database name information.

The [Server](source-profile-class-server-property.html) property may either be 1) a Domain Name System (DNS) host name, 2) a TCP/IP address in "dotted decimal" notation (such as "127.0.0.1"), or 3) the special value " ***LOCAL** ". In most cases ***LOCAL** is a synonym for the loopback TCP/IP address value "127.0.0.1".

>For DataGate Linear, ***LOCAL** allows ADO to negotiate the best of available connection protocols with SQL Server, including TCP/IP. When TCP/IP is disabled in SQL Server, this is the only way to connect using Datagate Linear. 

The [Label](source-profile-class-label-property.html) property specifies a particular database instance on the database provider for providers that allow more than one database instance, such as DataGate for Windows. For single-instance database providers, such as DataGate for iSeries, the **Label** property is ignored.

The [User](source-profile-class-user-property.html) property specifies the database provider-based user profile for authenticating access to the database. A special value, " ***PROMPT** ", may be used to require an interactive user to supply a user name and password (via dialog box) at the moment the database connection is initiated. Another special value, " ***DOMAIN** ", may be used to specify that the authentication of the currently signed on client-side user profile be used to authorize access to the server, if both the client and server machines are members of the same Windows NT domain.

The [Password](source-profile-class-password-property.html) property is a write-only property specifying the password for the user profile indicated by the **User** property. This property should only be set if the user profile has an associated password and only after setting the **User** property.

[PasswordType](source-profile-class-password-type-property.html) specifies how the **Password** property value is transmitted to and interpreted by the database provider.

The [Port](source-profile-class-port-property.html) property indicates the TCP/IP port number used to initiate connections to the database provider. This is the port that the provider is configured to "listen" to for incoming connections. By default DataGate servers listen to the Internet Assigned Numbers Authority-registered DataGate/Acceler8DB TCP port 5042.

The [PlatformAttribute](source-profile-class-platform-attribute-property.html) property is used to access SQL Server database providers and must be set to the value "* **SQLOLEB** " in this case. Otherwise, this property should be set to an empty string.

[PoolingTimeout](source-profile-class-pooling-timeout-property.html) specifies a time span in minutes that an open, unused database connection is held idle in the client pool before being closed. The value of **PoolingTimeout** must be set to zero if the connection should not be pooled.

The [Text](source-profile-class-text-property.html) property may hold application-specific comments about the database connection parameters. **Text** is not used to established database connections, but it is saved to the Windows registry by the **Register** method. For example, the value of **Text** may represent a longhand name for the **SourceProfile** .

The [Qualifier](source-profile-class-qualifier-property.html) property is reserved for future use, and should not be set by the application. 
## Requirements

**Namespace:** [ ASNA.DataGate.Providers](datagate-providers-namespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

## See Also

[SourceProfile Members](source-profile-members.html)
      <br />
[AdgConnection Class](adg-connection-class.html)
      <br />
[SourceProfile Property](adg-connection-class-source-profile-property.html)
      <br />
[AdgConnection Class Constructors](adg-connection-constructors-main.html)
      <br />
[ASNA DataGate Providers Namespace](datagate-providers-namespace.html)

