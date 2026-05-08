---
title: "Migrated Embedded SQL Statements to SQL Server"
description: "Unlock the power of RPG embedded SQL in MSSQL. This guide offers insights, best practices, and tips for effective database management and queries."
---

## Overview

When an RPG program with embedded SQL is migrated, the SQL statements are used to create requests to the database via the ADO.NET library.  Monarch provides a thin layer over the ADO facilities to facilitate the migration of the SQL statements.  There are two areas that may require manual remediation when the target database is SQL Server.  These areas are:
   - Syntax may need updating to comply with T-SQL.
   - Use of Library List must be resolved in code.

## IBM specific SQL syntax vs T-SQL

When a developer uses an SQL Statement within the RPG program, the statement may be standard SQL or it may contain elements that are specific to extensions supported by IBM.  When the statement is not standard SQL, then it will be necessary to modify it to conform to what can be supported by SQL Server's T-SQL. Some of these extensions include:
 - Operators like `¬>`, `'&'`, `*EQ`
 - Naming convention (`*SYS` vs `*SQL`)
 - Library List to locate DB objects

## Host Variables

A *host variable* is a field in the RPG legacy program that is specified in a SQL statement.

Embedded SQL syntax allows the use of *host variables* by pre-pending a colon in front of the field names.

For example,

```cs
0013.00        EXEC SQL                                                                                         
0014.00            SELECT SUM(BCAQTY) into :total FROM HBC
0015.00            WHERE BCCNUM = :piConsignment AND BCID = 'BC';                                                              
```

The fields `total` and `piConsignment` are used in this sample SQL statement indicated by pre-pending a colon to each field name.

This sample statement is migrated as the following code:

```cs
QueryResults = ExecSQL_Query( 1,          +
   "SELECT SUM(BCAQTY) FROM HBC         " + + 
   "WHERE BCCNUM = @sql_parm_1 AND BCID = ""BC"";", + 
   *New DBDecimalParm(piConsignment, %Len(piConsignment), %DecPos(piConsignment)) +
)

/region QueryResult Into total
If ( QueryResults <> *nothing )
    total = QueryResults[0].ToDecimal()
EndIf
/endregion
```

[QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) is a Runtime defined collection that is used (temporarily) to hold the results of the SQL operation.

Notice in the Migrated code, how the *host variables* are split between `input` and `output`. 

The `input` *host variables* are used by the SQL statements and indicated using the `@sql_parm_n` placeholder name (where `n` is the ordinal number of the variable used ). Following the SQL statement, the *host variables* values are passed **in order** to the `ExecQSL_Query` method, using `DBxxxParm` parameter class helpers (where xxx is `Char`, `Str`, `Decimal`, etc. according to the field type).

The `output` *host variables* appear in the migration in the *region* conditioned by [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) being different than  * nothing (or `null` in C#). Notice how each value in the [QueryResults](/reference/runtime/qsys-runtime-job-support/query-results.html) is retrieved using the indexer `[n]` (where `n` is a zero-based index), in the same order as the `output` *host variables* are referenced by the original Embedded SQL. (Each value is converted to the proper type using `ToXxx()` method helpers).

>Note: When the runtime executes the query, the `@sql_parm_n` placeholder parameters will be replaced by `?` - question mark symbol - (one per parameter) when using [ODBC.NET Provider](https://learn.microsoft.com/en-us/dotnet/api/system.data.odbc.odbccommand.commandtext?view=dotnet-plat-ext-8.0). **ODBC** does not allow named parameter passing. Please check `MyJob` class to determine which ADO.NET connection object is being used by the Logic Assembly.

<br>

## Locating files via the library list

> Notice that for 'regular' database access via record level file operations, the library list is supported by DataGate Linear. This section is concerned only with the resolution of the library list where needed in migrated **embedded sql** statements.

Use DataGate facilities to locate the library for a specific file (table/view) and then use the library name as part of the in-line SQL statement.  DataGate provides the method `ResolvePathName()` which is available for any kind of database object, this method can be the base to create a new method  specific for resolving a file’s library. 

Since this technique involves an extra call to the Datagate server to run the stored procedure to iterate over the library files to find the library location, the library name can be cached for scenarios where the SQL statement is run in a loop with no intervining changes to the library list.

**Usage:**
```cs
    string lib = ResolveLibraryForFile(CurrentJob.Database.Connection, "ACAMCU");
    QueryCursor C = new QueryCursor(CurrentJob.ADO_Connection, 
                        $"SELECT ACCNUM, AMNT, CURRENCY FROM {lib}.ACAMCU " + "WHERE COMPANY = @sql_parm_1;", 
                        new DBDecimalParm(DFCOMP, 2, 0));
```              

**Implementation:**
```cs
using ASNA.DataGate.Client;
using ASNA.DataGate.Common;

    . . .
    static internal string ResolveLibraryForFile(AdgConnection cn, string fileName)
    {
        try
        {
            IFileObject fileObject = AdgFactory.NewFile(cn, "*LIBL/" + fileName.Trim());
            string filePath = fileObject.ResolvePathName();
            if (filePath != null)
            {
                String[] strings = filePath.TrimStart('/').Split('/');
                return strings[0].Trim();
            }
       }
       catch(dgException _)
       {
       }
       return null;
    }
    . . . 
```

## Troubleshooting Complex SQL Statements

[SQL language for Db2 for IBM® i](https://www.ibm.com/docs/en/i/7.5?topic=reference-sql) is a very powerful language with a very flexible and rich syntax.

SQL statements remain as *text* during the compilation of a .NET Application. The SQL syntax validation *is deferred* until the the statement is executed. 

During or after the Migration, it is **not** uncommon to end up with a SQL statement that is not valid. Invalid SQL statements are sometimes difficult to fix (particularly when they are large).  

For those situations, the use of [SQL Parser Explorer Tool](/examples/sql-parser-explorer.html) is recommended.

Once the syntax is corrected, the [ADO.NET Provider for SQL Server](https://learn.microsoft.com/en-us/sql/connect/ado-net/microsoft-ado-net-sql-server?view=sql-server-ver16) will report back error codes that can be analyzed to fix execution issues.

Legacy RPG logic may depend on [SQLCA](https://www.ibm.com/docs/en/i/7.3?topic=reference-sqlca-sql-communication-area) which defines *program global* fields that provide access to execution state reporting fields like [SQLSTATE](https://www.ibm.com/docs/en/i/7.3?topic=area-field-descriptions) and [SQLCODE](https://www.ibm.com/docs/en/i/7.3?topic=area-field-descriptions).

[ASNA.QSys.Runtime](/concepts/architecture/asna-qsys.html) implements RPG [SQLCA](https://www.ibm.com/docs/en/i/7.3?topic=reference-sqlca-sql-communication-area) by populating the [SQL_CommunicationsArea](program-sql-communications-area-class.html).

>Note: In addition to the [SQLCA](https://www.ibm.com/docs/en/i/7.3?topic=area-field-descriptions) defined fields, [SQL_CommunicationsArea](/reference/runtime/qsys-runtime-job-support/sql-communications-area.html) provides [SQL_Exception](/reference/runtime/qsys-runtime-job-support/sql-communications-area.html#properties) giving access to the raw [.NET SqlClientException](https://learn.microsoft.com/en-us/dotnet/api/system.data.sqlclient.sqlexception?view=dotnet-plat-ext-8.0) instance.
