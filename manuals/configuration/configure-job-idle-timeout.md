---
title: "Configuring Job Idle Timeout: A Quick Guide"
description: "Learn how to set up job idle timeout settings effectively. This guide ensures your jobs manage resources efficiently, avoiding unnecessary costs."
---

Similar to a website session timeout, there is a Job Idle Timeout. The JobIdleTime is specified in minutes and direct the Monarch Server to terminate those jobs that have been idle for that length of time.  A Job is considered to be idle if it has been ‘sitting’ on a screen waiting for user input for a ‘long’ period of time.  The default is 20 minutes.

## There are 2 Timeouts
Monarch generated websites default the Session and the Job idle time out to 20 minutes.  These timeouts are set as part of the `ConfigureServices` Method of the website’s `Startup` Class as shown here:

```cs
        public void ConfigureServices(IServiceCollection services)
        {
            TimeSpan IdleTimeout20 = TimeSpan.FromMinutes(20);

               . . . 

            services.AddSession(options =>
            {
                options.IdleTimeout = IdleTimeout20;
                options.Cookie.IsEssential = true; // make the session cookie Essential -- Problematic for DGPR??
            });

               . . . 

            ConfigureMonaServer(services, IdleTimeout20);
        }
```

Notice that the value `IdleTimeout20` is used to configure both the [Session idle timeout](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/app-state#session-options) and is passed on to ConfigureMonaServer which uses the value to start the Monarch Server as shown below:

```cs
        void ConfigureMonaServer(IServiceCollection services, TimeSpan IdleTimeout)
        {
            MonaServerConfig monaServerConfig = new MonaServerConfig();
            Configuration.GetSection("MonaServer").Bind(monaServerConfig);

            if (string.Compare(monaServerConfig.HostName, "*InProcess", true) == 0)
            {
                if (monaServerConfig.JobIdleTimeout > 0)
                    IdleTimeout = TimeSpan.FromMinutes(monaServerConfig.JobIdleTimeout);
                var assemblies = string.Join(',', monaServerConfig.AssemblyList.ToArray());
                ASNA.QSys.MonaServer.Server.StartService("*LoopBack", monaServerConfig.Port, IdleTimeout, assemblies,
                                                        (ASNA.QSys.MonaServer.TraceOptions)monaServerConfig.TraceOption, false);
            }

            services.AddSingleton<IMonaServerConfig>(s => monaServerConfig);
        }
```

Also notice that it is possible to provide a [JobIdleTimeout](configure-expo-website.html#monaserver) value as part of the MonaServer configuration section to override the value passed to ConfigureMonaServer. The MonaServer configuration section is typically established in the website’s appsettings.json file. When the Monarch Server is not running in the same process as the web site, the only way to establish the job idle timeout is via a `JobIdleTimeout`.


## Timeouts and Debugging

When running a Monarch application within Visual Studio, and assuming the defaults have stayed at 20 minutes, it is expected that a developer will see the debugger popup an [JobShutDownException](/reference/runtime/qsys-runtime-job-support/shutting-down-exception.html) dialog around 20 minutes of inactivity. This exception will typically be thrown when the program has been sitting too long on an `ExFmt` or `Read` operation to a Workstation file.

It may be convenient to extend the time out period when running debug versions as shown in the following example.

```cs
        public void ConfigureServices(IServiceCollection services)
        {
            TimeSpan IdleTimeout20 = TimeSpan.FromMinutes(20);

            // Extend idle time out when running in debug mode
            #if DEBUG   
                 IdleTimeout20 = TimeSpan.FromHours(2);
            #endif
            . . . 
```