---
title: "Error Handling"
description: "Learn the essentials of effective error handling to improve application reliability and user experience with our concise guide."
---

In client/server environments such as the ASNA DataGate (DG) runtime, certain exceptions can occur that the programmer may wish to allow the program to recover from. For example, suppose that the network between your program (the client) and the database (the server) is disrupted. Instead of crashing or reporting the error and exiting, you could allow the user to try the procedure again when the network has been restored.

Exceptions specific to the DataGate provider being accessed by DG are communicated through [dgException](/reference/datagate/datagate-common/dg-exception.html). Most often, these exceptions are in the form of a condition identifier and a text message provided by the `Error` and `Message` [properties](/reference/datagate/datagate-common/dg-exception.html#properties) respectively.

The `ErrorClass` property classifies the condition identifier as one of the categories given by the [dgErrorClass](/reference/datagate/datagate-common/dg-error-class.html) enumeration. The `SystemError` property(/reference/datagate/datagate-common/dg-exception.html#properties) contains a provider-dependent exception identifier for certain exceptions. Likewise, the `Text` property may contain messages given by the underlying database for the exception.

DG throws other exceptions besides `dgException`. Please see the documentation for the particular DG object or method call for a description of the exceptions thrown.

`dgException` inherits from [System.Exception](https://learn.microsoft.com/en-us/dotnet/api/system.exception). `System.Exception` provides many useful functions for diagnosing and reporting bugs in your code and DG.

A reference to all DG error codes is provided in the documentation. Note that DG may report its own error codes as specified by the type library’s [ dgErrorNumber](/reference/datagate/datagate-common/dg-error-number.html) enumeration.


```cs 
using System;
using System.Data;
using ASNA.DataGate.Client;
using ASNA.DataGate.Common;

namespace NetworkRecovery 
{
      public class Tester
      {
          . . . 

          public void testConnection(string srcStr)
          {
                AdgConnection cx = new AdgConnection(srcStr);
                bool retry = false;
                // enter the "retry" loop
                do
                {
                    try
                    {
                        retry = false;
                        cx.Open();   // this will throw dgException if errors occur
                    }
                    catch ( dgException ex )
                    {
                        string errorMessge = ex.Message;
                        // check for error indicating "service not running"
                        if ( ex.Error == dgErrorNumber.dgEiNORESPONSE )
                            errorMessge = "Cannot connect to " + srcStr + ".  Is the service running?"; 
                        // check for error indicating "network down"
                        else if ( ex.Error == dgErrorNumber.dgEiCONNLOST ||
                                  ex.Error == dgErrorNumber.dgEiHOSTNOTFND )
                            errorMessge = "Cannot connect to " + srcStr + ".  Is the network available?";

                        Console.WriteLine ("Database Provider Unavailable.");
                        Console.WriteLine ( errorMessge );
                        Console.WriteLine ("Want to Retry? (Y/N)");
                        retry = Console.ReadLine() == "Y";
                    }
                } while (retry);
               // In this simple example, just check the connection state and quit
                if ( cx.State == ConnectionState.Open )
                    Console.WriteLine ( "Connected!" );
                cx.Close();
          }
      }
```

## See Also

[dgException Class](/reference/datagate/datagate-common/dg-exception.html)
<br />
[dgErrorClass Enumeration](/reference/datagate/datagate-common/dg-error-class.html)
<br />
[dgErrorNumber Enumeration](/reference/datagate/datagate-common/dg-error-number.html)

