---
title: "What's new in Monarch Base 4.0"
description: "Discover the latest updates in Version 4.0. This guide highlights new features, improvements, and how they benefit your projects."
---

The major new features on Monarch Base 4.0 are:
 * [Support for .NET 6.0](#support-for-net-60--70)
 * [Support for running multiple jobs from a single browser](#running-multiple-jobs-from-a-single-browser)
 * New [Context Menu](/reference/expo/qsys-expo-tags/dds-context-menu-tag-helper.html) tag helper
 * AssemblyList [configurable](/manuals/programming/programs-and-procedures/call-program.html#assembly-list) at the Website level
 * Program Call supports [Namespace List](/manuals/programming/programs-and-procedures/call-program.html#namespace-list) (Similar to Library List)


Other features include:
 * Change in the way keyboard errors are displayed; instead of a pop-up, they are being sent to the DdsMessagePanel location. The DdsMessagePanel should include a `class="dds-message-panel"`
 

Version 4.0 of ASNA.QSys.Expo is **not backwards compatible** with versions 3.x.  There are a few modifications for [upgrading websites](#upgrading-websites-from-3x) using Monarch Base 3.x to use version 4.0.


## Support for .NET 6.0 & 7.0
Monarch Base 4.0 is packaged with assemblies multitargeted for .NET 5.0 and .NET 6.0.  The 6.0 versions can also be used with .NET 7.0.

This multitargeting support is temporary and the .NET 5.0 assemblies will be eliminated at the end of spring 2023.

## Running Multiple Jobs from a Single Browser
To add support to your application for running multiple jobs, please read these articles:
 * [Running Multiple Jobs from a Single Browser](/manuals/configuration/multiple-jobs-one-browser.html)
 * [Configure Expo Website](/manuals/configuration/configure-expo-website.html)
 * [Enhancing Applications using Non-Display File Pages](/manuals/enhancements/enhancing-ui/enhancing-with-non-display-file.html)
 * [Calling a Program from a Non-DisplayFile Page](/manuals/enhancements/enhancing-ui/calling-program-from-non-displayfile-page.html)


## Upgrading Websites from 3.x

Before upgrading the Monarch Base NuGet packages to version 4.0, please read this section.

The following classes had some breaking changes:
 * The [Command](/reference/expo/qsys-expo-model/command.html) class had some method signature changes.
 * The [SessionStorage](/reference/expo/qsys-expo-model/session-storage.html) class lost several properties and methods.
 * The new class [JobSession](/reference/expo/qsys-expo-model/job-session.html) was added to replace or enhance the functionality of the previous two classes.

### Session Object
 There are also some values that version 3.0 used to save in the Session object that have been transferred to the JobSession class.  Of particular note is the value that used to be saved with key  `"ASNA_MonarchCommandParm"`. See the SessionStorage Class section below.

### Command Class
These signatures changed:
 * `Constructor` - The constructor requires now a JobHandle. To obtain a JobHandle for an existing job, you can use the new static method `GetRequestJobHandle`. You can also use the new factory method `GetCommandFromRequest` in lieu of using the constructor.
 * `StartJob` -  The `StartJob` method now returns the JobHandle of the started job.

There is a new method to `CommitJobSession`.


### SessionStorage Class

Some values that version 3.0 used to save in the Session object have been transferred to the [JobSession](/reference/expo/qsys-expo-model/job-session.html) class. 

The [SessionStorage](/reference/expo/qsys-expo-model/session-storage.html) class provides an ordered way of getting and setting values in the `ASP.NET Core` ISession collection.  Since the session storage is shared by all the Tabs on a user browser, the session is not a convenient place to store job related values. Monarch Base 4.0 provides the new class [JobSession](/reference/expo/qsys-expo-model/job-session.html) to facilitate the storage of job related items.  For this reason several properties and methods were lost from the SessionStorage class and 'transferred' to the [JobSession](/reference/expo/qsys-expo-model/job-session.html) class.

SessionStorage lost these properties:
 * `JobNumber` - Use the `Command.GetRequestJobHandle` to find a JobHandle instead.  For sites configured to run with a single job per browser, you can use the new `SingleJobNumber` property.
 * `EnabledKeys`
 * `OutsidePages`
 * `AbEndMessage`
 * `AbEndStack`
 
The following methods were removed:
 * `SetCmdParm`
 * `SetSessionBytes`
 * `GetSessionBytes`

 Additionally, the value that used to be saved with the key  `"ASNA_MonarchCommandParm"` has been removed and transferred to the `JobSession.CommandParm` property.

### Your Non-Display File Pages
Any usage of the methods or properties mentioned above will required changes to your non-display file pages.  It is useful to go thru the description on [Calling a Program from a Non-DisplayFile Page](/manuals/enhancements/enhancing-ui/calling-program-from-non-displayfile-page.html) where you will see the use `JobSession` class being used.

Note that you may need to call the `Command.CommitJobSession` if you modify the `JobSession` and do not `Command.Call` a program as the last operation of your Non-Display File page action. `Call` commits the `JobSession` prior to giving control to the called program.

### ASNA Provided Pages

The changes above will affect the following Razor Pages in the Monarch folder:
 * `Diagnose`
 * `EoJ`
 * `ExpiredSession`

#### Diagnose Page
The `OnGet()` method of `Diagnose.cshtml.cs` should read like this:
```cs
        public void OnGet()
        {
            AbEndMessage = Request.Query.ContainsKey("AbEndMessage") ? Request.Query["AbEndMessage"] : "";
            AbEndMessage = AbEndMessage.Replace("\\n", "\n");
            AbEndMessage = AbEndMessage.Replace("\\r", "\r");

            AbEndStack = Request.Query.ContainsKey("AbEndStack") ? Request.Query["AbEndStack"] : "";
            AbEndStack = AbEndStack.Replace("\\n", "\n");
            AbEndStack = AbEndStack.Replace("\\r", "\r");
        }

```
#### EoJ Page
The `OnGet` method of `EoJ.csctml.cs` should read like this:
```cs
        public void OnGet()
        {
            HttpContext.Session.Remove("ASNA_SingleJobNumber");
        }
```

> For websites supporting multiple jobs per browser, the `OnGet` can be removed.

#### ExpiredSession Page
The `OnGet` method in version 3.0 of `ExpiredSession.cshtml.cs` may had been clearing the session.  This should be removed.

#### AbEnd view
A new view `AbEnd` should be added to the Monarch folder with this content.

```html
@model ASNA.QSys.Expo.Model.YellowPageModel
@{
}

<div style="padding:1em">
    <h1>Abnormal Termination</h1>
    <br />
    <em>There has been an abnormal termination of the program.</em>

    <p><strong>Exception</strong></p>
    <pre style="background-color:yellow;">@ViewData["ASNA_AbEndMessage"]</pre>

    <p><strong>StackTrace</strong></p>
    <pre style="font-size: smaller">@ViewData["ASNA_AbEndStack"]</pre>
</div>
```






