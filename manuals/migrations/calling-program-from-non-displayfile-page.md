---
title: Calling a Program from a Non-DisplayFile Page

---

## On The Job
To prepare a Job to receive Call requests from the website it is necessary to have it enter a cycle of accepting commands; this is achieved by invoking the AcceptCommands method on the InteractiveJob. Here is an example on the MyJob class:

```cs
override protected void ExecuteStartupProgram()
{
    MyDatabase.Open();
    AcceptCommands();
}
```

## On The Website
On the website we'll be making calls to programs on the Job.  Assume a menu is to be displayed as the first page of the website and let's call the menu Razor Page Minutus:

```cs
    services.AddRazorPages(razorOptions =>
    {
        razorOptions.Conventions.AddPageRoute("/Minutus", "");
    })
    ...
```

### Starting the Job
The website is responsible for starting the Job, we will do it in the Minutus Razor Page prior to presenting the menu to the user, this could be achieved by adding an OnGet() method to Minutus as follows:

```cs
public void OnGet()
{
    var command = new ASNA.QSys.Expo.Model.Command(HttpContext);
    if (!command.JobStarted)
    {
        command.StartJob();
        return;
    }
    . . .
}
```

### Calling a Program
The menu could present various options, we could add this to the OnPost() method of the Minutus page to handle the user selection:

```cs
public IActionResult OnPost()
{
    try
    {
        if (ModelState.IsValid)
        {
            IConfiguration config = (IConfiguration)HttpContext.RequestServices.GetService(typeof(IConfiguration));
            var section = config.GetSection("JobDescriptor");
            string AssemblyPath = section["AssemblyPath"];
            switch (Option)
            {
                case 1:
                    {
                        var command = new ASNA.QSys.Expo.Model.Command(HttpContext);
                        command.Call(AssemblyPath, "Acme.ERCAP.CUSTINQ", Array.Empty<string>(), "/Minutus");
                        break;
                    }

                . . . 

                case 0:
                    {
                        return RedirectToPage("/Monarch/EoJ");
                    }
            }

        }
    }
    catch (RedirectedException redirect)
    {
        return RedirectToResult(redirect);
    }
    return Page();
}

```

Let's digest the line:
```cs
    command.Call(AssemblyPath, "Acme.ERCAP.CUSTINQ", Array.Empty<string>(), "/Minutus");
```    

The `Call` method receives the path to the assembly containing the Program to be called as the first parameter, in this case we are retrieving the path from the configuration's file.  The second parameter is the fully qualified class name of the program.  Any parameters needed by the program are sent in an array of **strings**.  Finally, the last parameter is the Page where control should be passed when the execution of the program is completed; this parameter is only necessary for **interactive programs**.

Since the program we are calling, `CUSTINQ` is interactive, the `Call` method will rise an exception with the information needed to redirect the browser to the CUSTINQ's displayfile page.  We will handle this exception on the `RedirectToResult` method:

```cs
IActionResult RedirectToResult(RedirectedException WhereTo)
{
    string newUrl = WhereTo.NewUrl.TrimStart();
    if (WhereTo.NewArea == null)
    {
        return RedirectToPage(newUrl);
    }

    return RedirectToPage(newUrl, new { area = WhereTo.NewArea });
}
```

After `CUSTINQ` completes execution and has 'used' the browser's screen for its I/O with the user, Monarch will redirect the browser to the `Minutes` page as requested on the original `Call` request:

```cs
    command.Call(AssemblyPath, "Acme.ERCAP.CUSTINQ", Array.Empty<string>(), "/Minutus");
```    
### Passing Parameters
Let's look at an example of passing parameters to the called program. Say we want to add an option '2' to allow the user to call a program passing it a number, the program will use the parameter and return a new value on the way out.  Furthermore assume the program is interactive.  The OnPost() switch statement would have this new code:

```cs
                case 2:
                    {
                        string[] parms = new string[1];
                        parms[0] = CustomerNumber.ToString();
                        var command = new ASNA.QSys.Expo.Model.Command(HttpContext);
                        command.Call(AssemblyPath, "Acme.ERCAP.ORDHINQ", parms, "/Minutus");
                        break;
                    }
```
The `Call` method receives an array of strings to be passed as parameters to the program.  Eventhough the parameters are passed as strings, these are casted to the type of parameter defined by the Program as long as they are: strings, decimals, FixedStrings and FixedDecimals. 

