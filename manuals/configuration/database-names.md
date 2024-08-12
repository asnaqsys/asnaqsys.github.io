---
title: "Effective Database Store Naming Conventions Guide"
description: "This document provides detailed instructions on how to configure the database name store, including setting up the initial environment, defining database names, and ensuring secure access."
---

## DataGate Source Profile

In order for DataGate to establish a connection from an application to a database server it is necessary to provide information about the server, communication protocol to use, user and password for the connection, etc.  This information is captured in what DataGate calls a database [Source Profile](/reference/datagate/datagate-providers/source-profile.html).

Monarch Base provides the class `QSys.Runtime.Database` to encapsulate a DataGate Source Profile and a DataGate connection to a database.

`QSys.Runtime.Database` provides a set of properties to establish programmatically the attributes of it Source Profile; it also provides methods to let DataGate set the attributes from configurations settings stored in text files or from other Configuration Sources as discussed below.

## Database Name
Database Names are unique, human-friendly character strings associated with the properties of a Source Profile within a Configuration Source.  Database Name identifiers may follow any mnemonic convention the user or enterprise chooses (for example, "milwaukee-10234-sql-server").  For purposes of comparison within DataGate, Database Name identifiers are [culturally-sensitive, but case-insensitive](https://docs.microsoft.com/en-us/dotnet/standard/base-types/best-practices-strings#recommendations-for-string-usage).

The `QSys.Runtime.Database` constructor accepts a Database Name string and it also provides the method SetDBName to set the string at run time.

Before the constructor or the SetDBName are executed, one or more Configuration Sources should be established via the static method `PrepareNameStore()`.

## Configuration Sources
The `PrepareNameStore()` method supports the following sources:
1. JSON Files
2. User Secrets
3. Environmental Variables
4. Command Line Arguments


### JSON Files
The following sample JSON file defines two Database Names profiles, the first one called "AppDB" and the second "HRDB":
```json
{
    "asna": {
        "dataGate": {
            "sources": {
                "AppDB": {
                    "server": "TESTSERV",
                    "user": "TESTUSER",
                    "password": "0Test.Psw9",
                    "platformAttribute": "*DATALINK",
                    "initialLibraryList": [ "ERCAP" ],
                    "port": 5160,
                },
                "HRDB": {
                    "server": "DEVSERV"
                }
            }
        }
    }
}
```

DataGate defines a [DataGate Schema](asna-qsys-schema.json) for JSON files defining named Source Profiles. Adding a reference to the schema file can assist on editors that provide intellisense like VS Code and Visual Studio.

```json
{
    "$schema": "asna-qsys-schema.json",
    "asna": {
        "dataGate": {
            "sources": {
                "AspenRND": {
                    "server": "MyMSSQL",
                    "label": "SQL",
                    "platformAttribute": "*SQLCLIENT",
                    "initialLibraryList": [
                        "MY_LIB"
                    ],
                    "user": "*DOMAIN"
                }
            }
        }
    }
}
```

### The DataGate JSON File
By convention a default JSON file called 'asnasettings.json' can be placed in the sub folder 'ASNA/DataGate' under the special folder [LocalApplicationData](https://docs.microsoft.com/en-us/dotnet/api/system.environment.specialfolder). 

If the file is not there, you can create it.

On a Windows system, the full path would be:
```
C:\Users\<USER>\AppData\Local\ASNA\DataGate\asnasettings.json
```

Where `<USER>` is the name of the user running the application.  This location and name are default options.  A DataGate JSON file may be located in any accessible directory and given any valid file name.

### Secrets
Similar to ASP.NET Core [User Secrets](https://docs.microsoft.com/en-us/aspnet/core/security/app-secrets), sensitive data can be kept in safe storage on a development machine. The most sensitive pieces of data on a Source Profile are the User and Password. 

You can learn more about the [Secret Manger here](https://docs.microsoft.com/en-us/aspnet/core/security/app-secrets?#secret-manager) and how to [manage user secrets with Visual Studio here](https://docs.microsoft.com/en-us/aspnet/core/security/app-secrets?tabs=windows#manage-user-secrets-with-visual-studio).

### Environmental Variables
Environment Variables are another place to set Source Profile attributes like this:

```
set asna__dataGate__sources__AppDB__password=TEMP1234
```

### Command Line Arguments
Finally, the command line can receive arguments with Source Profile attributes, like this one:

```
dotnet run /asna:dataGate:sources:AppDB:password=TEMP1234
```

## PrepareNameStore
The `PrepareNameStore<T>()` method accepts an options parameter and a list of JSON configuration files.

```cs
public static bool PrepareNameStore<T>(NameStoreOptions options, params string[] configFiles) where T : class
```

The ``options`` parameter, of enumerated type NameStoreOptions, has the following set of flags:

 * UseJsonDefaultPath = 1,
 * UseSecrets = 2,
 * UseEnvironmentalVars = 4,
 * UseCommandLineArgs = 8,

Configuration sources provide values to the store in order of increasing priority as given by the integer value shown above.  When two sources define a value for a single attribute of a database name, the source with higher priority has precedence over the attribute value defined by the lower priority source.

An optional list of configuration files specified by parameter ``configFiles`` are loaded in the order in which they are given, but after the default JSON file (if specified) and before the Secrets (if specified). 

> Notice that a website's `appsettings.json` file can be used a source for database names.

The Secrets used are those associated with the assembly of the type `<T>` passed to `PrepareNameStore<T>()`

The static method `PrepareNameStore<T>()` should be called only once per process.  It is typically called in the static constructor of the main application class; in the case of Monarch migrated applications, it is called in the static constructor of MyJob.

Here is a common pattern used:
```cs
    public partial class MyJob : InteractiveJob
    {
        . . .

        public Database MyDatabase = new Database("AppDB");

        . . .

        static MyJob()
        {
            Database.PrepareNameStore<MyJob>();
        }

        override protected void ExecuteStartupProgram()
        {
            . . .
            MyDatabase.Open();
            . . .
        }
```

Here is an alternative example:
```cs
    public partial class MyJob : Job
    {
        . . .

        public Database MyDatabase = new Database("");

        . . .

        static MyJob()
        {
            Database.PrepareNameStore<MyJob>(NameStoreOptions.UseEnvironmentalVars | NameStoreOptions.UseCommandLineArgs,
                                             @"C:\AppMain\ProductionSettings.json", @".\appsettings.json");
        }

        override protected void ExecuteStartupProgram()
        {
            . . .
            MyDatabase.SetDatabaseName("AppDB");
            MyDatabase.Open();
            . . .
        }

```
