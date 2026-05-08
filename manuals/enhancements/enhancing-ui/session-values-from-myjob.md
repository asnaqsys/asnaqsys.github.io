---
title: "Accessing Session Values from MyJob Class"
description: "Learn how to efficiently retrieve session values in MyJob, enhancing data management and user experience in your applications."
---

The Monarch Base architecture of an [interactive applications](/concepts/architecture/application-architecture.html#interactive-job-architecture) divides the user interface from the business logic.  The user interface runs in a Razor Pages based Website while the business logic DLLs may be run in a separate thread within the website or potentially in a separate process.  

The typical entry point into the business logic programs is the `ExecuteStartupProgram()` method of the `MyJob` class.

Sometimes is convenient to have `ExecuteStartupProgram()` get, or set, the value of certain elements stored in the Website's Session, e.g.: User Name or Password.  

The `MyJob` class extends the Monarch Base class `InteractiveJob` which provides two methods to Get and Set values in the Website's Session.  The values are of type string.

The following example shows how to override the database connection using a user and password stored in the Website's Session:

```c#
    override protected void ExecuteStartupProgram()
    {
        Indicator _LR = '0';

        string sessionUserName = GetSessionValue("Job_UserName");
        string sessionPass = GetSessionValue("Job_Pass");
        if (sessionUserName != null && sessionPass != null)
        {
            PsdsJobUser = sessionUserName;
            MyDatabase.User = sessionUserName;
            MyDatabase.Password = sessionPass;
                               
            SetSessionValue("Job_Pass", string.Empty); // Clear up the password from Session
            SetSessionValue("Job_UP", "Accepted");
        }

        MyDatabase.Open();
        _DynamicCaller.CallD("Acme.Starter", out _LR);
    }
```

The Session entries with their keys and string values are up to the developer to create as the application is enhanced.
