---
title: Configuring Job Idle Timeout
description: Maximize your system's efficiency and ensure optimal resource utilization with our step-by-step guide on Configuring Job Idle Timeout. This essential guide is tailored for system administrators and IT professionals looking to effectively manage job processes by setting appropriate idle timeouts. By adjusting the idle timeout settings, you can prevent unnecessary resource consumption by idle jobs, enhancing system performance and reliability. Whether you're working in a cloud computing environment, managing a server, or overseeing a network of computers, this guide provides the insights and instructions needed to fine-tune your job management strategy for better operational efficiency.
---

Similar to a website session timeout, there is a Job Idle Timeout. The JobIdleTime is specified in minutes and direct the Monarch Server to terminate those jobs that have been idle for that length of time.  A Job is considered to be idle if it has been ‘sitting’ on a screen waiting for user input for a ‘long’ period of time.  The default is 20 minutes.

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

So, assuming the defaults have stayed at 20 minutes in the SWBC website configuration then, it is expected that developer will see the debugger popup an [JobShutDownException](/reference/runtime/qsys-runtime-job-support/shutting-down-exception.html) dialog around 20 minutes of inactivity. This exception will typically be thrown when the program has been sitting too long on an `ExFmt` or `Read` operation to a Workstation file.


