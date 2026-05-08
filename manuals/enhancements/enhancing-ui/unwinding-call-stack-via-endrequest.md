---
title: "Unwinding the Call Stack via EndRequest"
description: "Master the technique of unwinding the call stack using EndRequest for cleaner, more efficient code execution in your applications."
---

## Introduction
Monarch Base defines the exception `ASNA.QSys.Runtime.EndRequestException` which can be used to orderly unwind an activation stack of program calls. 

The EndRequest exception is monitored within the CallD (Dynamic Call) infrastructure, when the exception is seen, CallD deactivates the called program and bubbles up the exception through the activation call stack.  

A program can also monitor for the EndRequest exception and handle it in any way it desires.  A program can throw the EndRequest exception to 'return' to a program in the call stack that is monitoring for the exception.  All the programs between the monitoring program and the throwing program will be deactivated when the exception is thrown.

In addition to a program throwing the exception, Monarch Base provides two other mechanisms that can be used to rise the exception from the website of an interactive job:
 + The JavaScript pushKey method to initiate from the browser.
 + The PushEndRequest method to initiate it from a page's model.

 These facilities can be employed to allow a user to end a particular process and return to a known point in an application, like a menu screen, or to start a different process.

 > **_NOTE:_** Not every program can be ended abruptly without compromising the work it was performing.  Use the EndRequest facility judiciously.



