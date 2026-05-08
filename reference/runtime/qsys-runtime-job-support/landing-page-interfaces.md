---
title: "ASNA.QSys.Runtime.JobSupport Interfaces"
description: TOC Landing page for ASNA.QSys.Runtime.JobSupport Interfaces
---

## Remarks

The `ASNA.QSys.Runtime.JobSupport` namespace contains interfaces that are used throughout the ASNA QSys system. These interfaces define a contract of operations, properties, and events that classes can implement, providing a way to achieve polymorphism and increase the flexibility and interoperability of the system.

These interfaces cover a wide range of functionalities, from defining functionality to perform conversions between EBCDIC and Unicode, to adding messages to a log, to creating an object that implements the IConverter interface, among others.

Here are some key points to remember when working with these interfaces:

- **Polymorphism**: By defining a common interface, different classes can implement the same interface in different ways. This allows you to write code that can work with objects of any class that implements a particular interface.
- **Flexibility**: Interfaces allow you to create systems that are flexible and easily extensible. You can add new classes that implement these interfaces without having to change the existing code that uses the interfaces.
- **Interoperability**: These interfaces provide a consistent way to interact with different parts of the ASNA QSys system, increasing the interoperability of your code.

Remember to refer to the individual interface documentation for specific details about each interface's contract and usage.

| Type | Description |
| --- | --- |
| [ICodePageConverter](/reference/runtime/qsys-runtime-job-support/i-code-page-converter.html) | Implement this interface to add your own CodePage conversion if Wings or the 5250 emulator don't already know it. |
| [IConverter](/reference/runtime/qsys-runtime-job-support/i-converter.html) | Defines functionality to perform conversions between EBCDIC and Unicode. |
| [IConverterFactory](/reference/runtime/qsys-runtime-job-support/i-converter-factory.html) | Defines the functionality to create an object that implements the IConverter interface. |
| [IJobLogger](/reference/runtime/qsys-runtime-job-support/i-job-logger.html) | Defines a generalized way to to add messages to a log. |
| [IJobLoggerFactory](/reference/runtime/qsys-runtime-job-support/i-job-logger-factory.html) | Defines a generalized way to to get hold of a message logger. |
