---
title: "SslOptions enum               | QSYS API Reference Guide"
description: "Specifies the SSL options for a connection. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the SSL options for a connection.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| AuthDns | Requires that the server certificate's CN matches the server's FQDN. | 8 |
| AuthLocal | Requires that the server certificate is installed in the user's local certificate store. | 16 |
| AuthName | Requires that the server certificate's CN matches a given string. | 4 |
| AuthPrompt | For desktops, prompts for action if the certificate is invalid. | 32 |
| AuthRevoked | Specifies that the certificate chain cannot include explicitly revoked certificates. | 256 |
| CASigned | Requires that the server certificate is chained to a trusted certificate authority. | 64 |
| NoClearText | Throws an exception if the server permits insecure connections. | 128 |
| None | Specifies a clear text connection. | 0 |
| Request | Requests but doesn't require an encrypted connection. | 1 |
| Require | Requires an encrypted connection. Throws an exception if an encrypted connection is unavailable. | 2 |
