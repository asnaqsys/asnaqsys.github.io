---
title: "Surfacing Program Calls as Web APIs"
description: "Create Web API to call program from a web client." 
---


## Application Architecture Refresher

As described [here](/concepts/architecture/application-architecture.html#interactive-job-architecture), a migrated application can run on a webserver with users interacting with it via a web browser running on their own PCs. 

![Application Tiers](/concepts/architecture/images/mas-in-process.svg)

_Interactive Application running in four tiers_

Conceptually there are four tiers or processes involved in the execution of the application:
1. User PC displaying UI (HTML)
2. Website rendering 'screens' as HTML
3. Application logic executing 'programs' which produce the 'screens'
4. Database Server

### Focus on 'Screens'
Let's focus on the second tier above. The rendering of the screens as HTML is achieved by using Razor Pages.  Razor Pages use a Controller/View architecture where the Controller gathers/produces all the data, and the View takes that data and produces the HTML (the View is a mixture of HTML and Tags). 

In migrated applications, each **Display File** is transformed into a **Razor Page**.

### Focus on 'Programs'
Migrated programs are converted to .NET classes. Programs can be generally divided as being Interactive or not. Interactive Programs _interact_ directly with the user via a migrated **Razor Page**.  Non-Interactive programs typically communicate via input and output parameters without requiring any data directly from the user.

## Exposing Non-Interactive programs as a Web API

Sometimes it may be convenient to allow processes outside of the Application to activate certain application functions by calling individual programs.  There are several methods that can be employed, a common one is the use of the Website facilities  to surface a **Web API**. 

There is a rich set of facilities to create [APIs with ASP.NET Core](https://dotnet.microsoft.com/en-us/apps/aspnet/apis).  These facilities allow for the creation of Web APIs that expose programs as endpoints of the website.

![Web API](./images/web-api.svg)

_Exposing a Program as a Web API_

The Web API plays along the rest of the Application tiers, however some of the tiers behave with some variations.  The tiers play these roles:
1. Client system provides and consumes the program parameters typically using JSON payloads
2. Website Controller exposed endpoints repackage parameters and call program
3. Application logic executes the program and returns any output parameters
4. Database Server

Tiers 3 and 4 above do not change much from the original setup prior to the migration. 

### The Web API Controller

The novelty of the setup is the creation of an ASP.NET Core Controller that implements routes or endpoints that do not go to a Razor Page but instead are directed to your code. 

You can define routes and HTTP verbs directly within your ASP.NET code using attributes. The framework automatically maps data from the request path, query string, and body to the corresponding method parameters.

To facilitate the creation of the Controller, Monarch provides the base class [YellowController](/reference/expo/qsys-expo-model/yellow-controller.html) which itself is an extension of .NET's [ControllerBase](//learn.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.mvc.controllerbase).

`YellowController` is a small helper controller class used by web endpoints that need to start, access, or end a Monarch job associated with the current ASP.NET Core session. It encapsulates the logic to retrieve a per-session job [Command](/reference/expo/qsys-expo-model/command.html) instance, start the job if it isn't already running, and to request a shutdown and clear session state when the job ends.

The `Command` class provides a method that allows for a program to be called, it is through this facility that a program can be invoked from an endpoint on the website.

Here is an example of a controller enabling the call to a non-interactive program called `CUSTCALC`, and the ending of the job that is used to host the program.  For the example `SalesController` shown below, a client application could invoke `CalcSalesReturns` multiple times, the first call would establish a new Job and subsequent calls (on the same Session) would reuse the Job, the client application would be responsible to end the Job by invoking the `EndSession` endpoint.

```csharp
    [Route("api/[controller]")]
    [ApiController]
    public class SalesController : YellowController
    {
        [HttpPost("CalcSalesReturns")]
        public IActionResult CalcSalesReturns([FromBody] CalcSalesReturnsRequest request)
        {
            try
            {
                Command command = GetJobCommand("Service");

                string[] parms = new string[3];
                parms[0] = request.CustNumber;
                parms[1] = request.Sales;
                parms[2] = request.Returns;

                command.Call("CUSTCALC", parms);
                parms[1] = ZonedToDecimal(parms[1]).ToString();     // Sales
                parms[2] = ZonedToDecimal(parms[2]).ToString();     // Returns
                parms[0] = "OK";
                return Ok(new { parms });
            }
            catch (Exception ex)
            {
                return StatusCode(500, new { error = $"CalcSalesReturns failed: {ex.Message}" });
            }
        }

        [HttpGet("EndSession")]
        public IActionResult EndSession()
        {
            EndJob();
            return Ok();
        }

        decimal ZonedToDecimal(string zoned)
        {
            . . . 
        }

        public class CalcSalesReturnsRequest
        {
            public string CustNumber { get; set; }
            public string Sales { get; set; }
            public string Returns { get; set; }
        }
    }
}
```

### The Web API Client

Here is an example of a Client application for the sample Controller shown above. The application defines a class to wrap the calls to the Web API.  This is the SalesApiClient:

```csharp
    public class SalesApiClient
    {
        private readonly HttpClient _httpClient;
        private readonly string _baseUrl;

        public SalesApiClient(HttpClient httpClient, string baseUrl)
        {
            _httpClient = httpClient;
            _baseUrl = baseUrl.TrimEnd('/');
        }

        public async Task<string[]> CalcSalesReturnsAsync(string custNumber, string sales, string returns)
        {
            var url = $"{_baseUrl}/Sales/CalcSalesReturns";
            var request = new CalcSalesReturnsRequest
            {
                CustNumber = custNumber,
                Sales = sales,
                Returns = returns
            };

            var response = await _httpClient.PostAsJsonAsync(url, request);
            if (!response.IsSuccessStatusCode)
            {
                // Read the error details from the response body
                var errorContent = await response.Content.ReadAsStringAsync();
                throw new HttpRequestException(
                    $"Request failed with status code {response.StatusCode}. Server response: {errorContent}");
            }
            var result = await response.Content.ReadFromJsonAsync<CalcSalesReturnsResponse>();
            return result?.parms;
        }

        public async Task<bool> EndSessionAsync()
        {
            var url = $"{_baseUrl}/Sales/EndSession";
            var response = await _httpClient.GetAsync(url);
            return response.IsSuccessStatusCode;
        }

        public class CalcSalesReturnsRequest
        {
            public string CustNumber { get; set; }
            public string Sales { get; set; }
            public string Returns { get; set; }
        }

        private class CalcSalesReturnsResponse
        {
            public string[] parms { get; set; }
        }
    }

```

The application could then use the `SalesApiClient` class like this:

```csharp
        private async Task RunSalesApiClientTests()
        {
            var salesClient = new SalesApiClient(new HttpClient(), "https://your-website/api-base/");

            decimal customerNumber = 1200;
            do
            {
                string textCustomerNumber = customerNumber.ToString("000000000");
                
                // Call CalcSalesReturns
                string[] result = await salesClient.CalcSalesReturnsAsync(textCustomerNumber, "0000000000000", "0000000000000");
                Console.WriteLine($"CalcSalesReturns for Customer# {customerNumber}: " + string.Join(", ", result));
                Console.WriteLine();

                Console.WriteLine("Would you like to test another customer number? (Enter a positive number or 0 to exit): ");
                string input = Console.ReadLine();
                
                customerNumber = 0;
                decimal.TryParse(input, out customerNumber);
            } while (customerNumber > 0);

            // Call EndSession
            bool ended = await salesClient.EndSessionAsync();
            Console.WriteLine("EndSession result: " + ended);
        }

    }
```    

## Configuration
There are three main aspects that require some configuration settings or additional application support. These are:
 - A Service Job class to support the programs called
 - Mapping of the endpoint controllers
 - And most important security

### Securing the Web API Services
A big WORD regarding Security.

It is imperative that prior to relasing a set of Web APIs to the wild, just as prior to releasing any website in general, the security of the services be well established.

The security concerns of a Web API service are well beyond the scope of this article. There is a plethora of [ASP.NET Core security](https://learn.microsoft.com/en-us/aspnet/core/security/) facilities that you should consider when configuring your services.

Exposing a service only to a single, trusted internal server (rather than the public internet or a broad internal network segment) significantly reduces the attack surface. This approach helps to:
 - Mitigate common attacks: Many automated attacks like vulnerability scans, brute-force attempts, and certain types of denial-of-service attacks are entirely avoided because they cannot reach the service from outside the trusted perimeter.
 - Implement defense in depth: This strategy uses the principle of least privilege, limiting access strictly to systems that absolutely require it, making it harder for an attacker who has compromised a different system to move laterally to this specific service.
 - Simplify security controls: Security efforts can be focused on securing the single trusted intermediary and the communication channel to it, rather than securing every possible entry point. 

Exposing the service exclusively to a single trusted internal server may alleviate many of the most common attacks but ask your **Security Department** to assist you in this matter.

Let's now go back to the basic configuration required to make the Web APIs functional.


### Service Job Class

#### Job Class for Users
Under typical scenarios, a migrated application's website defines its main [InteractiveJob](/reference/runtime/qsys-runtime-job-support/interactive-job.html) class in such a way that it invokes an interactive program to communicate with the user.  The steps taken by this InteractiveJob class, particularly in the implementation of the `ExecuteStartupProgram()` is not conducive to support Web API calls.

#### Job Class for Web APIs
What is needed to service API calls is a Job class that invokes not an Interactive Program but that instead calls the `AcceptCommands()` method.  The steps to setup the Job and the use of the Command class are similar to the steps needed to [call Programs from Non-Display Pages](/manuals/enhancements/enhancing-ui/calling-program-from-non-displayfile-page.html), please read the article for background knowledge.

#### Defining the Job Classes Names
For a website that serves both Interactive users and API calls it is convenient then to have two Job classes, one for each use case. The name of the default (the user's) Job class is defined in the `appsettings.json` file, for example, if the class were called `Acme.ERP.MyJob`, the appsettings.json would look like this:

```json
   . . . 
  "JobDescriptor": {
    "Class": "Acme.ERP.MyJob",
    "Name": "ERCAP"
  },
  . . . 
```

In order to distinguish the name of the other (the API) Job class the [GetJobCommand](/reference/expo/qsys-expo-model/yellow-controller.html#command-getjobcommandstring-jobclasssuffix) receives an optional parameter with the suffix to append to the job class name when starting the job. The name of the API Job class used is the concatenation of the class in the appsettings `"Class"` value plus the suffix modifier passed to the GetJobCommand method. 

If the class for the Web APIs was called `MyJobService` in the same namespace as used in the appsettings.json shown above, then the `GetJobCommand` call would have to look like this:

```cs
    Command command = GetJobCommand("Service");
    . . . 
    command.Call("CUSTCALC", parms);
    . . .
```

The `GetJobCommand("Service")` call would instantiate an object of type `Acme.ERP.MyJobService` and return a Command on that MyJobServce. 

### Job Class Example
Using the configuration above, the application would define two Job classes:
 - `Acme.ERP.MyJob` for 'regular' users interacting with the application with their browsers
 - `Acme.ERP.MyJobService` for Web API clients

Both classes would be defined within the same website. In their simplest form, the difference between the two lies in the implementation of their `ExecuteStartupProgram` methods: one ends up calling an interactive program (such as a menu), while the other invokes the `AcceptCommands` method from the base class.

#### MyJob Example

Let's first look at the `Acme.ERP.MyJob` class.  A simplistic implementation follows:

<details markdown="1">
  <summary><h5> ▼ C# Example</h5></summary>

```csharp
namespace Acme.ERP
{
    public class MyJob : InteractiveJob
    {
        public Database MyDatabase = new Database("TheIBMi");
        . . . 
        public static MyJob JobFactory()
        {
            MyJob job = new MyJob();
            return job;
        }

        override protected void ExecuteStartupProgram()
        {
            MyDatabase.Open();
            . . .
            _DynamicCaller.CallD("Acme.ERP.COSTMENU", out _LR);
        }
    }
    . . .
}
```

</details>

<details markdown="1">
  <summary><h5> ▼ Encore RPG Example</h5></summary>

```php
DclNamespace Acme.ERP
BegClass MyJob Extends(InteractiveJob)  Access(*Public)
    DclDB Name(MyDatabase) DBName("TheIBMi") Access(*Public) 
    . . . 
    BegFunc JobFactory Access(*Public) Shared(*Yes) Type(MyJob)
        DclFld job   Type(MyJob)
        job = *new MyJob()
        LeaveSr job     
    EndFunc

    BegSr  ExecuteStartupProgram Access(*Protected) Modifier(*Overrides)
        Connect     MyDatabase
        . . .
        CallD  "Acme.ERP.COSTMENU"
    EndSr
    . . .
EndClass    
```

</details>

#### MyJobService Example

Now let's see a trivial implementation of the `Acme.ERP.MyJobService` class. Both of these :

<details markdown="1">
  <summary><h5> ▼ C# Example</h5></summary>

```csharp
namespace Acme.ERP
{
    public class MyJobService : InteractiveJob
    {
        public Database MyDatabase = new Database("TheIBMi");
        . . . 
        public static new MyJobService JobFactory()
        {
            MyJobService serviceJob = new MyJobService();
            return serviceJob;
        }

        override protected void ExecuteStartupProgram()
        {
            MyDatabase.Open();
            . . .
            AcceptCommands();
        }
    }
    . . .
}
```

</details>

<details markdown="1">
  <summary><h5> ▼ Encore RPG Example</h5></summary>

```php
DclNamespace Acme.ERP
BegClass MyJobService Extends(InteractiveJob)  Access(*Public)
    DclDB Name(MyDatabase) DBName("TheIBMi") Access(*Public) 
    . . . 
    BegFunc JobFactory Access(*Public) Shared(*Yes) Type(MyJobService)
        DclFld serviceJob   Type(MyJobService)
        serviceJob = *new MyJobService()
        LeaveSr serviceJob     
    EndFunc

    BegSr  ExecuteStartupProgram Access(*Protected) Modifier(*Overrides)
        Connect     MyDatabase
        . . .
        AcceptCommands()
    EndSr
    . . .
EndClass    
```

</details>


### Mapping The Website Endpoint Controllers

Migrated applications have in their Website's `Startup` class the method `Configure` which establishes the main characteristics of the web application and includes the mapping of Razor Pages. When the website is to also serve Web APIs, it is necessary to also map the Controllers as shown below:

```cs
    public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
    {
        . . . 

        app.UseSession();

        app.UseRouting();

        app.UseEndpoints(endpoints =>
        {
            endpoints.MapRazorPages();
            endpoints.MapControllers();    // <<<<< Configure the Web APIs
        });
    }
```
