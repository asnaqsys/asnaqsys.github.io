---
title: "AuthenticationType enum       | QSYS API Reference Guide"
description: "Specifies the type of authentication used in the ASNA DataGate client. "
last_modified_at: 2024-08-09T17:25:07Z
---

Specifies the type of authentication used in the ASNA DataGate client.

**Namespace:** ASNA.DataGate.Client
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Remarks
This enumeration is used to specify the type of authentication used in the ASNA DataGate client. 
It includes options for no authentication, user/password credential authentication, 
*DOMAIN v1 NTLM token protocol, AuthenticatedStream authentication of unknown type, 
SslServer certificate accepted by client, client/server certificates accepted, 
and Negotiate SSPI: NTLM, Kerberos, etc.

<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| None | Represents no authentication. | 0 |
| SecurityToken | Represents *DOMAIN v1 NTLM token protocol. | 2 |
| SpnegoSspi | Represents Negotiate SSPI: NTLM, Kerberos, etc. | 6 |
| SslMutual | Represents client/server certificates accepted. | 5 |
| SslServer | Represents SslServer certificate accepted by client. | 4 |
| Unknown | Represents AuthenticatedStream authentication of unknown type. | 3 |
| UserPassword | Represents user/password credential authentication. | 1 |
