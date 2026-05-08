---
title: "Running Multiple Jobs from a Single Browser"
description: "Learn how to efficiently run multiple jobs in a single browser. Maximize productivity with our expert tips and tricks for seamless multitasking."
---

The `DisplayPages` section of the [website configuration](configure-expo-website.html#displaypages) provides the ability to decide the relationship of multiple tabs on a browser with the user jobs. 

Enabling the `MultiJobOnBrowser` property (setting it to true) allows a user to employ a single browser to start multiple jobs in different tabs. When the property is disabled (set to false), all the tabs on the user browser will display the state of the single job started on the first browser tab.

## The Mechanics
When a user request is received by the web server, it is necessary to associate that request with the user's job via a job number or handle.  

### One Job per Browser
To run a single job per browser set `MultiJobOnBrowser` to false
```json
    "DisplayPages": {
      "MultiJobOnBrowser": "false",
      . . .
    },
```

For websites configured to run a single job for all the tabs of a browser, the job number is stored in the ASP.NET Core Session object. 

### One Job per Tab
To run a different job on each of a browser's tab, set `MultiJobOnBrowser` to true
```json
    "DisplayPages": {
      "MultiJobOnBrowser": "true",
      . . .
    },
```

When the configuration states that each tab should be associated with its own job, then the Session object can't be used because ASP.NET Core has a single Session object for all the browser tabs.

> ASP.NET Core does [not support cookieless](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/app-state?view=aspnetcore-7.0#:~:text=replacement%20for%20the-,cookieless%20session,-feature%20from%20the) Sessions.

#### The Job Handle
For websites configured to run multiple jobs, the Job Handle that is used to identify the job associated with each tab is kept as a hidden field in the Display Page Form with the name of `__ASNA_JobHandle__`.  When there is the need to redirect from one Display Page to a different one, the redirect response sent to the browser includes a query string with the parameter `JobHandle` set to the Job Handle.

#### Beware of the ASP.NET Core Session
If your web pages need to keep data on a per-job basis, beware that you are not able to use the [Session](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/app-state) object to store data specific to each job as the Session is shared amongst all tabs.  Also note that the [Session state is not-locking](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/app-state?view=aspnetcore-7.0#:~:text=Session%20state%20is%20non%2Dlocking).  If two request for the same session are processed simultaneously, changes to the Session done by one request may be overridden by the other request.
 
 To assist in the keeping of data on a per-job basis, Monarch provides the  [JobSession](/reference/expo/qsys-expo-model/job-session.html) facilities which you can use.


