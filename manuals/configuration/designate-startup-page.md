---
title: "Designate a Startup Page"
description: "Establish a Razor Page, or route, as the one to execute to start a Job."
---

When a DisplayPage `Get` request is received, Expo attempts to locate the Job associated with the user's session; if no Job is found, Expo automatically creates one and associates it with that session.

You can [configure a route or Startup Page](configure-expo-website.html#displaypages) to be the one that starts the Job with your own custom logic. This enables you to perform tasks such as establishing credentials, creating claims, initializing session state, or validating access before the Job is created or to provide values to the Job during startup.

In order to customize the Job startup you will have to make provisions on the [website and job class](/concepts/architecture/application-architecture.html#interactive-job-architecture). 

## On The Job
In most cases the need to have custom code to start a job is caused by having to pass some values to the job from the website at startup time. The easiest way of accomplishing this is by having the job enter the [Accepting Commands](/manuals/enhancements/enhancing-ui/enhancing-with-non-display-file.html#accepting-commands) state; this is achieved by invoking the AcceptCommands method on the InteractiveJob. Here is an example on the MyJob class:

```cs
override protected void ExecuteStartupProgram()
{
    . . .

    string result = AcceptCommands();
    if (result != "OK")
       return;

    string UserName = CurrentJob.LDC["UserName"] as string;
    MyDatabase.Open();
    . . . 

    _DynamicCaller.CallD("FirstPgm, out _LR);

    . . .

}
```

In the code above, the Job enters the Accept Command state as soon as it starts.  It will process any commands sent from the web site until it receives the command to Continue normal execution, at that point the Job could open its database connection if it hadn't, and do any other setup needed to call the entry program.

## On The Website

### Configure PageStartup

The first order of business is to designate the route to the StartupPage, for example, you could point to a Razor Page called `Entry` located at the website's root, something like this:

```json
    "DisplayPages": {
      "StartupPage": "/Entry",
      . . .
    },
```

When `StartupPage` has a non-empty value and there is no Job for a user, Expo will reroute any HTML `Get` requests issued to any DisplayPage derived to the designated route, effectively any migrated Display File page that get's requested before the Job is started will reroute to the startup page.

### Starting the Job in Startup Page

The startup page is responsible for starting the Job. A common process to start the job includes the following steps on the OnGet method of the page:
  - Verify that a Job does not exists for the user
  - Start the Job
  - Perform any desired setup
  - Issue a Return command to the Job and redirect to the Job's requested page

Here is an example of a simple startup implementation of the model for a page called `Entry`:

```cs
    [Authorize]
    public class EntryModel : PageModel
    {
        public IActionResult OnGet()
        {
            int __ASNA_JobHandle__ = Command.GetRequestJobHandle(HttpContext);
            Command command = new Command(HttpContext, __ASNA_JobHandle__);
            if (!command.JobStarted)
            {
                __ASNA_JobHandle__ = command.StartJob();

                string userName = "";
                System.Security.Claims.ClaimsPrincipal user = HttpContext?.User;
                if (user != null && user.Identity is WindowsIdentity windowsIdentity)
                    userName = windowsIdentity.Name;

                command.SetLdcObject("UserName", userName);
                
                try
                {
                    command.Return("OK");
                }
                catch (RedirectedAbEndException AbnormalTermination)
                {
                    return redirectToAbEnd(AbnormalTermination);
                }
                catch (RedirectedException WhereTo)
                {
                    if (WhereTo.NewArea == null)
                        return RedirectToPage(WhereTo.NewUrl);
                    return RedirectToPage(WhereTo.NewUrl, new { area = WhereTo.NewArea });
                }
            }
            return Page();
        }

        private IActionResult redirectToAbEnd(RedirectedAbEndException abEndException)
        {
            ViewResult v = new ViewResult();
            v.ViewName = "/Pages/Monarch/AbEnd. cshtml";
            v.ViewData = this.ViewData;
            v.ViewData.Add("ASNA_AbEndMessage", abEndException.AbEndMessage);
            v.ViewData.Add("ASNA_AbEndStack", abEndException.AbEndStack);
            return v;
        }
    }
```

## See Also
See how to [configure the expo website](configure-expo-website.html).

For more information on using the [Command class](../../reference/expo/qsys-expo-model/command.html) see [this example](/manuals/enhancements/enhancing-ui/calling-program-from-non-displayfile-page.html).

