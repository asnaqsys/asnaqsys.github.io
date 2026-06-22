---
title: "IPrintProperties interface"
description: "Provides an interface for managing print properties. "
last_modified_at: 2024-08-09T17:25:07Z
---

Provides an interface for managing print properties.

**Namespace:** ASNA.DataGate.Providers
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>
## Thread Safety

In DG implementations of **IPrintProperties** , instance members are not guaranteed to be thread safe.


## Methods

| Signature | Description |
| --- | --- |
| [GetBoundType](i-print-properties-getboundtype.html#type-getboundtype-string-fieldname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the type information for a print control bound to a specific field.
| [GetTypedObject](i-print-properties-gettypedobject.html#object-gettypedobject-string-fieldname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets a typed object associated with a specific field.
| [GetValue](i-print-properties-getvalue.html#object-getvalue-string-fieldname-string-propname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Gets the value of a specific property for a given field.
| [SetValue](i-print-properties-setvalue.html#void-setvalue-string-fieldname-string-propname-object-val)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)) | Sets the value of a specific property for a given field.