Once the program returns, Monarch will redirect the browser back to /Minutes as requested on the `Call` method.  The values of the parameters returned by the program are concatenated into a single string, separated by newline characters, and stored into the session under a key of `"ASNA_MonarchCommandParm"`. These values can be retrieved as shown here:
```cs
        public void OnGet()
        {
            var command = new ASNA.QSys.Expo.Model.Command(HttpContext);
            if (!command.JobStarted)
            {
                command.StartJob();
                return;
            }

            string parameter = HttpContext.Session.GetString("ASNA_MonarchCommandParm");
            if (!string.IsNullOrEmpty(parameter))
            {
                HttpContext.Session.SetString("ASNA_MonarchCommandParm", "");
                CustomerNumber = decimal.Parse(parameter);
            }
        }

```

### Calling a Non-Interactive program
Calling non-interactive programs is simpler as it is not necessary to deal with the browser redirecting to display file pages and back to some other landing page.

In the following example we have added an option to call a program, which requires an character input parameter with a customer number, and to process the two values returned by the program.

```cs
                case 3:
                    {
                        string[] parms = new string[3];
                        parms[0] = CustomerNumber.ToString("000000000");
                        parms[1] = "0";
                        parms[2] = "0";
                        command.Call(AssemblyPath, "Acme.ERCAP.CUSTCALC", parms);
                        Sales = decimal.Parse(parms[1]);
                        Returns = decimal.Parse(parms[2]);
                        break;
                    }
```


### Driving an Interactive Program
It is possible to call an interactive program, but instead of letting it display its screen, capture the data in the display file and then feed it arbitrary data and function keys.  This process is achieved by the use of the `CallSilent` and `PushKeyFocus` methods as shown below.

```cs
                case 4:
                    {
                        WebDisplayFileProxy df = command.CallSilent(AssemblyPath, "Acme.ERCAP.CUSTINQ", Array.Empty<string>());
                        var recordRow = df.DataSet.Tables["SFLC"].Rows[0];
                        recordRow["SETNAME"] = "Interna";
                        recordRow["*Direction"] = "I";
                        df = command.PushKeyFocus(AidKeyIBM.Enter, 17, "SETNAME");
                        if (df.DataSet.Tables["SFL1"].Rows.Count > 0)
                        {
                            var subfileRecordRow = df.DataSet.Tables["SFL1"].Rows[0];
                            SimilarCustomer = subfileRecordRow["SFNAME1"].ToString();
                        }
                        // End CUSTINQ execution and take Job back to Accepting Commands.
                        df = command.PushKeyFocus(AidKeyIBM.F3, 0, "");
                        break;
                    }
```

There are a few things to consider when driving a program this way.  It is the responsibility of the website to directly populate the display file's dataset tables with whatever data is desired to be delivered to the program. Each record format in the display file has a corresponding data table in the dataset. In the example above we are setting the value of the SETNAME field of the SFLC record format.

