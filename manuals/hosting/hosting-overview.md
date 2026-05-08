---
title: "Hosting a Monarch Application"
description: "Get a comprehensive overview of web hosting. Learn key concepts, tips, and best practices to host your website effectively."
---

There are two main types of applications:
 - Interactive
 - Batch

Accordingly, it is possible to host these applications on separate application servers, but commonly they are both hosted on the same (web) server.  Please see this article to learn how to [Host Interactive Applications](host-interactive-application.html).

When Batch Applications make use of delayed Job Queues, it is necessary to have a batch processor dispatching the jobs found on the queue.  Please see how to configure [Batch Dispatch](mom/batch-dispatch.html).

Similarly, if the reporting facilities of an application make use of delayed Output Queues, it is also necessary to have a printer writer produce the printed output.  Please see how to configure  [Printer Writer](mom/printer-writer.html).

 
