---
title: "Edit Code Configuration"
description: "Discover how using fake data can accelerate development and testing. This guide covers benefits, tools, and best practices for effective use."
---


## Configure Zero Suppresion

To have Edit Codes Zero suppress at the second character position of the decimal part, similar to setting QDECFMT to 'J' on an IBM i, set the static configuration property `EditCodeFlags` of the `EditCode` class to  `EditCodeFlags.ZeroSuppressAt2ndChar`. 

### How Much To Suppress?
There are several EditCodes that request that, as numbers are being formatted, the leading zeros be replaced with blanks; these edit codes are:
 - EditCodes.**One**
 - EditCodes.**Three**
 - EditCodes.**A**
 - EditCodes.**C**
 - EditCodes.**J**
 - EditCodes.**L**
 - EditCodes.**N**
 - EditCodes.**P**

On certain systems like the IBM i, there is a way to configure the behaviour on how many leading zeros to the left of the decimal point should be replaced.  The two options are to replace all the way to the first character to the left of the decimal point or to only zupress at the second character.

For example, if the five digit value `000.50` were to be edited using the 'J' edit code, then this would be the result depending on the value of `EditCode.EditCodeFlags` (in this example the character '•' is used in place of a blank space):

|   `EditCodeFlags.None`   | `EditCodeFlags.ZeroSupressAt2ndChar` |
|------------|------------------------|
|  `•••.50`  |      `••0.50`          |

> When formatting, the character used for the decimal point is taken from the [current culture](https://learn.microsoft.com/en-us/dotnet/api/system.globalization.numberformatinfo.currentinfo) `NumberFormatInfo.CurrentInfo.NumberDecimalSeparator`


### Components that use EditCode

These are the components that format numbers using Edit Codes:
 - Website's Razor Pages TagHelpers (ASNA.QSys.Expo). Comparable to the old DDS EDTCDE for Display Files.
 - The Rutime EditCode methods for programs (ASNA.QSys.Runtime). Comparable to the old RPG bulit-in function %EDITC.
 - The Print File Manuscript Renderers (ASNA.QSys.Renderer...). Comparable to the old DDS EDTCDE for Printer Files.

Each one may be configured separately and with different approaches, but all of them share in common the usage of the Environmental Variable `asna:SystemValues:EditCodeFlags`.

The environment variable can be set like this:

```bat
C:\>set asna:SystemValues:EditCodeFlags=ZeroSuppressAt2ndChar
```

### Default Value

The default value for the EditCodeFlags static property for all the components below is taken from the Environmental Variable `asna:SystemValues:EditCodeFlags`.

The EditCode class has a static constructor with code similar to this:
```cs
        static EditCode()
        {
            string editCodeFlagsString = Environment.GetEnvironmentVariable("asna:SystemValues:EditCodeFlags");
            if (!string.IsNullOrWhiteSpace(editCodeFlagsString))
            {
                if (Enum.TryParse(editCodeFlagsString, out EditCodeFlags editCodeFlags))
                    EditCodeFlags = editCodeFlags;
            }
        }
```

### Configuration of the Website
The following code code may be added to the `Starup.cs` class to configure the TagHelpers behavior:

```cs

        // Set the EditCodeFlags from the appsettings.json file or other configuration sources
        private void ConfigureEditCodeFlags()
        {
            var editCodeFlagsString = Configuration.GetValue<string>("ASNA:SystemValues:EditCodeFlags");

            if (!string.IsNullOrWhiteSpace(editCodeFlagsString))
            {
                if (Enum.TryParse(editCodeFlagsString, out EditCodeFlags editCodeFlags))
                    EditCode.EditCodeFlags = editCodeFlags;
            }
        }

        // This method gets called by the runtime. Use this method to add services to the container.
        public void ConfigureServices(IServiceCollection services)
        {
            . . . 

            ConfigureMonaServer(services, IdleTimeout20);
            ConfigureEditCodeFlags();
        }

```

ASP.NET Core initializes the `Configuration` object using a [variety of configuration sources](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/configuration).

### Job Configuration for the Application Logic
The class ASNA.QSys.Runtime.Job uses a IConfigurationBuilder to set the value of EditCodeFlags. `Job` intitializes the ConfigurationBuilder with the file `appsettings.json` and with the environmental variables only.

### Manuscript Renderer Configuration
There are [several renderers](/manuals/hosting/mom/manuscript-renderer.html) provided with Monarch Base. These renderers can be configured using the common approach of using the Environmental Variable `asna:SystemValues:EditCodeFlags`.
