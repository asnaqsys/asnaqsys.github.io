---
title: "NoDbNameException class"
description: "The NoDbNameException class is a custom exception class that is thrown when a database name is not provided where it is required. "
last_modified_at: 2024-08-09T17:25:07Z
---

The NoDbNameException class is a custom exception class that is thrown when a database name is not provided where it is required.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) --> [dgException](/reference/datagate/datagate-common/dg-exception.html)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [NoDbNameException()](no-db-name-exception-ctor.html#nodbnameexception) | Initializes a new instance of the NoDbNameException class.
| [NoDbNameException](no-db-name-exception-ctor.html#nodbnameexception-string)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the NoDbNameException class with a specified database name.
| [NoDbNameException](no-db-name-exception-ctor.html#nodbnameexception-string-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the NoDbNameException class with a specified database name and a reference to the inner exception that is the cause of this exception.

## Methods

| Signature | Description |
| --- | --- |
| [FormatMessage](no-db-name-exception-formatmessage.html#string-formatmessage-iformatprovider-provider-string-msg)([IFormatProvider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Formats the error message and the database name into a single string for logging or displaying to the user.

