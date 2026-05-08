---
title: "Showing a Non-DisplayFile Page"
description: "Learn how to show Non-DisplayFile Page in your application without using display files, enhancing flexibility and user interface design."
---

## On the Job (Blue Thread)

To display an arbitrary page use the ShowPage method of the InteractiveJob class. :

```cs
    string returnValue = (CurrentJob as InteractiveJob).ShowPage("https://www.time.gov/");
```    

The following example shows how to 'call' a page of the website from a program within a Job.  

```cs
    string returnValue = (CurrentJob as InteractiveJob).ShowPage("/Presenter", "23, ABC, Train");
    . . . 
```

## On the Page (Yellow thread)
On the previous example, the browser would be redirected to the *Presenter* page after storing the SHowPage() parameter in the session.  Here is what Presenter could have on its OnGet() method to use the stored parameter:

```cs
    public int CustomerNumber    { get; private set; }
    public string Destination    { get; private set; }
    public string Transportation { get; private set; }
    public string InternalError  { get; private set; }

    public void OnGet()
    {
        string parameter = HttpContext.Session.GetString("ASNA_MonarchCommandParm");
        HttpContext.Session.SetString("ASNA_MonarchCommandParm", "");

        // Validate that we got to this page due to a ShowPage request from the Job
        if (string.IsNullOrEmpty(parameter))
        {
            InternalError = "Page Request Out Of Sequence";
            return;
        }

        // Now parse out the parameters for the presenter and ensure we got correct number
        string[] aParameters = parameter.Split(',');
        if (aParameters.Length < 3)
        {
            InternalError = $"Expecting at least 3 Parameters but received {aParameters.Length}";
            return;
        }

        CustomerNumber = int.Parse(aParameters[0]);
        Destination = aParameters[1].Trim();
        Transportation = aParameters[2].Trim();
    }

```

> Notice how OnGet() uses the parameter stored in session as an indication that the page was requested by a program and was not arbitrarily navigated to it by the user typing the URL on the browser address bar.

Once the users finish using the non-displayfile pages, a mechanism should be given to them to return to the procedural programs of the job.

The example does this by including a button on the *Presenter* page which will cause a postback to the same page.

```cs
    <form method="post">
        <h1>Here is an important announcment.</h1>

        @{
            if (!string.IsNullOrEmpty(Model.InternalError))
            {
                <span class="text-danger">@Model.InternalError</span>
            }
            else
            {
                <table>
                    <tr> <td>Customer Number </td><td>@Model.CustomerNumber</td>  </tr>
                    <tr> <td>Destination     </td><td>@Model.Destination</td>     </tr>
                    <tr> <td>Transportation  </td><td>@Model.Transportation</td>  </tr>
                </table>
                <p class="actions">
                    <button class="btn proceed-button">Proceed</button>
                </p>
            }
        }

    </form>
```

The OnPost() of Presenter could look like this:

```cs
        public IActionResult OnPost()
        {
            try
            {
                ASNA.QSys.Expo.Model.Command command = new ASNA.QSys.Expo.Model.Command(HttpContext);
                command.Return("proceed");
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
            if (WhereTo.NewArea == null)
            {
                if (newUrl.StartsWith("//") || newUrl.IndexOf("://") <= 5)      // URL is // or similar to http:// or https://
                    return RedirectPreserveMethod(newUrl);                      //  Redirect to page outside of our website

                return RedirectToPage(newUrl);  // equivalent to providing ( new { area = "" } ) as a second parameter
            }

            return RedirectToPage(newUrl, new { area = WhereTo.NewArea });
        }
```

## Back on the Job
The program had been waiting on the ShowPage() method serving requests from the Yellow thread, in our case the only request was the Return() command.  When Presenter called Return() it passed a value of "proceed".  This could be processed by the program as follows:

```cs
    string returnValue = (CurrentJob as InteractiveJob).ShowPage("/Presenter", "23, ABC, Train");
    if (returnValue == "proceed")
        DynamicCaller_.CallD("Acme.Bookit", out _LR);
    . . .
```