Another consideration is the need to mark the record's row as being available to the program with input data.  This is effected by this line:
```cs
        recordRow["*Direction"] = "I";
```

 It is very important that the program must ends execution so that the Job goes back to the [**D**. Accepting Commands](enhancing-with-non-display-file.html#accepting-commands) state. In the example above this is effected by 'pushing' key F3 which is how the CUSTINQ program ends.  


## Minutus
Here is the complete code for Minutus.

### Minutus.cshtml
```cs
@page
@model CustAppSite.Pages.MinutusModel
@{ ViewData["Title"] = "Minutus"; }

<div style="padding:1em">
    <form method="post">
        <h1>Select on of the details.</h1>
        <p> <em>1 - Customer Maintenance.</em> </p>

        Provide a customer number for options 2 and 3.
        <label asp-for="CustomerNumber" />
        <input asp-for="CustomerNumber" />

        <p><em>2 - Orders for Customer </em></p>

        <p><em>3 - Sales & Returns for Customer </em> </p>
        @if (@Model.Sales >= 0)
        {
            <p>
                <span>Sales = @Model.Sales Returns=@Model.Returns</span>
            </p>
        }

        <p> <em>4 - Harvest Screen.</em> </p>
        @if (@Model.SimilarCustomer != null)
        {
            <p>
                <span>Customer similar to 'Interna' is '@Model.SimilarCustomer'</span>
            </p>
        }
        <p> <em>5 - Proceed with normal job execution.</em> </p>
        <p> <em>0 - Exit.</em></p>
        <label asp-for="Option"></label>
        <input asp-for="Option" />

        <p class="actions">
            <button class="btn">Execute</button>
        </p>
    </form>
</div>
```

### Minutus.cshtml.cs

```cs
using System;
using System.ComponentModel.DataAnnotations;
using ASNA.QSys.Expo.Model;
using Microsoft.AspNetCore.Http;
using Microsoft.AspNetCore.Mvc;
using Microsoft.AspNetCore.Mvc.RazorPages;
using Microsoft.Extensions.Configuration;

namespace CustAppSite.Pages
{
    [BindProperties]
    public class MinutusModel : PageModel
    {
        [Range(0, 5)]
        public int Option { get; set; } = 2;

        [Range(10000, 99999)]
        public decimal CustomerNumber { get; set; } = 64000;

        public decimal Sales { get; private set; } = -1;

        public decimal Returns { get; private set; } = -1;

        public string SimilarCustomer { get; private set; }

        public void OnGet()
        {
            var command = new ASNA.QSys.Expo.Model.Command(HttpContext);
            if (!command.JobStarted)
            {
                command.StartJob();
                return;
            }

            string parameter = HttpContext.Session.GetString("ASNA_MonarchCommandParm");
            if (!string.IsNullOrEmpty(parameter))
            {
                HttpContext.Session.SetString("ASNA_MonarchCommandParm", "");
                CustomerNumber = decimal.Parse(parameter);
            }
        }

        public IActionResult OnPost()
        {
            try
            {
                if (ModelState.IsValid)
                {
                    var command = new ASNA.QSys.Expo.Model.Command(HttpContext);
                    while (!command.JobStarted)
                        System.Threading.Thread.Sleep(100);

                    IConfiguration config = (IConfiguration)HttpContext.RequestServices.GetService(typeof(IConfiguration));
                    var section = config.GetSection("JobDescriptor");
                    string AssemblyPath = section["AssemblyPath"];
                    switch (Option)
                    {
                        case 1:
                            {
                                // command.SetLdcObject("MyCookie1", "Oatmeal");
                                command.Call(AssemblyPath, "Acme.ERCAP.CUSTINQ", Array.Empty<string>(), "/Minutus");
                                break;
                            }
                        case 2:
                            {
                                string[] parms = new string[1];
                                parms[0] = CustomerNumber.ToString();
                                command.Call(AssemblyPath, "Acme.ERCAP.ORDHINQ", parms, "/Minutus");
                                break;
                            }
                        case 3:
                            {
                                string[] parms = new string[3];
                                parms[0] = CustomerNumber.ToString("000000000");
                                parms[1] = "0";
                                parms[2] = "0";
                                command.Call(AssemblyPath, "Acme.ERCAP.CUSTCALC", parms);
                                Sales = decimal.Parse(parms[1]);
                                Returns = decimal.Parse(parms[2]);
                                break;
                            }
                        case 4:
                            {
                                WebDisplayFileProxy df = command.CallSilent(AssemblyPath, "Acme.ERCAP.CUSTINQ", Array.Empty<string>());
                                var recordRow = df.DataSet.Tables["SFLC"].Rows[0];
                                recordRow["SETNAME"] = "Interna";
                                recordRow["*Direction"] = "I";
                                df = command.PushKeyFocus(AidKeyIBM.Enter, 17, "SETNAME");
                                if (df.DataSet.Tables["SFL1"].Rows.Count > 0)
                                {
                                    var subfileRecordRow = df.DataSet.Tables["SFL1"].Rows[0];
                                    SimilarCustomer = subfileRecordRow["SFNAME1"].ToString();
                                }
                                // End CUSTINQ execution and take Job back to Accepting Commands.
                                df = command.PushKeyFocus(AidKeyIBM.F3, 0, "");
                                break;
                            }
                        case 5:
                            {
                                command.Return("proceed");
                                break;
                            }
                        case 0:
                            {
                                return RedirectToPage("/Monarch/EoJ");
                            }
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
            string area = WhereTo.NewArea ?? "";
            return RedirectToPage(newUrl, new { area });
        }

    }
}
```

