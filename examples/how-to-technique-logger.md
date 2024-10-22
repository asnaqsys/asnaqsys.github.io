---
title: "Effective Logging Techniques Guide"
description: "Master the art of logging with our guide. Learn best practices, tools, and techniques to enhance your application's logging strategy."
---

Visual Studio has a sophisticated [Output Window](https://docs.microsoft.com/en-us/visualstudio/ide/reference/output-window) where lots of messages are displayed as the Application executes.

During ASNA.QSys Application Debugging, it is desirable to display field values or complete dumps of records in a place where this information can be isolated from the rest of ASP.NET Core.

The following technique shows how we can Log Application information to an external text file for reference.

Add the following class to a file in one of your Logic Projects.

A good name for the C# file may be `ProgramLogger.cs`: 

```cs
using System;
using ASNA.DataGate.Client;
using System.Data;
using System.IO;
using System.Diagnostics;
using System.Runtime.CompilerServices;
using ASNA.QSys.Runtime;

class ProgramLogger
{
    static private string LOG_PATHNAME = "Trace.log"; // May be a pathname like: @"C:\Projects\TraceOutput\Trace.log";

    //
    //  Extract Source filename, method and line number (uses System.Runtime.CompilerServices)
    //
    public static string Label(string text,
                    [CallerFilePath] string file = "",
                    [CallerMemberName] string member = "",
                    [CallerLineNumber] int line = 0)
    {
        return $"{Path.GetFileName(file)} {member}:{line} *** {text} ***";
    }

    private static TextWriterTraceListener OpenLogFile(string entryTitle)
    {
        TextWriterTraceListener trace = new TextWriterTraceListener(LOG_PATHNAME, "ASNA.QSys.Listener");

        trace.WriteLine(string.Empty);
        trace.WriteLine($"{DateTime.Now.ToLongTimeString()} {entryTitle}");
        return trace;
    }

    private static void CloseLogFile(TextWriterTraceListener trace)
    {
        trace.Flush();
        trace.Close();
    }

    public static void Message(string entryTitle)
    {
#if DEBUG
        TextWriterTraceListener trace = OpenLogFile(entryTitle);
        CloseLogFile(trace);
#endif
    }

    public static void DumpWorkstationRecordFormat(WorkstationFile workstationFile, string recordFormatName, string entryTitle)
    {
#if DEBUG
        TextWriterTraceListener trace = OpenLogFile(entryTitle);

        trace.Write($"Workstation [{recordFormatName}]");

        AdgDataSet dataSet = workstationFile.DataSet;
        try
        {
            AdgTable table = dataSet[recordFormatName];

            trace.WriteLine($" Records:{table.DataTable.Rows.Count}");

            foreach (DataColumn col in table.DataTable.Columns)
            {
                trace.Write($"{col.ColumnName} |");
            }
            trace.WriteLine(string.Empty);
            int rrn = 0;
            foreach (DataRow row in table.DataTable.Rows)
            {
                trace.Write($"{rrn}:");
                foreach (object item in row.ItemArray)
                {
                    trace.Write(item);
                    trace.Write("|");
                }
                trace.WriteLine(string.Empty);
                rrn++;
            }

        }
        catch { }

        CloseLogFile(trace);
#endif
    }
}
```

At any method in your Logic Application code, you may want to add `Debug Log` lines such as:

```cs
using Log = ProgramLogger; // Shorthand "alias"

namespace MyCompany.MyApplication
{
    public partial class MyProgram : Program
    {
        .
        .
        .

        Log.Message(Log.Label("Page Down Requested"));

        .
        .
        .

        Log.DumpWorkstationRecordFormat(MYDSPF, "SFL1", Log.Label("Before writing to subfile"));

        .
        .
        .

        Log.DumpWorkstationRecordFormat(MYDSPF, "SFL1", Log.Label("After writing to subfile"));
}
```

When the `Log` static method(s) calls execute, a text file named `Trace.Log` will be created (in current directory).

>You can open the `Trace.Log` on an editor that may automatically loads the file as it changes, and you can see the logged information.

When the Application terminates, the `Trace.Log` remains for future reference. (To clear it, delete the file at any time).

Here is an example of a run, using this technique:

```

6:39:44 PM CUSTINQ.cs LoadSfl:534 *** Before writing to subfile ***
Workstation [SFL1] Records:0
SFCOLOR |SFSEL |SFCUSTNO |SFNAME1 |SFCSZ |*Direction |*Indicators |*ResponseIndicators |

6:39:44 PM CUSTINQ.cs LoadSfl:563 *** After writing to subfile ***
Workstation [SFL1] Records:14
SFCOLOR |SFSEL |SFCUSTNO |SFNAME1 |SFCSZ |*Direction |*Indicators |*ResponseIndicators |
0:G|0|64000|Advantage Ranch Manufacturing Inc       |Somersworth, AR 03878    |O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
1:W|0|29400|Advertising Agricultural 2nd Day        |Bryan, OH 43506          |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
2:G|0|48100|Advertising Electric                    |Gillette, AL 82716       |O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
3:W|0|68100|Advertising Murray Ltd                  |Palo Alto, CA 94303-0000 |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
4:G|0|86400|Agency Way Loans                        |Merryville, TN 37801-3748|O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
5:W|0|64700|Aims Analysis Group Singapore           |Wilkes-barre, PA 18701   |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
6:G|0|99500|Aims College Corp Company               |Fairmont, MN 56031       |O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
7:W|0|82600|Aims Group Berry Compositing            |New York, AS 10004       |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
8:G|0|25300|Aims Management Data                    |Orlando, FL 32832        |O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
9:W|0|17100|Akashic City Insurance                  |Cleveland, OH 45202      |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
10:G|0|19300|Akzo Allyn Inc Co                       |Tucson, AZ 85713         |O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
11:W|0|80600|Akzo Of Maine                           |Sanford, ME 04073        |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
12:G|0|59700|Akzo Sign Systems Co                    |Dalton, GA 30720         |O|0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
13:W|0|50500|Alamo Elias Board Overland              |Greensboro, NC 27407     |O|0000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|

6:39:50 PM CUSTINQ.cs StarEntry:148 *** Page Down Requested ***

6:39:50 PM CUSTINQ.cs LoadSfl:534 *** Before writing to subfile ***
Workstation [SFL1] Records:0
SFCOLOR |SFSEL |SFCUSTNO |SFNAME1 |SFCSZ |*Direction |*Indicators |*ResponseIndicators |

6:39:50 PM CUSTINQ.cs LoadSfl:563 *** After writing to subfile ***
Workstation [SFL1] Records:14
SFCOLOR |SFSEL |SFCUSTNO |SFNAME1 |SFCSZ |*Direction |*Indicators |*ResponseIndicators |
0:G|0|92000|Alexvale Danek Noble Incorporated Mfg   |Pompano Beach, IL 33064  |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
1:W|0|10100|Alexvale Investments Publishing         |Rumford, RI 02916        |O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
2:G|0|92100|Allegiance York Center Canada Div       |West Hazleton, PA 18201  |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
3:W|0|17300|Allied Inc                              |Scottsboro, AL 35768     |O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
4:G|0|17600|Allstate C Associates Corp.             |St Louis, MO 63127       |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
5:W|0|80200|Allstate California Telephone           |Smyrna, TN 37167         |O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
6:G|0|95900|Allstate M Technology Hq Services       |Elmhurst, IL 60126-0000  |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
7:W|0|52100|Amco Capitol Services                   |Minneapolis, MN 55404    |O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
8:G|0|84900|America School Industries               |Mississauga, Ontario, CA |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
9:W|0|49100|American Computong Carrier Insurance Inc|Hialeah, FL 33014        |O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
10:G|0|14500|American Insurance Writers              |Memphis, TN 38134        |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
11:W|0|33200|Ameritech Co Robins Inc                 |City Of Industry, CA 9174|O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
12:G|0|25700|Ames Foods Corp                         |Milwaukee, WI 53223      |O|0000000000000000000000000000000000000000000000000010000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
13:W|0|64800|Ames Furniture Bank Systems             |Winchester, VA 22601     |O|0000000000000000000000000000000000000000000000000010000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|

6:39:54 PM CUSTINQ.cs StarEntry:165 *** Page Up Requested ***

6:39:54 PM CUSTINQ.cs LoadSfl:534 *** Before writing to subfile ***
Workstation [SFL1] Records:0
SFCOLOR |SFSEL |SFCUSTNO |SFNAME1 |SFCSZ |*Direction |*Indicators |*ResponseIndicators |

6:39:54 PM CUSTINQ.cs LoadSfl:563 *** After writing to subfile ***
Workstation [SFL1] Records:14
SFCOLOR |SFSEL |SFCUSTNO |SFNAME1 |SFCSZ |*Direction |*Indicators |*ResponseIndicators |
0:G|0|64000|Advantage Ranch Manufacturing Inc       |Somersworth, AR 03878    |O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
1:W|0|29400|Advertising Agricultural 2nd Day        |Bryan, OH 43506          |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
2:G|0|48100|Advertising Electric                    |Gillette, AL 82716       |O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
3:W|0|68100|Advertising Murray Ltd                  |Palo Alto, CA 94303-0000 |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
4:G|0|86400|Agency Way Loans                        |Merryville, TN 37801-3748|O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
5:W|0|64700|Aims Analysis Group Singapore           |Wilkes-barre, PA 18701   |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
6:G|0|99500|Aims College Corp Company               |Fairmont, MN 56031       |O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
7:W|0|82600|Aims Group Berry Compositing            |New York, AS 10004       |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
8:G|0|25300|Aims Management Data                    |Orlando, FL 32832        |O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
9:W|0|17100|Akashic City Insurance                  |Cleveland, OH 45202      |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
10:G|0|19300|Akzo Allyn Inc Co                       |Tucson, AZ 85713         |O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
11:W|0|80600|Akzo Of Maine                           |Sanford, ME 04073        |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
12:G|0|59700|Akzo Sign Systems Co                    |Dalton, GA 30720         |O|0000000000000000000000000000000000000000000000000001000000000000000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
13:W|0|50500|Alamo Elias Board Overland              |Greensboro, NC 27407     |O|0000000000000000000000000000000000000000000000000001000000000100000000000001000000000000000000000000|xxx0xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx|
```


## Using Windows PowerShell

An alternative to using a full-editor to watch the Logger messages, is to use [Windows PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/overview).

If you open a `PS` window, and issue the command `Get-Content` using the `-Wait` option, you can display the Log file as soon as it changes.

```
Get-Content "Trace.log" -Wait
```

Furthermore, you can combine with option `-Tail`, to only display the **last** `(n)` lines from the end of the file:

```
Get-Content "Trace.log" -Tail 10 -Wait
```



## Customizing Log output
`ProgramLogger` is a small class, that can be studied and tailored to your needs. 