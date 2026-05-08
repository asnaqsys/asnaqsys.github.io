---
title: "ASNA.DataGate.Common Classes"
description: TOC Landing page for ASNA.DataGate.Common Classes
---

## Remarks

The following are the Common classes provided by **ASNA DataGate Common** namespace.

| Type | Description |
| --- | --- |
| [AdgTrace](/reference/datagate/datagate-common/adg-trace.html) | Provides methods and properties for tracing and logging in the application.This class cannot be inherited. |
| [ClrStringHelpers](/reference/datagate/datagate-common/clr-string-helpers.html) | This class offers some abstractions for .NET string functions peculiarto the net core platform (and suggested by CA). |
| [DecNumZPRep](/reference/datagate/datagate-common/dec-num-zp-rep.html) | DecNumZPRep provides methods for interpreting the Acceler8DB "ZPREP"code for packed and zoned decimal data representation, therebydescribing the format of these data representations. |
| [dgException](/reference/datagate/datagate-common/dg-exception.html) | The dgException class is a custom exception class that extends the base Exception class.It provides additional functionality for handling errors specific to the application. |
| [DgNegotiateException](/reference/datagate/datagate-common/dg-negotiate-exception.html) | Specialized Exception dealing with DataGate protocol negotiation. |
| [FieldType](/reference/datagate/datagate-common/field-type.html) | Represents the type of a field in a data structure. |
| [IndicatorExpression](/reference/datagate/datagate-common/indicator-expression.html) | A condition is an ANDed grouping of two through nine indicators thatmust all be in effect (set off if N or ! is specified; set on if Nor ! is not specified) before the field or keyword is selected. You canspecify a maximum of nine indicators for each condition and nineconditions for each field or keyword. You can also specify severalconditions for a field or keyword so that if any one of them issatisfied, the field or the keyword is selected. This is called an ORrelationshipexample: 1 & 2 & !3 | 44 & 55 | 60 |
| [InputStreamAggregator](/reference/datagate/datagate-common/input-stream-aggregator.html) | Queue multiple, fixed-length, read-only streams into one stream. |
| [InvariantCultureTypeConverter](/reference/datagate/datagate-common/invariant-culture-type-converter.html) | Provides a type converter to convert object types to and from string representations, using the invariant culture. |
| [NoDbNameException](/reference/datagate/datagate-common/no-db-name-exception.html) | The NoDbNameException class is a custom exception class that is thrown when a database name is not provided where it is required. |
| [TraceSinkSectionHandler](/reference/datagate/datagate-common/trace-sink-section-handler.html) | Handles the configuration section for trace sinks in the application.Implements the  interface. |
| [XmlElementConverter](/reference/datagate/datagate-common/xml-element-converter.html) | Provides methods for converting between XmlElement objects and their string, boolean, and child element representations. |
