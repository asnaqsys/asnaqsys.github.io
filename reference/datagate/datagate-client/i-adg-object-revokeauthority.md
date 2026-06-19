---
title: "IAdgObject interface.RevokeAuthority Method"
description: "Revokes a specific authority from a user for the ADG object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Revokes a specific authority from a user for the ADG object.

<a id="void-revokeauthority-string-username-authoritytypes-authoritytype"></a>
## void RevokeAuthority(string userName, AuthorityTypes authorityType)

Revokes a specific authority from a user for the ADG object.

#### Remarks
This method is used to revoke a specific authority from a user for the ADG object. The userName parameter specifies the user to revoke the authority from. The authorityType parameter specifies the type of authority to revoke, which can be read, write, execute, or other types of authority.

```cs
void RevokeAuthority(string userName, AuthorityTypes authorityType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | userName | The user to revoke the authority from.
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | authorityType | The type of authority to revoke.

## See Also
- [IAdgObject interface class](i-adg-object.html)
