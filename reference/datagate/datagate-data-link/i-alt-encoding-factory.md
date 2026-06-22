---
title: "IAltEncodingFactory interface"
description: "Defines methods for creating instances of AltEncoding and getting information about the encodings supported by the factory. "
last_modified_at: 2024-08-09T17:25:07Z
---

Defines methods for creating instances of AltEncoding and getting information about the encodings supported by the factory.

**Namespace:** ASNA.DataGate.DataLink.Text
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Extends:** doesn't extend any other interfaces.
<br>
<br>

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IEnumerable\<AltEncodingInfo\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.ienumerable-1?view=net-8.0) | Encodings | This method should return an array of AltEncodingInfo objectsrepresenting all encodings supported by the factory.  Only includean AltEncoding object in the returned array if that object's Nameproperty value can be passed to GetEncoding to return a validAltEncoding object. |

## Methods

| Signature | Description |
| --- | --- |
| [GetEncoding](i-alt-encoding-factory-getencoding.html#altencoding-getencoding-string-name)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Generally, this method should only return an instance ofAltEncoding if the encoding is represented by one of theAltEncodingInfo objects returned by the Encodings property.This method should throw ArgumentException if the name given is notsupported by the factory.