## Some Code
For the following discussion, please see first the topics [Enhancing Applications using Non-Display File Pages](enhancing-with-non-display-file.html) and [Calling a Program from a Non-DisplayFile Page](calling-program-from-non-displayfile-page.html). In the latter topic, a 'regular' Razor Page (Minutes) is used as a menu on the website where different programs are called via the [Command.Call](reference/asna-qsys-expo/expo-model/command.html#callstring-string-string-string) method while the Job awaited for commands via the [AcceptCommands](/reference/runtime/qsys-runtime-job-support/interactive-job.html#string-acceptcommands) method.

## Returning to a Menu

Assume an application which wants to present a regular Razor Page as its menu.  The menu page will determine what program is to be invoked and will do so via the Command.Call() method.  The application's Job will have to be ready to accept commands so that the program call can take effect.  Furthermore, the application will provide a button on some screens allowing the user to click on it to go back to the menu effectively ending whatever process had been initiating via the last menu option invoked.

### On the Job

The job will call [AcceptCommands](/reference/runtime/qsys-runtime-job-support/interactive-job.html#string-acceptcommands) in a loop so that it can continue  processing commands even after receiving an EndRequest exception.

```cs
    ...
    MyDatabase.Open();
    bool EndRequestReceived;
    do
    {
        EndRequestReceived = false;
        try
        {
            returnValue = AcceptCommands();
        }
        catch (EndRequestException e)
        {
            EndRequestReceived = true;
            ReclaimResources();
        }
    } while (EndRequestReceived);
    ...
```

### On the Website

Let's start by assuming that all the display file Razor Pages will use a common `_Layout.cshtml` file and that all of them will allow their process to be interrupted via EndRequest.  We could add the following code to `_Layout.cshtml` to show a button for the user to press.

```cs
<body>
    <button type="button" onclick="window.asnaExpo.page.pushKey('EndRqs')">Go To Menu</button>
    @RenderBody()
    ...
```

The `pushKey()` JavaScript function simulates a user pressing a function key; The 'EndRqs' is a special key that will be interpreted by the Monarch Base display file handler as a petition to throw the `EndRequest` exception.  When the user presses the button, the exception will be thrown on the Job's blue thread and the program that had presented the current screen will terminate along with all the programs in the call stack until execution reaches back to `AcceptCommands` which will also throw the `EndRequest` exception. The `catch` in the job's loop will process the exception and invoke again `AcceptCommands` to process any future commands from the menu.

#### Allowing only some pages to be ended
If we only wanted some of the pages to include the button with the `pushKey` code, we could control its presentation with some flag in the `ViewData` collection and have in `_Layout.cshtml` this code:
```cs
<body>
    @if ((string)ViewData["AllowEndRequest"] == "Y")
    {
        <button type="button" onclick="window.asnaExpo.page.pushKey('EndRqs')">Go To Menu</button>
    }
    @RenderBody()
    ...
```

If most of the pages would allow the 'Go to Menu' button, then the _ViewStart.cshtml could default the flag to 'Y' like this:
```cs
@{
    Layout = "_Layout";
    ViewData["AllowEndRequest"] = "Y";
}
```

and then individual pages could disable the button by setting the flag to 'N' like this:
```cs
@page
@model DSPFXYZ
@{
    ViewData["Title"] = "DSPFXYZ";
    ViewData["AllowEndRequest"] = "N";
}
...
```

### Starting EndRequest in the Model

It is also possible to initiate an EndRequest from the code behind in a Page's Model; to do so use the method `PushEndRequest` from the [Command](/reference/expo/qsys-expo-model/command.htmll#void-pushendrequest) class.

For this scenario, assume there are some programs that can allow the user to end the processing on their current screen and 'jump' to a different program of the application, for example the employee directory program.

Using the same technique as above, the `_Layout.cshtml` could include code like this:
```cs
<body>
    @if ((string)ViewData["AllowEmployeeDirectory"] == "Y")
    {
        <button type="button" onclick="location.href='/Switch?Option=1'">Go To Employee Directory</button>
    }
    @RenderBody()
    ...
```

Notice how this time the button allows the user to redirect the browser to a `Switch` page with an option of '1'.

The Switch page can PushEndRequest() in the OnGet method and follow it with a call to the Employee Directory program.  The following code assumes the same website structure where programs are called by the menu page 'Minutes' discussed [here](https://asnaqsys.github.io/manuals/migrations/calling-program-from-non-displayfile-page.html#minutus).

The code only shows the handling of options '1' and '5' as an example of calling a program or having the Job return out of `AcceptCommands`.

```cs
using System;
using ASNA.QSys.Expo.Model;
using Microsoft.AspNetCore.Http;
using Microsoft.AspNetCore.Mvc;
using Microsoft.AspNetCore.Mvc.RazorPages;
using Microsoft.Extensions.Configuration;

namespace CustAppSite.Pages
{
    [BindProperties]
    public class SwitchModel : PageModel
    {
        int __ASNA_JobHandle__ = 0;

        public IActionResult OnGet()
        {
            var command = Command.GetCommandFromRequest(HttpContext);
            while (!command.JobStarted)
                System.Threading.Thread.Sleep(100);

            try
            {
                command.PushEndRequest();
            }
            catch (RedirectedException redirect)
            {
                if (string.Compare(redirect.NewUrl, "/Minutes", StringComparison.OrdinalIgnoreCase)==0)
                {
                    // we don't need to redirect, this page just got poped from the 'return to pages' stack
                }
            }

            try
            { 
                IConfiguration config = (IConfiguration)HttpContext.RequestServices.GetService(typeof(IConfiguration));
                var section = config.GetSection("JobDescriptor");
                string AssemblyPath = section["AssemblyPath"];
                int option = 0;
                int.TryParse(Request.Query["Option"], out option);
                int.TryParse(Request.Query["JobHandle"], out __ASNA_JobHandle__);
                switch (option)
                {
                    case 1:
                        {
                            command.Call(AssemblyPath, "Acme.ERCAP.EMPDIR", Array.Empty<string>(), "/Minutus");
                            break;
                        }
                    // . . . 
                    case 5:
                        {
                            command.Return("proceed");
                            break;
                        }
                }
            }
            catch (RedirectedException redirect)
            {
                return RedirectToResult(redirect);
            }
            return Page();
        }

        IActionResult RedirectToResult(RedirectedException WhereTo)
        {
            string newUrl = WhereTo.NewUrl.TrimStart();
            if (newUrl.StartsWith("/Monarch/"))
            {
                newUrl = newUrl.Replace("\n", "\\n");
                newUrl = newUrl.Replace("\r", "\\r");
                return Redirect(newUrl);
            }

            QSysRoute route = new QSysRoute(WhereTo.NewArea, __ASNA_JobHandle__);
            return RedirectToPage(newUrl, route);
        }
    }
}

```

## Calling an Arbitrary Program
A generic facility can be created to call a program and pass parameters to it by providing a URL to the facility.  This URL would contain the name of the program and the parameters to pass.  

Assume the facility is implemented in a Razor Page called _Restart_.

When _Restart_ is called it ends the current request, something that, as mentioned earlier may not be wholesome to any program. Caution has to be taken to allow the call to _Restart_ only when the user transaction can be interrupted, use judiciously.  After ending the current request, _Restart_ calls the program indicated to it passing the parameters found in the Query string.

The sample facility is called _Restart_ instead of _Call_ or _Invoke_ to stress the fact that _Restart_ ends the current transaction before doing the call to the new program.

### Using _Restart_
Here is an example of how to call _Restart_ from an arbitrary page, the example uses links but they could be substituted with whatever other element you may need:

```html
   <a href='/Restart/CUSTINQ?CustNum=10300'>Details of customer 10300</a> <br />
   <a href='/Restart/ORDHINQ?CustNum=10300'>Orders for customer 10300</a> <br />
   <a href='/Restart/CUSTPRMPT?mode="SFSTATE"&current="TX"'>Available States and Provinces</a> <br />
   <a href='/Restart/CUSTPRMPT?field="SFSTATUS"&selector="A"'>Available Status</a> <br />
```
In this prototype, parameters are passed positionally, the name used in the query string is irrelevant. Notice for instance that the last two links are calling the same program, `CUSTPRMPT`, but one of them calls the first parameter `mode` while the other one calls it `field`. In either case the first parameter will be passed as parameter number 1 to `CUSTPRMPT`.

The MyJob’s `ExecuteStartupProgram` method (or any other suitable place) has to have a loop similar to the one shown [on the job](#on-the-job).

### Restart.cshtml 
This is the contents of the Restart.cshtml markup:
```html
@page "{programName}"
@model CustAppSite.Pages.RestartModel
@{ ViewData["Title"] = "Restart"; }

<div style="padding:1em">
    <form method="post">
        <h1>You should not be here!</h1>
    </form>
</div>
```

Don’t miss the first line on the Restart.cshtml markup:

```    @page "{programName}"```

Using this syntax tells ASP.NET to take the URL segment after the page’s name and pass it to Get() as a parameter.

### Restart.cshtml.cs 
```cs
using System;
using ASNA.QSys.Expo.Model;
using Microsoft.AspNetCore.Http;
using Microsoft.AspNetCore.Mvc;
using Microsoft.AspNetCore.Mvc.RazorPages;
using Microsoft.Extensions.Configuration;

namespace CustAppSite.Pages
{
    [BindProperties]
    public class RestartModel : PageModel
    {
        int __ASNA_JobHandle__ = 0;

        public IActionResult OnGet(string programName)
        {
            // Ensure Job is up and running
            var command = Command.GetCommandFromRequest(HttpContext);
            while (!command.JobStarted)
                System.Threading.Thread.Sleep(100);

            // End any previous request, collapsing the call stack
            try
            {
                command.PushEndRequest();
            }
            catch (RedirectedException redirect)
            {
                if (string.Compare(redirect.NewUrl, "/Minutes", StringComparison.OrdinalIgnoreCase) == 0)
                {
                    // we don't need to redirect, this page just got popped from the 'return to pages' stack
                }
            }

            // Get parameters sent on the Query String
            IConfiguration config = (IConfiguration)HttpContext.RequestServices.GetService(typeof(IConfiguration));
            var section = config.GetSection("JobDescriptor");
            string AssemblyPath = section["AssemblyPath"];

            string[] parms = new string[Request.Query.Count];
            int i = 0;
            bool hasJobHandle = false;
            foreach (var p in Request.Query)
            {
                string parm = p.Value;
                parm = parm.Trim('"');
                if (p.Key == "JobHandle")
                {
                    hasJobHandle = true;
                    __ASNA_JobHandle__ = int.Parse(parm);
                }
                else
                {
                    parms[i++] = parm;
                }
            }
            if (hasJobHandle)
            {
                Array.Resize<string>(ref parms, parms.Length-1);
            }

            // Call requested program
            try
            {
                command.Call(AssemblyPath, "Acme.ERCAP."+ programName, parms, "/Minutus");
            }
            catch (RedirectedException redirect)
            {
                return RedirectToResult(redirect);
            }
            return Page();
        }

        IActionResult RedirectToResult(RedirectedException WhereTo)
        {
            string newUrl = WhereTo.NewUrl.TrimStart();
            if (newUrl.StartsWith("/Monarch/"))
            {
                newUrl = newUrl.Replace("\n", "\\n");
                newUrl = newUrl.Replace("\r", "\\r");
                return Redirect(newUrl);
            }

            QSysRoute route = new QSysRoute(WhereTo.NewArea, __ASNA_JobHandle__);
            return RedirectToPage(newUrl, route);
        }
    }
}
```
