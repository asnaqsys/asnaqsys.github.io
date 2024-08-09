---
title: "IChannelSecurity interface    | QSYS API Reference Guide"
description: "Defines the contract for managing security in the ASNA DataGate client&#39;s communication channel. "
last_modified_at: 2024-08-09T16:18:40Z
---

Defines the contract for managing security in the ASNA DataGate client's communication channel.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Remarks
This interface provides properties to get the security details of the communication channel in the ASNA DataGate client. 
It includes properties to check if the channel is encrypted, signed, authenticated, 
the type of authentication used, the SSL certificate used (if any), the SPNEGO authentication ID (if any), 
and the SSL protocol used.

<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [AuthenticationType](/reference/datagate/datagate-client/authentication-type.html) | AuthenticationType | Gets the type of authentication used in the channel. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsAuthenticated | Gets a value indicating whether the channel is authenticated. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsEncrypted | Gets a value indicating whether the channel is encrypted. |
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | IsSigned | Gets a value indicating whether the channel is signed. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | SpnegoAuthID | Gets the SPNEGO authentication ID. This is only non-null when  isand thenegotiation succeeds. |
| [X509Certificate](https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.x509certificates.x509certificate?view=net-8.0) | SslCertificate | Gets the SSL certificate used in the channel, if any. |
| [SslProtocols](https://learn.microsoft.com/en-us/dotnet/api/system.security.authentication.sslprotocols?view=net-8.0) | SslProtocol | Gets the SSL protocol used in the channel. |
