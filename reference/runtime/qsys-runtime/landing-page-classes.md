---
title: "ASNA.QSys.Runtime Classes"
description: TOC Landing page for ASNA.QSys.Runtime Classes
---

## Remarks

The `ASNA.QSys.Runtime` assembly contains a collection of classes that are integral to the operation of the ASNA QSys system. These classes provide a range of functionalities, from handling arrays and built-in functions according to RPG semantics, to managing database connections and performing operations on data files.

The classes in this assembly are designed to work together to provide a comprehensive set of tools for interacting with the ASNA QSys system. They encapsulate complex operations into easy-to-use methods, making it easier for developers to build robust and efficient applications.

Here are some key points to remember when working with these classes:

- **Interoperability**: These classes are designed to work seamlessly with each other, providing a consistent and predictable interface for developers.
- **RPG Semantics**: Many of these classes provide methods that follow RPG programming patterns, making it easier for developers familiar with RPG to use them.
- **Exception Handling**: Several classes are dedicated to handling exceptions, providing detailed error information that can help with debugging and error handling.
- **Database Operations**: There are classes that manage database connections and perform operations on data files, abstracting the complexities of these tasks away from the developer.

Remember to refer to the individual class documentation for specific details about each class's behavior, usage, and special considerations.


| Type | Description |
| --- | --- |
| [ArrayMethods](/reference/runtime/qsys-runtime/array-methods.html) | Contains extension methods for handling Arrays according to RPG semantics. |
| [BadRecordNameException](/reference/runtime/qsys-runtime/bad-record-name-exception.html) | Exception thrown when a bad record name is encountered when constructing a WRF (Wings Record Format). |
| [BuiltInMethods](/reference/runtime/qsys-runtime/built-in-methods.html) | Contains extension methods for handling Built-in functions according to RPG semantics. |
| [BuiltInSupport](/reference/runtime/qsys-runtime/built-in-support.html) | Contains static methods to perform certain RPG Built In functions. |
| [Call](/reference/runtime/qsys-runtime/call.html) | Provides functionality to handle calling a program residing in an IBMi server. |
| [CallDSupport](/reference/runtime/qsys-runtime/call-d-support.html) | Provides methods to construct Omissible and Optional parameters for CALLD |
| [CannotCallException](/reference/runtime/qsys-runtime/cannot-call-exception.html) | Exception thrown when trying to use a multidimensional multi data structure in a CALL. |
| [CharacterMethods](/reference/runtime/qsys-runtime/character-methods.html) | Contains extension methods for Char (onechar/indicator) conversions. |
| [CharTypeAttribute](/reference/runtime/qsys-runtime/char-type-attribute.html) | A non-RPG class may stamp a string member with this attribute to be considered as a fixed-sized character field by a consumer RPG program. |
| [ConnectionNotOpenException](/reference/runtime/qsys-runtime/connection-not-open-exception.html) | File -filename- cannot be opened because a connection to database -database- has not been established exception. |
| [Convert](/reference/runtime/qsys-runtime/convert.html) | Converts a base data type to another base data type, using RPG type conversion rules. |
| [CurrentFormatException](/reference/runtime/qsys-runtime/current-format-exception.html) | -Format name- is not the current record format in the DataSet exception. |
| [DataAreaManager](/reference/runtime/qsys-runtime/data-area-manager.html) | Handles DataArea operations. |
| [DataAreaNotLockableException](/reference/runtime/qsys-runtime/data-area-not-lockable-exception.html) | DataArea Exception issued when a DataArea fails to Unlock. |
| [Database](/reference/runtime/qsys-runtime/database.html) | Handles connections to a Database. |
| [DatabaseCycleFile](/reference/runtime/qsys-runtime/database-cycle-file.html) | Database file that participates in the RPG program Cycle. When a Cycle file record is read from the Database,the file buffer values are not immediately copied into the program fields. The RPG cycle explicitly issues a LoadBuffer callat the proper time within the cycle to load the buffer into the program fields. |
| [DatabaseFile](/reference/runtime/qsys-runtime/database-file.html) | Represents a single format Database data file. It contains methods to handle all Input and Output operations on the file. |
| [DatabaseFileBase](/reference/runtime/qsys-runtime/database-file-base.html) | Common base class for Database data files, single format and multiformat. It contains methods common to both kinds. |
| [DatabaseFileExtensions](/reference/runtime/qsys-runtime/database-file-extensions.html) | Defines a collection of extension methods to aid in operating with the file's dataset. |
| [DataGateException](/reference/runtime/qsys-runtime/datagate-exception.html) | DataGate operation on file -filename- caused -datagate exception- exception. |
| [DataStructure](/reference/runtime/qsys-runtime/data-structure.html) | Contains the functionality to support the semantics of a RPG Data Structure with a memory layout. |
| [DateTimeMethods](/reference/runtime/qsys-runtime/date-time-methods.html) | Contains extension methods for handling Date/Time/Timestamp conversions. |
| [DateTimeOps](/reference/runtime/qsys-runtime/date-time-ops.html) | Defines operations with RPG semantics on System.DateTime values. |
| [DateTimeTypeAttribute](/reference/runtime/qsys-runtime/date-time-type-attribute.html) | A non-RPG class may stamp a System.DateTime member with this attribute to be considered as a fixed-sized date/time/timestamp field by a consumer RPG program. |
| [DecimalMethods](/reference/runtime/qsys-runtime/decimal-methods.html) | Contains extension methods for handling RPG operations for decimal numbers. |
| [DecimalOps](/reference/runtime/qsys-runtime/decimal-ops.html) | Provide fixed length decimal storage and operations. |
| [Dim\<T1, T2, T3\>](/reference/runtime/qsys-runtime/dim-3.html) | Defines a 3-digit dimension, from 100 to 999, to be used in the declaration of fixed-length array types. |
| [Dim\<T1, T2, T3, T4\>](/reference/runtime/qsys-runtime/dim-4.html) | Defines a 4-digit dimension, from 1000 to 9999, to be used in the declaration of fixed-length array types. |
| [Dim\<T1, T2, T3, T4, T5\>](/reference/runtime/qsys-runtime/dim-5.html) | Defines a 5-digit dimension, from 10000 to 99999, to be used in the declaration of fixed-length array types. |
| [DimArrayTypeAttribute](/reference/runtime/qsys-runtime/dim-array-type-attribute.html) | A non-RPG class may stamp an array member with this attribute to be considered as a fixed-sized array by a consumer RPG program. |
| [DimensionAttribute](/reference/runtime/qsys-runtime/dimension-attribute.html) | A non-RPG class, property or field may be stamped with this attribute to indicate a consumer RPG program to consider it as an array with the specified dimension. |
| [DSArrayField](/reference/runtime/qsys-runtime/ds-array-field.html) | Describes a Data Structure field that is an array. |
| [DSCallParm](/reference/runtime/qsys-runtime/ds-call-parm.html) | Describes a Data Structure (either single or Multi) as a parameter for a CALL to an IBMi program. |
| [DSDataArea](/reference/runtime/qsys-runtime/ds-data-area.html) | Describes and manages the use of a Data Structure as a Data Area value. |
| [DSField](/reference/runtime/qsys-runtime/ds-field.html) | Describes a field in a Data Structure. |
| [DSLengthAttribute](/reference/runtime/qsys-runtime/ds-length-attribute.html) | A non-RPG class may be stamped with this attribute to indicate a consumer RPG program to consider it as a Data Structure with the specified length. |
| [DSParameter](/reference/runtime/qsys-runtime/ds-parameter.html) | Describes the datastructure parameters sent into an IBMi program call. |
| [DuplicateFieldException](/reference/runtime/qsys-runtime/duplicate-field-exception.html) | Field -field- was specified more than once in -specification- exception. |
| [DynamicCaller](/reference/runtime/qsys-runtime/dynamic-caller.html) | Support for CALLD as a dynamic call. |
| [DynamicReferenceAttribute](/reference/runtime/qsys-runtime/dynamic-reference-attribute.html) | Declares an assembly to be used as a dynamic reference, which will be queried at runtime to find CALLD targets. |
| [EditCode](/reference/runtime/qsys-runtime/edit-code.html) | Provides methods for applying and manipulating edit codes, which define output formatting patterns for business numeric data. |
| [EditWord](/reference/runtime/qsys-runtime/edit-word.html) | Provides methods for applying edit word parameters to numeric values, including formatting and manipulating the output string based on specified patterns. |
| [EndOperationException](/reference/runtime/qsys-runtime/end-operation-exception.html) | Defines the core behavior of the the base class that is thrown to unwind the program call stack. |
| [EndRequestException](/reference/runtime/qsys-runtime/end-request-exception.html) | The exception that is thrown for an EndRequest operation. |
| [FieldNotFoundException](/reference/runtime/qsys-runtime/field-not-found-exception.html) | -Field name- was not found in format -record format name- of -filename-. |
| [FileAlreadyOpenException](/reference/runtime/qsys-runtime/file-already-open-exception.html) | File -filename- is already open exception. |
| [FileBase](/reference/runtime/qsys-runtime/file-base.html) | Defines common functionality for files (Database, Printfile, Workstation) |
| [FileNotOpenException](/reference/runtime/qsys-runtime/file-not-open-exception.html) | File -filename- is not open exception. |
| [FixedArrayMethods](/reference/runtime/qsys-runtime/fixed-array-methods.html) | Contains extension methods for handling FixedArrays according to RPG semantics. |
| [FixedDateMethods](/reference/runtime/qsys-runtime/fixed-date-methods.html) | Contains extension methods for handling RPG operations for FixedDate values. |
| [FixedDecimalMethods](/reference/runtime/qsys-runtime/fixed-decimal-methods.html) | Contains extension methods for handling RPG operations for FixedDecimal values. |
| [FixedDecimalTypeAttribute](/reference/runtime/qsys-runtime/fixed-decimal-type-attribute.html) | A non-RPG class may stamp a decimal member with this attribute to be considered as a fixed-sized decimal field by a consumer RPG program. |
| [FixedStringComparer](/reference/runtime/qsys-runtime/fixed-string-comparer.html) | Provides a comparer for fixed-length strings, allowing for consistent comparison of strings with fixed lengths. |
| [FixedStringMethods](/reference/runtime/qsys-runtime/fixed-string-methods.html) | Contains extension methods for handling RPG operations for FixedString values. |
| [FixedTimeMethods](/reference/runtime/qsys-runtime/fixed-time-methods.html) | Contains extension methods for handling RPG operations for FixedTime values. |
| [FixedTimeStampMethods](/reference/runtime/qsys-runtime/fixed-time-stamp-methods.html) | Contains extension methods for handling RPG operations for FixedTimestamp values. |
| [FloatMethods](/reference/runtime/qsys-runtime/float-methods.html) | Contains extension methods for handling RPG operations for floating point numbers. |
| [GetObject](/reference/runtime/qsys-runtime/get-object.html) | Class that contains methods to construct certain RPG objects. |
| [GlobalFlagProperty](/reference/runtime/qsys-runtime/global-flag-property.html) | GlobalFlagProperty class. |
| [GlobalFlags](/reference/runtime/qsys-runtime/global-flags.html) | Holds the application flags that correspond to RPG's %ERROR, not %FOUND, %EOF, and %EQUAL. These flags are local per thread. |
| [HexMethods](/reference/runtime/qsys-runtime/hex-methods.html) | Contains extension methods for handling RPG conversions between character strings and their hexadecimal representation. |
| [InconsistentOpenAttributesException](/reference/runtime/qsys-runtime/inconsistent-open-attributes-exception.html) | The following Open attributes were inconsistent with the Query File: -attributes- exception. |
| [IndicatorMethods](/reference/runtime/qsys-runtime/indicator-methods.html) | Contains extension methods for handling RPG operations for Indicator values. |
| [IndicatorTypeAttribute](/reference/runtime/qsys-runtime/indicator-type-attribute.html) | A non-RPG class may stamp a char member with this attribute to be considered as an indicator field by a consumer RPG program. |
| [InfSrException](/reference/runtime/qsys-runtime/inf-sr-exception.html) | Exception that can be thrown from InfSr to return or report an error condition. |
| [IntDigitSize](/reference/runtime/qsys-runtime/int-digit-size.html) | Constants for the size of integers, in digits. |
| [IntegerMethods](/reference/runtime/qsys-runtime/integer-methods.html) | Contains extension methods for handling RPG operations and conversions for Integer (2, 4, and 8-byte long) values. |
| [InvalidCodePageForVirtualTerminalException](/reference/runtime/qsys-runtime/invalid-code-page-for-virtual-terminal-exception.html) | Code page 0 is not valid when starting interactive job without server support. |
| [InvalidDataAreaTypeException](/reference/runtime/qsys-runtime/invalid-data-area-type-exception.html) | DataArea Exception issued when the DataArea type is not valid. |
| [InvalidDSFieldsException](/reference/runtime/qsys-runtime/invalid-ds-fields-exception.html) | Exception that is thrown when a data structure contains a field of a not supported type. |
| [InvalidFileOperationException](/reference/runtime/qsys-runtime/invalid-file-operation-exception.html) | Invalid Operation: -operation- on file: -filename- exception. |
| [InvalidInputAttemptException](/reference/runtime/qsys-runtime/invalid-input-attempt-exception.html) | Invalid input attempt on format : -record format name- on file: -filename- exception. |
| [InvalidKeySpecException](/reference/runtime/qsys-runtime/invalid-key-spec-exception.html) | Key part -name- is invalid exception. |
| [InvalidRecordFieldsException](/reference/runtime/qsys-runtime/invalid-record-fields-exception.html) | Record Format contains fields with types not compatible for this operation exception. |
| [InvalidRRNException](/reference/runtime/qsys-runtime/invalid-rrn-exception.html) | Invalid RRN Value: -rrn- on file: -filename- exception. |
| [InvalidSourceLengthException](/reference/runtime/qsys-runtime/invalid-source-length-exception.html) | Length of source is less than length of data structure exception. |
| [InvalidVirtualTerminalException](/reference/runtime/qsys-runtime/invalid-virtual-terminal-exception.html) | Virtual Terminal value -mode- is not supported exception. |
| [JobShutDownException](/reference/runtime/qsys-runtime/job-shut-down-exception.html) | The exception that is thrown to end a job. |
| [Len\<T1, T2, T3\>](/reference/runtime/qsys-runtime/len-3.html) | Defines a 3-digit length, from 100 to 999, to be used in the declaration of fixed-length types. |
| [Len\<T1, T2, T3, T4\>](/reference/runtime/qsys-runtime/len-4.html) | Defines a 4-digit length, from 1000 to 9999, to be used in the declaration of fixed-length types. |
| [Len\<T1, T2, T3, T4, T5\>](/reference/runtime/qsys-runtime/len-5.html) | Defines a 5-digit length, from 10000 to 99999, to be used in the declaration of fixed-length types. |
| [LibraryListException](/reference/runtime/qsys-runtime/library-list-exception.html) | There was an error of type -error- while trying to modify the library list. |
| [LocalScopeDS](/reference/runtime/qsys-runtime/local-scope-ds.html) | Base class that contains functionality to support locally scoped data structures. |
| [LocalScopeMultiDS\<T\>](/reference/runtime/qsys-runtime/local-scope-multi-ds-1.html) | Contains functionality to support locally scoped multiple occurrence data structures. A LocalScopeMultiDS object contains an array of LocalScopeDS objects. |
| [MemUnit](/reference/runtime/qsys-runtime/mem-unit.html) | Defines methods to handle RPG MOVE semantics. |
| [MessageFileReader](/reference/runtime/qsys-runtime/message-file-reader.html) | Provides the contents of a message file. |
| [MissingFormatException](/reference/runtime/qsys-runtime/missing-format-exception.html) | The program was compiled to use format -format-, but it was not found in file -filename-. |
| [MODSRankAttribute](/reference/runtime/qsys-runtime/mods-rank-attribute.html) | A non-RPG class may be stamped with this attribute to indicate a consumer RPG program to consider it as a Multiple Occurrence Data Structure with the rankindicated in this attribute. |
| [MultiDataStructure](/reference/runtime/qsys-runtime/multi-data-structure.html) | Contains functionality to support multiple occurrence data structures. |
| [MultiFormatDatabaseFile](/reference/runtime/qsys-runtime/multi-format-database-file.html) | Represents a multiformat Database data file. It contains methods to handle all Input and Output operations on the file.  |
| [NetworkBlockingOutputException](/reference/runtime/qsys-runtime/network-blocking-output-exception.html) | Network Blocking is not allowed for *OUTPUT if CacheWrites is *NO on file -filename-. |
| [NetworkBlockingUpdateException](/reference/runtime/qsys-runtime/network-blocking-update-exception.html) | Network Blocking is not allowed for -filename- because it is opened for *UPDATE. |
| [NonexistentDataAreaException](/reference/runtime/qsys-runtime/nonexistent-data-area-exception.html) | DataArea Exception issued when requesting a non-existing DataArea. |
| [NoPassOmit\<T\>](/reference/runtime/qsys-runtime/no-pass-omit-1.html) | Encapsulates a *OMIT wnd *NOPASS parameter. |
| [NullCapableFieldAttribute](/reference/runtime/qsys-runtime/null-capable-field-attribute.html) | A non-RPG class may stamp a property or field member with this attribute to be considered as a null capable field by a consumer RPG program. |
| [Omissible\<T\>](/reference/runtime/qsys-runtime/omissible-1.html) | Encapsulates a *OMIT parameter. |
| [OpenSimpleQueryFileException](/reference/runtime/qsys-runtime/open-simple-query-file-exception.html) | An invalid QryKeyFlds string format has been entered. |
| [Optional\<T\>](/reference/runtime/qsys-runtime/optional-1.html) | Encapsulates a *NOPASS parameter. |
| [OSExecute](/reference/runtime/qsys-runtime/os-execute.html) | This class contains methods to start an external process. |
| [Parameter](/reference/runtime/qsys-runtime/parameter.html) | Describes a parameter sent into an IBMi program call. |
| [ParameterOptions\<T\>](/reference/runtime/qsys-runtime/parameter-options-1.html) | Represents the base functionality of the special RPG parameters *OMIT and *NOPASS |
| [PrintFile](/reference/runtime/qsys-runtime/print-file.html) | Represents a Database print file. It contains methods to handle all Output operations on the file. |
| [PrintFileBase](/reference/runtime/qsys-runtime/print-file-base.html) | Base class for Database print files. Contains the print file setup information and some output operations. |
| [ProcedureSupport](/reference/runtime/qsys-runtime/procedure-support.html) | Provides static methods to support finding a class used in dynamic calls (RPG's CallD). |
| [ProgramEntryAttribute](/reference/runtime/qsys-runtime/program-entry-attribute.html) | A non-RPG class may use this attribute to indicate which method in it corresponds to RPG's *ENTRY. |
| [ProgramIndicatorsAttribute](/reference/runtime/qsys-runtime/program-indicators-attribute.html) | For a non-RPG class to be used as the base class of an RPG class (AVR or Encore), this attribute indicates the name of the *INLR, *IN, and *INRT indicators. |
| [QueryFileNotOpenException](/reference/runtime/qsys-runtime/query-file-not-open-exception.html) | Query File -filename- is not open exception. |
| [QueryKeyFieldsLengthException](/reference/runtime/qsys-runtime/query-key-fields-length-exception.html) | Expecting a string in the format: 'VALUE1 ORDER1 ... VALUEn ORDERn'. |
| [QueryKeyFieldsUsageException](/reference/runtime/qsys-runtime/query-key-fields-usage-exception.html) | Expecting: '*ASCEND', '*DESCEND' or '*ABSVAL' but found -usage- exception. |
| [RecordAlreadyExistsInSubfileException](/reference/runtime/qsys-runtime/record-already-exists-in-subfile-exception.html) | Record already exists in subfile: -subfile record name- exception. |
| [RecordAsBuffer](/reference/runtime/qsys-runtime/record-as-buffer.html) | Defines operations to move data between a file record, a row in a dataset, and a string buffer. |
| [RecordFormatAttribute](/reference/runtime/qsys-runtime/record-format-attribute.html) | A non-RPG class may stamp a field with this attribute to be considered as a record format by a consumer RPG program. |
| [RequiredOpenConnectionException](/reference/runtime/qsys-runtime/required-open-connection-exception.html) | Operation not available on un-opened Database -database name- exception. |
| [Return](/reference/runtime/qsys-runtime/return.html) | RETURN operation is implemented as a long jump using the exception catching C# mechanism. |
| [RowAddedEventArgs](/reference/runtime/qsys-runtime/row-added-event-args.html) | Holds information that the RowAddedEvent requires. |
| [RowAddedEventHandler](/reference/runtime/qsys-runtime/row-added-event-handler.html) | Event raised when a row was added to a subfile. |
| [RowInsertedEventArgs](/reference/runtime/qsys-runtime/row-inserted-event-args.html) | Holds information that the RowInsertedEvent requires. |
| [RowInsertedEventHandler](/reference/runtime/qsys-runtime/row-inserted-event-handler.html) | Event raised when a row was inserted in a subfile. |
| [RpgTypeExtensions](/reference/runtime/qsys-runtime/rpg-type-extensions.html) | Provides extension methods for RPG types, including methods for moving and manipulating fixed-length strings and decimal numbers. |
| [RuntimeException](/reference/runtime/qsys-runtime/runtime-exception.html) | Base class for all ASNA QSys Runtime generated exceptions. |
| [StringMethods](/reference/runtime/qsys-runtime/string-methods.html) | Contains extension methods for handling RPG operations and conversions for string values. |
| [StringOps](/reference/runtime/qsys-runtime/string-ops.html) | Provide fixed length character string storage and operations. |
| [Table\<T\>](/reference/runtime/qsys-runtime/table-1.html) | Supports RPG's table type by encapsulating an array and providing it with an implied index through the use of the CurrentElement property. |
| [TableMethods](/reference/runtime/qsys-runtime/table-methods.html) | Contains extension methods for handling Table RPG semantics. |
| [TooManySubfileRecordsException](/reference/runtime/qsys-runtime/too-many-subfile-records-exception.html) | Record -rrn- does not fit in subfile -subfile name- on file -filename- exception. |
| [TransactionNotStartedException](/reference/runtime/qsys-runtime/transaction-not-started-exception.html) | The transaction has not been started exception. |
| [TypeDigestor](/reference/runtime/qsys-runtime/type-digestor.html) | Contains methods that aid in the parsing of the generic type arguments of fixed-sized types. |
| [UnlockedDataAreaException](/reference/runtime/qsys-runtime/unlocked-data-area-exception.html) | DataArea Exception issued when attempting to unlock a DataArea that is not locked. |
| [UpdateWithoutAPriorInputOperationException](/reference/runtime/qsys-runtime/update-without-a-prior-input-operation-exception.html) | Update subfile record without a prior input operation. |
| [VaryingLengthFieldAttribute](/reference/runtime/qsys-runtime/varying-length-field-attribute.html) | A non-RPG class may stamp a property or field member with this attribute to be considered as a varying length field by a consumer RPG program. |
| [WingsRecordFormat](/reference/runtime/qsys-runtime/wings-record-format.html) | Contains functionality to construct the WRF, an XML representation of a file. |
| [WorkstationDataSet](/reference/runtime/qsys-runtime/workstation-data-set.html) | Represents the dataset of a workstation file. |
| [WorkstationFile](/reference/runtime/qsys-runtime/workstation-file.html) | Represents a Workstation file. It contains methods to handle all Input and Output operations on the file. |
| [WorkstationFileBase](/reference/runtime/qsys-runtime/workstation-file-base.html) | Base class for Workstation files. It contains functionality to support common input/output operations on Workstation files. |
