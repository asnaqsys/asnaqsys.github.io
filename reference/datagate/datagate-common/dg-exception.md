---
title: "dgException class             | QSYS API Reference Guide"
description: "The dgException class is a custom exception class that extends the base Exception class. It provides additional functionality for handling errors spec"
last_modified_at: 2024-08-09T17:25:07Z
---

The dgException class is a custom exception class that extends the base Exception class.
It provides additional functionality for handling errors specific to the application.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)
<br>
<br>
## Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.


## Constructors

| Name | Description |
| --- | --- |
| [dgException()](#dgexception) | Initializes a new instance of the dgException class.
| [dgException](#dgexceptionstring)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Initializes a new instance of the dgException class with a specified error message.
| [dgException](#dgexceptionstring-exception)([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Initializes a new instance of the dgException class with a specified error message and a reference to the inner exception that is the cause of this exception.
| [dgException](#dgexceptiondgerrornumber-int32-dgerrorclass-string-string-exception)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.
| [dgException](#dgexceptiondgerrornumber-int32-dgerrorclass-string-string)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.
| [dgException](#dgexceptiondgerrornumber)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html)) | Create a dgException with the passed error code.
| [dgException](#dgexceptiondgerrornumber-exception)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception)) | Create a dgException with the passed error code and exception.

### dgException()

Initializes a new instance of the dgException class.

```cs
dgException()
```

### dgException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Initializes a new instance of the dgException class with a specified error message.

```cs
dgException(String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The message that describes the error.

### dgException([String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Initializes a new instance of the dgException class with a specified error message and a reference to the inner exception that is the cause of this exception.

```cs
dgException(String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message that explains the reason for the exception.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The exception that is the cause of the current exception, or a null reference if no inner exception is specified.

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.

```cs
dgException(dgErrorNumber, Int32, dgErrorClass, String, String, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | systemError | The system error code.
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | errorClass | The class of the error.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The error text.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | inner | The inner exception.

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32), [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string))

Create a dgException with the passed error code, system error code,error class, and text.  This dgException is constructed and thrownwhen the database server program returns an error.

```cs
dgException(dgErrorNumber, Int32, dgErrorClass, String, String)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.
| [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32) | systemError | The system error code.
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | errorClass | The class of the error.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | message | The error message.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | text | The error text.

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html))

Create a dgException with the passed error code.

```cs
dgException(dgErrorNumber)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.

### dgException([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html), [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception))

Create a dgException with the passed error code and exception.

```cs
dgException(dgErrorNumber, Exception)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | error | The error code.
| [Exception](https://docs.microsoft.com/en-us/dotnet/api/system.exception) | e | The Exception object.

## Properties

| Type | Name | Description
| --- | --- | --- 
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | DefaultErrorClass | Gets or sets the default error class. This property is used to categorize the type of error that occurred. |
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) | Error | The error code for this dgException.  For server side errors, thisis the error code returned by the server following a databasetransaction. |
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | ErrorClass | The error class for this dgException. This categorizes the type of error that occurred. |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Message | Gets a message that describes the current exception. This property is overridden to provide custom error messages. |
| [Int32](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types) | SystemError | The system error code, if any for this dgException.  This memberwill contain meaningful information only with the value ofErrorClass is one of the following: |
| [String](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0) | Text | The text message for this dgException. This provides additional details about the error. |

## Methods

| Signature | Description |
| --- | --- |
| [FormatMessage](#string-formatmessageiformatprovider-provider-string-msg)([IFormatProvider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0), [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)) | Formats the error message into a single string for logging or displaying to the user.
| [GetDefaultErrorClass](#dgerrorclass-getdefaulterrorclassdgerrornumber-err)([dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html)) | Each dgErrorNumber has a default associated dgErrorClass.  Thismethod returns it.
| [GetVerboseText()](#string-getverbosetext) | Return a string containing a verbose description of thedgException. This string will most likely contain line separatorcharacters.  All dgException member variables are included in thestring.

### string FormatMessage([IFormatProvider provider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0), [string msg](https://learn.microsoft.com/en-us/dotnet/api/system.string?view=net-8.0))

Formats the error message into a single string for logging or displaying to the user.

```cs
string FormatMessage(IFormatProvider provider, string msg)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [IFormatProvider](https://learn.microsoft.com/en-us/dotnet/api/system.iformatprovider?view=net-8.0) | provider | An object that supplies culture-specific formatting information.
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | msg | The error message.

#### Returns

| Type | Description
| --- | ---
| [String](https://docs.microsoft.com/en-us/dotnet/api/system.string) | A formatted string containing the error message.

### dgErrorClass GetDefaultErrorClass([dgErrorNumber err](/reference/datagate/datagate-common/dg-error-number.html))

Each dgErrorNumber has a default associated dgErrorClass.  Thismethod returns it.

```cs
dgErrorClass GetDefaultErrorClass(dgErrorNumber err)
```

#### Parameters

| Type | Parameter name | Description
| --- | --- | ---
| [dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) |  | 

#### Returns

| Type | Description
| --- | ---
| [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) | 

### string GetVerboseText()

Return a string containing a verbose description of thedgException. This string will most likely contain line separatorcharacters.  All dgException member variables are included in thestring.

```cs
string GetVerboseText()
```

### Example 1. dgException ErrorClass and SystemError properties example.

```cs 
  /* This code attempts to open a file exclusively. 
  * If it fails, we print out the IBM i exception responsible.
  * "dbFile" is of type FileAdapter. */ 
  dbFile.AccessMode = AccessMode.Write;
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;
  dbFile.OpenAttributes.WaitForFile = 0;

  AdgDataSet dataSet = null;
  try
  {
      dbFile.Open(dataSet);
  }
  catch(dgException dgEx)
  {
      /* Take special action if error is due to the IBM i exception
       * "CPF1002". */
      if (dgEx.ErrorClass == dgErrorClass.dgEC_AS400CPF &amp;&amp;
          dgEx.SystemError.ToString("X") == "1002")
      {
          MessageBox.Show("iSeries threw exception CPF1002.");
          // Take alternative action here.
      }
      else
      {
          /* Throw exception otherwise. */
          throw dgEx;
      }
  }
```

### Example 2. dgException Message property example.


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* This will show a somewhat specific message as to what 
       * went wrong opening the file. */
      MessageBox.Show(dgEx.Message, "Error opening file");
      //Exit procedure here.
  }
```

## Example 3. GetVerboseText method example.

```cs 
  /* Verbose text generates a large string which is a concatanation 
   * of several of dgException's properties and also shows the
   * stack trace. While not very user friendly, it can come in handy
   * developing a program. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read ;

  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);

  /* We retrieve the record for customer number 7800. */
  AdgKeyTable keyTbl = myDS.NewKeyTable("RCMMASTL1");
  keyTbl.Row["CMCUSTNO"] = 7800;
  try
  {
      dbFile.ReadRandomKey(myDS, ReadRandomMode.Equal, LockRequest.Write, keyTbl);
      myDS.ActiveRow["CMCUSTNO"] = 300;
      dbFile.ChangeCurrent(myDS);
  }
  catch(dgException dgEx)
  { /* Print out Verbose text to figure out why ReadRandomKey is
     * throwing an exception. */
      MessageBox.Show(dgEx.GetVerboseText(), "Datagate Exception");
  }

  dbFile.Close();
  db.Close();
```

## Example 4. dgErrorNumber property example.


```cs 
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMMASTERL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;

  AdgDataSet myDS = null;
  try
  {
      dbFile.OpenNewAdgDataSet(out myDS);
  }
  catch(dgException dgEx)
  {
      /* There are many reasons why opening a file can fail. Here, we
       * catch some of the more general ones. */
      if (dgEx.Error == dgErrorNumber.dgEmMNOTFND)
          MessageBox.Show("Member " + dbFile.MemberName + " not found!", "Error opening file");
      else if (dgEx.Error == dgErrorNumber.dgEmFNOTFND)
          MessageBox.Show("File " + dbFile.FileName + " not found!", "Error opening file");
      else
          MessageBox.Show(dgEx.Message, "Error opening file");
          //Exit procedure here.
  }

  /* Do some action here. */

  dbFile.Close();
  db.Close();
```


