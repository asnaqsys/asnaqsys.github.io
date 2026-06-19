---
title: "IAdgObject interface.GrantAuthority Method"
description: "Grants authority to a user or group for the ADG object."
---

## Definition

**Namespace:** ASNA.DataGate.Client  
**Assembly:** ASNA.QSys.DataGate.Client.dll

Grants authority to a user or group for the ADG object.

<a id="void-grantauthority-string-user-authoritytypes-authority"></a>
## void GrantAuthority(string user, AuthorityTypes authority)

Grants authority to a user or group for the ADG object.

#### Remarks
This method is used to grant a specific authority to a user or group for the ADG object. The user parameter specifies the user or group to grant the authority to. The authority parameter specifies the authority to grant, which can be read, write, execute, or other types of authority.

```cs
void GrantAuthority(string user, AuthorityTypes authority)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | user | The user or group to grant authority to.
| [AuthorityTypes](/reference/datagate/datagate-common/authority-types.html) | authority | The authority type to grant.

## See Also
- [IAdgObject interface class](i-adg-object.html)
