---
title: "YellowController class          | QSYS API Reference Guide"
description: "Represents a controller for facilitating operations from a web application to a Monarch job."
last_modified_at: 2025-11-07T12:00:00Z
---

Represents a controller for facilitating operations from a web application to a Monarch job.

**Namespace:** ASNA.QSys.Expo.Model
**Assembly:** ASNA.QSys.Expo.Model.dll

**Inheritance:** [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) --> [ControllerBase](https://learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.controllerbase?view=aspnetcore-8.0)
<br>
<br>

## Remarks

`YellowController` is a small helper controller class used by web endpoints that need to start, access, or end a Monarch job associated with the current ASP.NET Core session. It encapsulates the logic to retrieve a per-session job `Command` instance, start the job if it isn't already running, and to request a shutdown and clear session state when the job ends.

The implementation follows a pattern where session-backed state (`SessionStorage`) holds the job handle. `GetJobCommand` returns a `Command` configured for the session and ensures the job is started. `EndJob` asks the job to shut down (if started) and clears session storage to avoid stale state.

## Properties

| Type | Name | Description |
| --- | --- | --- |
| Command | command | Private field that holds the `Command` instance used to interact with the Monarch job. (private) |
| [SessionStorage](/reference/expo/qsys-expo-model/session-storage.html) | SessionStore | Lazily-initialized session storage helper (wraps `HttpContext.Session`) |

## Methods

| Signature | Description |
| --- | --- |
| [Command](/reference/expo/qsys-expo-model/command.html) [GetJobCommand(String)](#command-getjobcommandstring-jobclasssuffix) | Retrieves the `Command` for the current session, starting the job on the blue side if necessary. |
| void [EndJob()](#void-endjob) | Ends the current job and clears the session store. |

### Command GetJobCommand(string jobClassSuffix)

Retrieves the job command for the current session, starting the job on the blue side if necessary.

```cs
protected Command GetJobCommand(string jobClassSuffix = "")
```

Parameters

| Type | Parameter name | Description |
| --- | --- | --- |
| string | jobClassSuffix | Optional suffix to append to the job class name when starting the job (defaults to empty string). |

Returns

| Type | Description |
| --- | --- |
| [Command](/reference/expo/qsys-expo-model/command.html) | The `Command` instance associated with the current session. The method ensures the job is started before returning. |

Exceptions

This method may throw if the underlying job start operation fails; the implementation clears the ASP.NET session before rethrowing an exception wrapper indicating failure to start the job.

### void EndJob()

Ends the current job and clears the session.

```cs
protected void EndJob()
```

Behavior

- Constructs a `Command` for the session's job handle and calls the request-shutdown method if the job is running.
- Catches `RedirectedException` instances raised during shutdown and rethrows only if the redirect is not an End-Of-Job (EOJ) type. Finally, the ASP.NET session is cleared to remove job-related state.

## Usage notes

- Controllers or endpoints that need to perform operations against a Monarch job can inherit from `YellowController` and call `GetJobCommand()` to get an initialized `Command` instance.
- Call `EndJob()` to request a job shutdown and to ensure session data (including the job handle) is removed.

## Examples

Simple usage in a derived controller action:

```cs
[HttpPost("CustomerSales")]
public IActionResult CustomerSales([FromBody] CustomerSalesRequest request)
{
    Command cmd = GetJobCommand("Service"); // ensures job is started

    // use cmd to interact with the job...
    string[] parms = new string[2];
    parms[0] = request.CustNumber;
    parms[1] = request.Sales;
    command.Call("CUSTSALES", parms);
    parms[1] = ZonedToDecimal(parms[1]).ToString();     // Sales
    parms[0] = "OK";
    return Ok(new { parms });
}

[HttpGet("EndSession")]
public IActionResult EndSession()
{
    EndJob(); // requests shutdown and clears the session
    return Ok();
}
```

## See also

- [SessionStorage](/reference/expo/qsys-expo-model/session-storage.html)
- [Command](/reference/expo/qsys-expo-model/command.html)
- [RedirectedException](/reference/expo/qsys-expo-model/redirected-exception.html)
