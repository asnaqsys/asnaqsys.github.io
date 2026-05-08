---
title: "Considerations for Accessing the Database"
description: "Explore efficient database access techniques. Learn about different methods, best practices, and tips for optimal data retrieval."
---

## Database Files

### Client/Server _vs_. Host Based

Traditional, green-on-black iSeries applications have the advantage of being run on the same machine as the database engine and data store. The foremost constraint in client/server processing is the network. Software engineers from all disciplines know that with client/server they are dealing with the physical aspects of packet transfer, task switching, band-width, traffic congestion, and so on. Client/server is well suited to transaction processing, especially when these features can be employed.

Batch and batch-like processing may be problematic with client/server because of the high data volumes and the high number of I/O requests. When the performance of batch processing becomes an issue considerably affecting the application's user experience - the Migrator needs to manually improve the program's performance.

### Improving Batch Processing Performance

Depending on the algorithm used by the legacy host-based batch processing program, one or more of the following techniques may need to be manually applied:
- Use net-blocking on input only files.
- Reduce the number of times loops execute.
- Utilize Range operations like SetRange and ReadRange.
- Reduce – or eliminate – file operations that use random access reads of related records in different files by utilizing join files.
