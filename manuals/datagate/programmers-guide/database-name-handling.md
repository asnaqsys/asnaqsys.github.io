---
title: "Effective Database Name Handling Techniques"
description: "This document focuses on the methods and best practices for handling database names within applications, including naming conventions, case sensitivity issues, and strategies for avoiding naming conflicts."
---

DG for Visual Studio is adept at handling the standard "database name" conventions familiar to AVR programmers and users of tools such as DataGate Database Manager. A database name is simply a shorthand notation, redirecting the client-side engine to a set of client/server database connection parameters stored in the system registry. These registry entries can be accessed and manipulated with the [ SourceProfile](source-profile-class.html) object. **SourceProfile** provides the programmer with some of the functionality of DataGate Database Manager’s "Work with Database Names" option. The object constructor and methods [ Register](source-profile-class-register-method.html) and [Unregister](source-profile-class-unregister-method.html) are used to retrieve, persist, and delete respectively, database name registry entries.

The following example retrieves a database name called "Asna 400 db" (in the process of constructing the SourceProfile object), changes the user and password, and then saves the changes by calling Register. 

```cs 
  using ASNA.DataGate.Providers;
  SourceProfile AsnaDbName;
  AsnaDbName = new SourceProfile("Asna 400 db");
  AsnaDbName.User = "NewUser";
  AsnaDbName.Password = "NewPasswd";
  AsnaDbName.Register()
```

To discover the currently registered database names available for use in a program, use the [SourceProfile.GetNames](source-profile-class-get-names-method.html) static method. This method returns an array of strings as shown in the following example. This snippet of AVR code will print "*PUBLIC" and "User" database names registered on the machine where the code runs. 

```cs 
     Console.WriteLine( "*Public Database Names:" );
  Foreach Name(DbName) Collection(SourceProfile.GetNames(*True)) 
				Type(*String);
     Console.WriteLine( "  *Public\" + DbName );
  Endfor;
     Console.WriteLine( "User Database Names:" );
  Foreach Name(DbName) Collection(SourceProfile.GetNames(*False)) 
				Type(*String);
  Console.WriteLine( "  " + DbName );
  Endfor;
```

Console.WriteLine( " " + DbName ) Endfor <p> **SourceProfile** objects may be assigned to the [ AdgConnection.SourceProfile](adg-connection-class-source-profile-property.html) property to force a subsequent call to [ AdgConnection.Open](adg-connection-class-open-method.html) to use the SourceProfile’s connection parameters. Changing **AdgConnection.SourceProfile** has no effect on the database connection of an **AdgConnection** object in the *Open* state. Rather, **AdgConnection.SourceProfile** is used by the **AdgConnection.Open** method to initialize the database connection. 
## See Also

[Database Name Handling](database-name-handling.html)<br />[AdgConnection Class](adg-connection-class.html)<br />[AdgConnection.Open Method](adg-connection-class-open-method.html)<br />[AdgConnection.SourceProfile 
					Property](adg-connection-class-source-profile-property.html)<br />[AdgConnection.State Property](adg-connection-class-state-property.html)<br />[SourceProfile Class](source-profile-class.html)<br />[SourceProfile.Register 
					Method](source-profile-class-register-method.html)<br />[SourceProfile.GetNames 
					Method](source-profile-class-get-names-method.html)<br />[SourceProfile.Unregister 
					Method](source-profile-class-unregister-method.html)

