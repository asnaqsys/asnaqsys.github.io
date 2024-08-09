---
title: "Module class                  | QSYS API Reference Guide"
description: "Defines the core behavior of classes that were migrated from RPG or CL programs and modules. "
last_modified_at: 2024-08-09T16:18:25Z
---

Defines the core behavior of classes that were migrated from RPG or CL programs and modules.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [Module](#modulecommonprogram)([CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html)) | Called from constructors in derived classes to initializes the Module class. 

### Module([CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html))

Called from constructors in derived classes to initializes the Module class. 

```cs
Module(CommonProgram)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [CommonProgram](/reference/runtime/qsys-runtime-job-support/common-program.html) | containerProgram | The program containing the module.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [IndicatorArray\<Len\<_1, _0, _0\>\>](/reference/runtime/qsys-runtime/indicator-array-1.html) | _IN | The array of 100 main indicators. |
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | _INLR | The Last Record indicator. |
| [Indicator](/reference/runtime/qsys-runtime/indicator.html) | _INRT | The Return indicator. |
| [ActivationGroup](/reference/runtime/qsys-runtime-job-support/activation-group.html) | ActivationGroup | Gets the program's activation group. |
| [Job](/reference/runtime/qsys-runtime-job-support/job.html) | CurrentJob | Gets the module's Job. |
| [DocumentLibraryObject](/reference/runtime/qsys-runtime-job-support/document-library-object.html) | DLO | Gets the Job's DLO. |
| [IntegratedFileSystem](/reference/runtime/qsys-runtime-job-support/integrated-file-system.html) | IFS | Gets the Job's IFS. |
| [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) | QueryResults | Used to retrieve host variables in EmbeddedSQL  |
| [Spooler](/reference/runtime/qsys-runtime-job-support/spooler.html) | Spooler | Gets the Job's spooler. |
| [SQL_CommunicationsArea](/reference/runtime/qsys-runtime-job-support/sql-communications-area.html) | SQLCA | Gets the SQL commuication area. It is populated AFTER (embedded) SQL command executes. |
| [Dictionary\<String, Object\>](https://learn.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-8.0) | SqlQueryResults | Gets the result dictionary used to retrieve host variables in EmbeddedSQL  |
| [DateTime](https://docs.microsoft.com/en-us/dotnet/api/system.datetime) | StartupMoment | Gets the timestamp when the module was created. |

## Methods

| Signature | Description |
| --- | --- |
| [Dispose](#void-disposebool-disposing)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Releases the resources used by the current instance of the Module class. This default implementation does nothing.
| [EndModuleCall()](#void-endmodulecall) | Notifies the program that contains this module that the *ENTRY module call has ended.
| [ExecOS400Command](#void-execos400commandstring-cmdtext)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Executes a command on the IBM i serving as the database server for the Job.
| [ExecSQL_Query](#queryresults-execsql-queryint-expectedresults-dbconnection-sqlconnection-string-sqltext-dbparm--parameters)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Execute an SQL Command producing a QueryResults.
| [ExecSQL_Query](#queryresults-execsql-queryint-expectedresults-string-sqltext-dbparm--parameters)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Execute an SQL Command, on the default Job's ado connection, producing a QueryResults.
| [ExecSQL_Query](#queryresults-execsql-queryint-expectedresults-sqlpreparedstatement-preparedstatement-dbparm--parameters)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Execute an prepared SQL Command producing a QueryResults.
| [ExecSQL_Statement](#void-execsql-statementdbconnection-sqlconnection-string-sqltext-dbparm--parameters)([DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Execute an non-query SQL Command.
| [ExecSQL_Statement](#void-execsql-statementstring-sqltext-dbparm--parameters)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Execute an non-query SQL Command on the default Job's ado connection.
| [ExecSQL_Statement](#void-execsql-statementsqlpreparedstatement-preparedstatement-dbparm--parameters)([SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html), [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html)) | Execute an non-query prepared SQL Command.
| [FormatMessage](#string-formatmessagestring-msgfile-string-msgid-string-msgdata-string-secondleveltext)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Produces the strings with the formatted first and second level text for a message. Any placeholders are replaced with values from the message data. 
| [GetLdaField](#string-getldafieldint-start-int-length)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)) | Gets a value stored in the LDA.
| [GetModule<T>()](#t-getmodule-t) | Gets a module contained in the same program or in one of the service programs.
| [PopInvocation()](#void-popinvocation) | Pops one invocation from the invocation stack.
| [PushInvocation()](#void-pushinvocation) | Pushes the caller procedure in the invocation stack.
| [ReceiveMessage](#message-receivemessageint-stackposition-string-stackname-messagetype-msgtype-string-msgkey-bool-remove)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Receive messages from the Program Queue. Messages are received in FIFO order.
| [ReceiveMessage](#message-receivemessagestring-pgmq-messagetype-msgtype-string-msgkey-bool-remove)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Receive messages from the Program Queue. Messages are received in FIFO order.
| [ReclaimActivationGroup](#void-reclaimactivationgroupstring-groupname)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Reclaim the resources on the Job's named activation group.
| [ReclaimResources](#void-reclaimresourcesbool-caller)([Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)) | Reclaim the resources on the Job's default activation group.
| [RemoveMessage](#void-removemessagestring-pgmq-string-messagekey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Remove messages from the program queue entry.
| [RemoveMessage](#void-removemessageint-stackposition-string-stackname-string-messagekey)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Remove messages from the Program Queue.
| [RemoveMessage](#void-removemessagestring-messagekey)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Remove messages from *PRVious program called.
| [SendExternalMessage](#string-sendexternalmessagestring-msgid-string-msgfilename-string-msgdata-messagetype-msgtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Send a message to *EXTernal message queue.
| [SendExternalMessage](#string-sendexternalmessagestring-msgtext-messagetype-msgtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Send text message to *EXTernal message queue.
| [SendProgramMessage](#string-sendprogrammessagestring-msgid-string-msgfilename-string-msgdata-string-pgmq-messagetype-msgtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Send message to program message entry queue in the invocation stack.
| [SendProgramMessage](#string-sendprogrammessagestring-msgid-string-msgfilename-string-msgdata-int-stackposition-string-stackname-messagetype-msgtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Send message to program message queue in the invocation stack.
| [SendProgramMessage](#string-sendprogrammessagestring-msgtext-string-pgmq-messagetype-msgtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Send text message to program message entry queue in the invocation stack.
| [SendProgramMessage](#string-sendprogrammessagestring-msgtext-int-stackposition-string-stackname-messagetype-msgtype)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html)) | Send text message to program message queue in the invocation stack.
| [SetLdaField](#void-setldafieldint-start-int-length-string-newvalue)([Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Stores a value in the LDA.

### void Dispose([bool disposing](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Releases the resources used by the current instance of the Module class. This default implementation does nothing.

```cs
void Dispose(bool disposing)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | disposing | true to release managed and unmanaged resources; false to release only unmanaged resources.

### void EndModuleCall()

Notifies the program that contains this module that the *ENTRY module call has ended.

```cs
void EndModuleCall()
```

### void ExecOS400Command([string cmdText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Executes a command on the IBM i serving as the database server for the Job.

```cs
void ExecOS400Command(string cmdText)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | cmdText | The command to execute on the server.

### QueryResults ExecSQL_Query([int expectedResults](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [DbConnection sqlConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [string sqlText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Execute an SQL Command producing a QueryResults.

```cs
QueryResults ExecSQL_Query(int expectedResults, DbConnection sqlConnection, string sqlText, DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | expectedResults | The number of expected results.
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | sqlConnection | An open connection to the server where the SQL command will execute.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sqlText | The SQL command to execute.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | An array of parameters to be used with the command.

#### Returns

| Type | Description
| --- | ---
| [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) | The results produced by the server.

### QueryResults ExecSQL_Query([int expectedResults](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string sqlText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Execute an SQL Command, on the default Job's ado connection, producing a QueryResults.

```cs
QueryResults ExecSQL_Query(int expectedResults, string sqlText, DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | expectedResults | The number of expected results.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sqlText | The SQL command to execute.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | An array of parameters to be used with the command.

#### Returns

| Type | Description
| --- | ---
| [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) | The results produced by the server.

### QueryResults ExecSQL_Query([int expectedResults](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [SqlPreparedStatement preparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html), [DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Execute an prepared SQL Command producing a QueryResults.

```cs
QueryResults ExecSQL_Query(int expectedResults, SqlPreparedStatement preparedStatement, DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | expectedResults | The number of expected results.
| [SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html) | preparedStatement | The prepared SQL command to execute.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | An array of parameters to be used with the command.

#### Returns

| Type | Description
| --- | ---
| [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) | The results produced by the server.

### void ExecSQL_Statement([DbConnection sqlConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0), [string sqlText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Execute an non-query SQL Command.

```cs
void ExecSQL_Statement(DbConnection sqlConnection, string sqlText, DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [DbConnection](https://learn.microsoft.com/en-us/dotnet/api/system.data.common.dbconnection?view=net-8.0) | sqlConnection | An open connection to the server where the SQL command will execute.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sqlText | The SQL command to execute.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | An array of parameters to be used with the command.

### void ExecSQL_Statement([string sqlText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Execute an non-query SQL Command on the default Job's ado connection.

```cs
void ExecSQL_Statement(string sqlText, DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | sqlText | The SQL command to execute.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | An array of parameters to be used with the command.

### void ExecSQL_Statement([SqlPreparedStatement preparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html), [DBParm\[\] parameters](/reference/runtime/qsys-runtime-job-support/db-parm.html))

Execute an non-query prepared SQL Command.

```cs
void ExecSQL_Statement(SqlPreparedStatement preparedStatement, DBParm[] parameters)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [SqlPreparedStatement](/reference/runtime/qsys-runtime-job-support/sql-prepared-statement.html) | preparedStatement | The prepared SQL command to execute.
| [DBParm\[\]](/reference/runtime/qsys-runtime-job-support/db-parm.html) | parameters | An array of parameters to be used with the command.

### string FormatMessage([string MsgFile](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgData](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [String& secondLevelText](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Produces the strings with the formatted first and second level text for a message. Any placeholders are replaced with values from the message data. 

```cs
string FormatMessage(string MsgFile, string MsgId, string MsgData, String& secondLevelText)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgFile | The message file name where the message description is to be found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgId | The message identification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgData | The replacement text, if any, for the message placeholders.
| [String&](https://docs.microsoft.com/en-us/dotnet/api/system.string) | secondLevelText | The formatted second level text of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The formatted first level text of the message.

### string GetLdaField([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types))

Gets a value stored in the LDA.

```cs
string GetLdaField(int start, int length)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where the value is stored.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to retrieve.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The requested field value.

### T GetModule<T>()

Gets a module contained in the same program or in one of the service programs.

```cs
T GetModule<T>()
```

### void PopInvocation()

Pops one invocation from the invocation stack.

```cs
void PopInvocation()
```

### void PushInvocation()

Pushes the caller procedure in the invocation stack.

```cs
void PushInvocation()
```

### Message ReceiveMessage([int stackPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string stackName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html), [string MsgKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool Remove](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Receive messages from the Program Queue. Messages are received in FIFO order.

```cs
Message ReceiveMessage(int stackPosition, string stackName, MessageType MsgType, string MsgKey, bool Remove)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | stackPosition | Relative position from the stackName starting at 0.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | stackName | Name of Program or Procedure in the stack.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | Type of message to receive.  Use Any if type is indifferent.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgKey | The message to remove.  Use null if key is indifferent.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Remove | true to remove the message from the queue.

#### Returns

| Type | Description
| --- | ---
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | The message specified or null if the message was not found in the queue.

### Message ReceiveMessage([string pgmQ](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html), [string MsgKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [bool Remove](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Receive messages from the Program Queue. Messages are received in FIFO order.

```cs
Message ReceiveMessage(string pgmQ, MessageType MsgType, string MsgKey, bool Remove)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pgmQ | The description of the program queue entry in the invocation stack. Composed of optional relative position (one of: *SAME, *PRV, number) and a procedure name (Use * for current procedure).
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | Type of message to receive.  Use Any if type is indifferent.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgKey | The message to Remove.  Use null if key is indifferent.
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | Remove | true to Remove the message from the queue.

#### Returns

| Type | Description
| --- | ---
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | The message specified or null if the message was not found in the queue.

### void ReclaimActivationGroup([string groupName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Reclaim the resources on the Job's named activation group.

```cs
void ReclaimActivationGroup(string groupName)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | groupName | Name of the activation group.

### void ReclaimResources([bool caller](https://docs.microsoft.com/en-us/dotnet/api/system.boolean))

Reclaim the resources on the Job's default activation group.

```cs
void ReclaimResources(bool caller)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean) | caller | true to include the resource of the module's program making this call; otherwise, false.

### void RemoveMessage([string pgmQ](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string messageKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Remove messages from the program queue entry.

```cs
void RemoveMessage(string pgmQ, string messageKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pgmQ | The description of the program queue entry in the invocation stack. Composed of optional relative position (one of: *SAME, *PRV, number) and a procedure name (Use * for current procedure).
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageKey | The message to remove.  It should always be "*ALL".

### void RemoveMessage([int stackPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string stackName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string messageKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Remove messages from the Program Queue.

```cs
void RemoveMessage(int stackPosition, string stackName, string messageKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | stackPosition | Relative position from the stackName starting at 0.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | stackName | Name of Program or Procedure in the stack.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageKey | The message to remove.  It should always be "*ALL".

### void RemoveMessage([string messageKey](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Remove messages from *PRVious program called.

```cs
void RemoveMessage(string messageKey)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | messageKey | The message to remove.  It should always be "*ALL".

### string SendExternalMessage([string MsgId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgData](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Send a message to *EXTernal message queue.

```cs
string SendExternalMessage(string MsgId, string MsgFileName, string MsgData, MessageType MsgType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgId | The message identification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgData | The replacement text, if any, for the message placeholders.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgFileName | The message file name where the message description is to be found.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The message key.

### string SendExternalMessage([string MsgText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Send text message to *EXTernal message queue.

```cs
string SendExternalMessage(string MsgText, MessageType MsgType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgText | The user provide text of the message.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The message key.

### string SendProgramMessage([string MsgId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgData](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string pgmQ](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Send message to program message entry queue in the invocation stack.

```cs
string SendProgramMessage(string MsgId, string MsgFileName, string MsgData, string pgmQ, MessageType MsgType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgId | The message identification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgData | The replacement text, if any, for the message placeholders.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgFileName | The message file name where the message description is to be found.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pgmQ | The description of the program queue entry in the invocation stack. Composed of optional relative position (one of: *SAME, *PRV, number) and a procedure name (Use * for current procedure).
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The message key.

### string SendProgramMessage([string MsgId](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgFileName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string MsgData](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int stackPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string stackName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Send message to program message queue in the invocation stack.

```cs
string SendProgramMessage(string MsgId, string MsgFileName, string MsgData, int stackPosition, string stackName, MessageType MsgType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgId | The message identification.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgData | The replacement text, if any, for the message placeholders.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgFileName | The message file name where the message description is to be found.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | stackPosition | Relative position from the stackName starting at 0.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | stackName | Name of Program or Procedure in the stack.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The message key.

### string SendProgramMessage([string MsgText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [string pgmQ](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Send text message to program message entry queue in the invocation stack.

```cs
string SendProgramMessage(string MsgText, string pgmQ, MessageType MsgType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgText | The user provide text of the message.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | pgmQ | The description of the program queue entry in the invocation stack. Composed of optional relative position (one of: *SAME, *PRV, number) and a procedure name (Use * for current procedure).
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The message key.

### string SendProgramMessage([string MsgText](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [int stackPosition](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string stackName](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0), [MessageType MsgType](/reference/runtime/qsys-runtime-job-support/message-type.html))

Send text message to program message queue in the invocation stack.

```cs
string SendProgramMessage(string MsgText, int stackPosition, string stackName, MessageType MsgType)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | MsgText | The user provide text of the message.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | stackPosition | Relative position from the stackName starting at 0.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | stackName | Name of Program or Procedure in the stack.
| [MessageType](/reference/runtime/qsys-runtime-job-support/message-type.html) | MsgType | One of the enumeration values that specifies the severity of the message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | The message key.

### void SetLdaField([int start](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [int length](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types), [string newValue](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Stores a value in the LDA.

```cs
void SetLdaField(int start, int length, string newValue)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | start | The one-based index into the location within the LDA where newValue will be stored.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | length | The length in characters of the value to store.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | newValue | The string value to store in the LDA.
