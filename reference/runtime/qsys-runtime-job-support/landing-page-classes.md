---
title: "ASNA.QSys.Runtime.JobSupport Classes"
description: TOC Landing page for ASNA.QSys.Runtime.JobSupport Classes
---

## Remarks

The `ASNA.QSys.Runtime.JobSupport` namespace contains classes that provide support for managing jobs, programs, and service programs in an ASNA environment. These classes provide the core functionality for organizing and controlling the execution of programs, handling exceptions, managing message queues, and interacting with the integrated file system, among other tasks.

This namespace is crucial for developers working with ASNA, as it provides the necessary tools for managing the lifecycle of jobs and handling the complexities of program execution. Each class in this namespace is documented in detail in the subsequent pages, providing developers with the information they need to effectively use these tools in their applications.

| Type | Description |
| --- | --- |
| [ActivationGroup](/reference/runtime/qsys-runtime-job-support/activation-group.html) | Provides the facilities to organize the instances of programs and service programs into related groups. |
| [ActivationGroupAttribute](/reference/runtime/qsys-runtime-job-support/activation-group-attribute.html) | Defines the Activation Group Attribute used to mark a program or service program class. |
| [ActivationGroupCallException](/reference/runtime/qsys-runtime-job-support/activation-group-call-exception.html) | The exception that is thrown when an program is to be activated in the caller's activation but the caller activation group could not be found. |
| [ActivationGroupCreateException](/reference/runtime/qsys-runtime-job-support/activation-group-create-exception.html) | The exception that is thrown when an activation could not be found or created. |
| [ActivationGroupDisposeException](/reference/runtime/qsys-runtime-job-support/activation-group-dispose-exception.html) | The exception that is thrown when an program has a null activation group at dispose time. |
| [ActivationGroupInvalidCreatorException](/reference/runtime/qsys-runtime-job-support/activation-group-invalid-creator-exception.html) | The exception that is thrown when an activation group's dynamic creator is being overwritten. |
| [ActivationGroupInvalidProgramException](/reference/runtime/qsys-runtime-job-support/activation-group-invalid-program-exception.html) | The exception that is thrown when an activation could not be created because the program is invalid. |
| [ActivationGroupProgramConstructorException](/reference/runtime/qsys-runtime-job-support/activation-group-program-constructor-exception.html) | The exception that is thrown when a program could not be constructed. |
| [ActivationManager](/reference/runtime/qsys-runtime-job-support/activation-manager.html) | Provides the facilities to manage the instances of programs and service programs. |
| [AssemblyListProfilesSetting](/reference/runtime/qsys-runtime-job-support/assembly-list-profiles-setting.html) | Gets or sets a dictionary of named assembly lists.  |
| [BatchEntry](/reference/runtime/qsys-runtime-job-support/batch-entry.html) | Represents a single entry in a batch processing system. This class providesthe necessary properties and methods to manage the entry's data and state. |
| [BatchJob](/reference/runtime/qsys-runtime-job-support/batch-job.html) | Defines the core behavior of a batch job. |
| [BatchJobProfile](/reference/runtime/qsys-runtime-job-support/batch-job-profile.html) | Provides the facilities to configure and launch a batch job. |
| [BatchOptions](/reference/runtime/qsys-runtime-job-support/batch-options.html) | Defines the options for a batch job. |
| [BatchPoint](/reference/runtime/qsys-runtime-job-support/batch-point.html) | Defines the location and time or a batch job. |
| [CallerActivationGroupAttribute](/reference/runtime/qsys-runtime-job-support/caller-activation-group-attribute.html) | Defines the special Attribute used to mark a program or service program class for it to be activated in the caller's Activation Group. |
| [CallHostSpecs](/reference/runtime/qsys-runtime-job-support/call-host-specs.html) | Packages the specification of a remote program call command and its parameters. |
| [CLProgram](/reference/runtime/qsys-runtime-job-support/cl-program.html) | Defines the core behavior of programs migrated from CL program . |
| [CodePage](/reference/runtime/qsys-runtime-job-support/code-page.html) | Provides facilities to probe an IBM i file's code page. |
| [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html) | Defines the core behavior of programs and service programs. |
| [DatabaseProfile](/reference/runtime/qsys-runtime-job-support/database-profile.html) | Represents the configuration settings for a database connection within a batch entry.This class encapsulates all necessary details required to establish a connectionto the database, including server information, authentication credentials, andother connection-specific settings. |
| [DBCharParm](/reference/runtime/qsys-runtime-job-support/db-char-parm.html) | Represents a parameter for a Character type. |
| [DBDateTimeParm](/reference/runtime/qsys-runtime-job-support/db-date-time-parm.html) | Represents a parameter for a date-time type. |
| [DBDecimalParm](/reference/runtime/qsys-runtime-job-support/db-decimal-parm.html) | Represents a parameter for a decimal type. |
| [DBIntegerParm](/reference/runtime/qsys-runtime-job-support/db-integer-parm.html) | Represents a parameter for an integer type. |
| [DBParm](/reference/runtime/qsys-runtime-job-support/db-parm.html) | Represents a SQL Parameter (used as base to specific parameter type) |
| [DBScaledParm](/reference/runtime/qsys-runtime-job-support/db-scaled-parm.html) | Represents a parameter for a Scalar type. |
| [DBStrParm](/reference/runtime/qsys-runtime-job-support/db-str-parm.html) | Represents a String SQL Parameter. |
| [DocumentLibraryObject](/reference/runtime/qsys-runtime-job-support/document-library-object.html) | Provides functionality to manipulate Document Library Objects (DLO). |
| [DynamicDisplayFile](/reference/runtime/qsys-runtime-job-support/dynamic-display-file.html) | Provides the facilities to use a display file without prior infrastructure. |
| [ExecuteStateException](/reference/runtime/qsys-runtime-job-support/execute-state-exception.html) | The exception that is thrown when a job is artificially being set to a state of 'Running'. |
| [FileOverrideOptionMismatchException](/reference/runtime/qsys-runtime-job-support/file-override-option-mismatch-exception.html) | The exception that is thrown when a file override has an option value that does not match expected by the named option. |
| [FileOverrideSettingsException](/reference/runtime/qsys-runtime-job-support/file-override-settings-exception.html) | The exception that is thrown when a file override specified in the config file is invalid. |
| [IntegratedFileSystem](/reference/runtime/qsys-runtime-job-support/integrated-file-system.html) | Holds the Integrated File System (IFS) root folder. |
| [InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html) | Defines the core behavior of an interactive job. |
| [InvalidMessageIntValueException](/reference/runtime/qsys-runtime-job-support/invalid-message-int-value-exception.html) | The exception that is thrown when an exception placeholder integer is not an integer value string. |
| [InvalidMessageLengthException](/reference/runtime/qsys-runtime-job-support/invalid-message-length-exception.html) | The exception that is thrown when the replacement data length does not correspond to placeholder length. |
| [InvalidMessagePlaceholderException](/reference/runtime/qsys-runtime-job-support/invalid-message-placeholder-exception.html) | The exception that is thrown when an message string is missing matching curly braces on a placeholder. |
| [Job](/reference/runtime/qsys-runtime-job-support/job.html) | Defines the core behavior of a Job that provides an environment to submit, control, and keep track of Program activation and execution. |
| [JobConfig](/reference/runtime/qsys-runtime-job-support/job-config.html) | Holds configuration values for the creation of new jobs. |
| [JobException](/reference/runtime/qsys-runtime-job-support/job-exception.html) | Defines the core behavior of the the base class that is thrown when there is a job exception. |
| [JobFrameworkException](/reference/runtime/qsys-runtime-job-support/job-framework-exception.html) | Defined the core behavior of exceptions thrown by Monarch Base and provides a base for derived exceptions. |
| [JobLogger](/reference/runtime/qsys-runtime-job-support/job-logger.html) | Defines the core behavior of a job message logger and provides a base for derived classes. |
| [JobStats](/reference/runtime/qsys-runtime-job-support/job-stats.html) | Tracks lifetime metrics for the job. |
| [JobStatus](/reference/runtime/qsys-runtime-job-support/job-status.html) | Represents the status of a job. |
| [LDACapacityException](/reference/runtime/qsys-runtime-job-support/lda-capacity-exception.html) | The exception that is thrown when a field being get or set on the LDA is beyond the LDA length. |
| [LDALengthException](/reference/runtime/qsys-runtime-job-support/lda-length-exception.html) | The exception that is thrown when a field being get or set from the LDA has a negative length. |
| [LDAOffsetException](/reference/runtime/qsys-runtime-job-support/lda-offset-exception.html) | The exception that is thrown when a field being get or set from the LDA has a negative offset. |
| [LocalDataCollection](/reference/runtime/qsys-runtime-job-support/local-data-collection.html) | Represents a versioned collection of name/value pairs. |
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | Represent a message sent by a program. |
| [MessageBase](/reference/runtime/qsys-runtime-job-support/message-base.html) | Represents a base class for messages, providing properties and methods for message text, cause, recovery suggestions, and logging functionality. |
| [MessageFormatter](/reference/runtime/qsys-runtime-job-support/message-formatter.html) | Provides functionality to format a message. |
| [MessageQueue](/reference/runtime/qsys-runtime-job-support/message-queue.html) | Holds a group of messages in a queue. |
| [MessageQueueNotFoundException](/reference/runtime/qsys-runtime-job-support/message-queue-not-found-exception.html) | The exception that is thrown when a program message queue is not found in the invocation stack. |
| [Module](/reference/runtime/qsys-runtime-job-support/module.html) | Defines the core behavior of classes that were migrated from RPG or CL programs and modules. |
| [ModuleCollection](/reference/runtime/qsys-runtime-job-support/module-collection.html) | A dictionary of the modules making up this program. |
| [ModuleImportAttribute](/reference/runtime/qsys-runtime-job-support/module-import-attribute.html) | Attribute to indicate the list of (external) modules this program will contain. |
| [NewActivationGroupAttribute](/reference/runtime/qsys-runtime-job-support/new-activation-group-attribute.html) | Defines the special Attribute used to mark a program or service program class for it to be activated in a brand new Activation Group. |
| [NoDeviceAvailableException](/reference/runtime/qsys-runtime-job-support/no-device-available-exception.html) | The exception that is thrown when an operation is attempted when the job is not attached to a device. |
| [ObjectLockRequest](/reference/runtime/qsys-runtime-job-support/object-lock-request.html) | Provides facilities to Allocate and De-Allocate object related. |
| [OpenAccessFile](/reference/runtime/qsys-runtime-job-support/open-access-file.html) | Provides the facilities to use a display file without prior infrastructure. |
| [OutOfProcessBatchJob](/reference/runtime/qsys-runtime-job-support/out-of-process-batch-job.html) | Defines the core behavior of an out of process batch job. |
| [Program](/reference/runtime/qsys-runtime-job-support/program.html) | Defines the core behavior of a program and provides a base for migrated derived classes. |
| [QueryCursor](/reference/runtime/qsys-runtime-job-support/query-cursor.html) | Represents the SQL Query Cursor. |
| [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) | Dictionary with Query result items. |
| [QueryValue](/reference/runtime/qsys-runtime-job-support/query-value.html) | Represents a Value stored in a SQL Query Result. |
| [RecursiveCallException](/reference/runtime/qsys-runtime-job-support/recursive-call-exception.html) | The exception that is thrown when a program is being called recursively. |
| [ServerTerminatedException](/reference/runtime/qsys-runtime-job-support/server-terminated-exception.html) | The exception that is thrown to signal the host server is being shut down. |
| [ServiceProgram](/reference/runtime/qsys-runtime-job-support/service-program.html) | Defines the core behavior of a service program and provides a base for migrated derived classes. |
| [ServiceProgramCollection](/reference/runtime/qsys-runtime-job-support/service-program-collection.html) | A dictionary of the service programs used by this program. |
| [ServiceProgramUseAttribute](/reference/runtime/qsys-runtime-job-support/service-program-use-attribute.html) | Attribute to indicate the list of service programs to which a program is bound. |
| [ShuttingDownException](/reference/runtime/qsys-runtime-job-support/shutting-down-exception.html) | The exception that is thrown to signal the Job is being shut down. |
| [Spooler](/reference/runtime/qsys-runtime-job-support/spooler.html) | Provides the infrastructure to manage spooled output from print files.  |
| [SQL_CommunicationsArea](/reference/runtime/qsys-runtime-job-support/sql-communications-area.html) | Implements SQLCA (SQL communications area) |
| [SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html) | Used to implement SQL PREPARE statements. |
| [SystemValue](/reference/runtime/qsys-runtime-job-support/system-value.html) | Provides System Value attributes. |
| [UnsupportedOperationException](/reference/runtime/qsys-runtime-job-support/unsupported-operation-exception.html) | The exception that is thrown when an unsupported operation is attempted. |
| [UserDefinedCommand](/reference/runtime/qsys-runtime-job-support/user-defined-command.html) | Defines the core behavior of user defined commands and provide a base for derived classes. |
| [WebDevice](/reference/runtime/qsys-runtime-job-support/web-device.html) | Defines the core behavior of the device handling the user interface for an interactive job and provides a base for derived classes. |
| [WebDisplayFile](/reference/runtime/qsys-runtime-job-support/web-display-file.html) | Provides a program with an interface to the user interactions, supporting read and write operation to the user's screen. |
| [WebSocketDevice](/reference/runtime/qsys-runtime-job-support/web-socket-device.html) | Implements a WebDevice using a socket to communicate with a website for its UI services. |
