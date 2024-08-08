---
title: "dgErrorClass enum             | QSYS API Reference Guide"
description: "Represents the different error classes generated as a result of Acceler8DB or Datagate/400 server errors. "
last_modified_at: 2024-08-08T21:41:32Z
---

Represents the different error classes generated as a result of Acceler8DB or Datagate/400 server errors.

**Namespace:** ASNA.DataGate.Common
**Assembly:** ASNA.QSys.DataGate.Client.dll
<br>
<br>

## Enum Values

| Name | Description | Value
| --- | --- | --- 
| dgEC_Access | Represents an access error. | 3 |
| dgEC_APPC | Represents an APPC error. | 10 |
| dgEC_AS400CPF | Represents an AS400 CPF error. | 16 |
| dgEC_AS400CPI | Represents an AS400 CPI error. | 18 |
| dgEC_AS400DG8 | Represents an AS400 DG8 error. | 19 |
| dgEC_AS400MCH | Represents an AS400 MCH error. | 17 |
| dgEC_Base | Represents a base error. | 1 |
| dgEC_CallParm | Represents a call parameter error. | 8 |
| dgEC_Catalog | Represents a catalog error. | 2 |
| dgEC_Command | Represents a command error. | 13 |
| dgEC_CommitCtl | Represents a commit control error. | 20 |
| dgEC_Compiler | Represents a compiler error. | 5 |
| dgEC_ExitPoints | Represents an exit points error. | 22 |
| dgEC_License | Represents a license error. | 14 |
| dgEC_Object | Represents an object error. | 7 |
| dgEC_Print | Represents a print error. | 9 |
| dgEC_Repository | Represents a repository error. | 6 |
| dgEC_SqlServer | Represents a SQL Server error. | 21 |
| dgEC_SSL | Represents an SSL error. | 23 |
| dgEC_Stream | Represents a stream error. | 4 |
| dgEC_Supervisor | Represents a supervisor error. | 12 |
| dgEC_System | Represents a system error. | 15 |
| dgEC_TCPIP | Represents a TCP/IP error. | 11 |
| dgEC_Unknown | Represents an unknown error. | 0 |

## Examples 


```cs 
  /* This code attempts to open a file exclusively. 
   * If it fails, we print out the IBM i exception responsible.
   * "dbFile" is of type FileAdapter. */ 
  dbFile.AccessMode = AccessMode.Write;
  dbFile.OpenAttributes.ShareTypes = ShareTypes.Exclusive;

  AdgDataSet dataSet = null;
  try
  {
      dbFile.Open(dataSet);
  }
  catch(dgException dgEx)
  {
      string msg;
      switch(dgEx.ErrorClass)
      {
          case dgErrorClass.dgEC_AS400CPF:
              msg = "CPF";
              break;
          case dgErrorClass.dgEC_AS400CPI:
              msg = "CPI";
              break;
          case dgErrorClass.dgEC_AS400DG8:
              msg = "DG8";
              break;
          case dgErrorClass.dgEC_AS400MCH:
              msg = "MCH";
              break;
          default:
              throw dgEx; /* Throw exception otherwise. */
      }
      /* Append the hexadecimal value of the SystemError to
       * form the classic name of the IBM i exception. */
      msg = msg + dgEx.SystemError.ToString("X");
      MessageBox.Show("iSeries threw exception " + msg + 
          " while opening file.", "iSeries exception.");
      /* Throw exception otherwise. */
      throw dgEx;
  }
```

