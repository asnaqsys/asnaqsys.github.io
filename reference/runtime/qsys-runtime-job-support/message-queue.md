---
title: "MessageQueue class            | QSYS API Reference Guide"
description: "Holds a group of messages in a queue. "
last_modified_at: 2024-08-09T16:18:25Z
---

Holds a group of messages in a queue.

**Namespace:** ASNA.QSys.Runtime.JobSupport
**Assembly:** ASNA.QSys.Runtime.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)
<br>
<br>

## Constructors

| Name | Description |
| --- | --- |
| [MessageQueue()](#messagequeue) | Initializes a new, empty instance of the MessageQueue class.

### MessageQueue()

Initializes a new, empty instance of the MessageQueue class.

```cs
MessageQueue()
```

## Methods

| Signature | Description |
| --- | --- |
| [Clear()](#void-clear) | Removes all elements from the MessageList.
| [Dequeue](#void-dequeuemessage-message)([Message](/reference/runtime/qsys-runtime-job-support/message.html)) | Removes the message from the queue.
| [GetEnumerator()](#ienumerator-getenumerator) | Returns an IEnumerator that iterates through the MessageQueue.
| [Queue](#void-queuemessage-message)([Message](/reference/runtime/qsys-runtime-job-support/message.html)) | Enqueues a message at the end of the queue.

### void Clear()

Removes all elements from the MessageList.

```cs
void Clear()
```

### void Dequeue([Message message](/reference/runtime/qsys-runtime-job-support/message.html))

Removes the message from the queue.

```cs
void Dequeue(Message message)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | message | The message to be dequeued.

### IEnumerator GetEnumerator()

Returns an IEnumerator that iterates through the MessageQueue.

```cs
IEnumerator GetEnumerator()
```

### void Queue([Message message](/reference/runtime/qsys-runtime-job-support/message.html))

Enqueues a message at the end of the queue.

```cs
void Queue(Message message)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [Message](/reference/runtime/qsys-runtime-job-support/message.html) | message | The message to be added.
