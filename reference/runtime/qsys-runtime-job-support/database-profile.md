---
title: "DatabaseProfile class         | QSYS API Reference Guide"
description: "Represents the configuration settings for a database connection within a batch entry. This class encapsulates all necessary details required to establ"
last_modified_at: 2024-08-08T21:41:46Z
---

Represents the configuration settings for a database connection within a batch entry.
This class encapsulates all necessary details required to establish a connection
to the database, including server information, authentication credentials, and
other connection-specific settings.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [CredentialType](/reference/datagate/datagate-providers/credential-type.html) | Credential | Gets or sets the type of credentials used for database authentication. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Label | Gets or sets the label or identifier for the database profile. |
| [List\<String\>](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1) | LibraryList | Gets or sets the list of libraries to be used with the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Password | Gets or sets the password for database authentication. |
| [PasswordType](/reference/datagate/datagate-common/password-type.html) | PasswordType | Gets or sets the type of password used for database authentication. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | PlatformAttribute | Gets or sets the platform-specific attribute for the database connection. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | Port | Gets or sets the port number for the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Server | Gets or sets the server name or IP address for the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | ServicePrincipalName | Gets or sets the Service Principal Name (SPN) for the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SslCertificateName | Gets or sets the name of the SSL certificate for the database connection. |
| [SslOptions](/reference/datagate/datagate-common/ssl-options.html) | SslOptions | Gets or sets the SSL options for the database connection. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | User | Gets or sets the username for database authentication. |
