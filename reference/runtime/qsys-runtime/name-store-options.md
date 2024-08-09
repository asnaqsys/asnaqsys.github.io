---
title: "NameStoreOptions enum         | QSYS API Reference Guide"
description: "Defines flags that tell the name store which name sources to use. "
last_modified_at: 2024-08-09T17:25:29Z
---

Defines flags that tell the name store which name sources to use.

**Namespace:** ASNA.QSys.Runtime
**Assembly:** ASNA.QSys.Runtime.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| none | No Name Store. | 0 |
| UseCommandLineArgs | Use command-line arguments as to pass the Name Store. | 8 |
| UseEnvironmentalVars | Use OS Environmental variables to resolve the Name Store. | 4 |
| UseJsonDefaultPath | Use JSON default path as the Name Store. | 1 |
| UseSecrets | Use secrets as the Name Store. | 2 |
| WithCommonDefaults | With Common defaults as the Name Store. | 15 |
| WithSecretsJsonDefault | With Secrets JSON default as the Name Store. | 3 |
