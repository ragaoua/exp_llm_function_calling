This is just an experimentation with function calling

Run with

~~~bash
podman-compose up
~~~

The python container should print out something like :

~~~
[python] | DEBUG - Executing tool call : function=Function(name='get_db_logs', arguments={'range_end': '2025-02-12 10:00:00', 'range_start': '2025-02-12 09:00:00', 'server': 'DEA657FD'})
[python] | DEBUG - Function returned with : 2025-02-12 09:02:28 INFO: User 'admin' logged out.
[python] | 2025-02-12 09:07:15 INFO: New user 'mary_smith' created.
[python] | 2025-02-12 09:14:42 WARNING: Slow query detected on 'orders' table.
[python] | 2025-02-12 09:22:35 INFO: Database optimization process started.
[python] | 2025-02-12 09:28:50 INFO: Optimization completed successfully.
[python] | Based on the output, two major events happened around 9 AM on February 12th, 2025 on the database hosted on server DEA657FD:
[python] |
[python] | 1. A slow query was detected on the 'orders' table at 09:14:42.
[python] | 2. The database optimization process started at 09:22:35 and completed successfully at 09:28:50.
[python] |
[python] | These events may indicate potential issues with the performance of the database or the need for further maintenance.
~~~


Or :

~~~
[python] | DEBUG - Executing tool call : function=Function(name='get_db_logs', arguments={'range_end': '2025-02-12 09:59:59', 'range_start': '2025-02-12 09:00:00', 'server': 'DEA657FD'})
[python] | DEBUG - Function returned with : 2025-02-12 09:02:28 INFO: User 'admin' logged out.
[python] | 2025-02-12 09:07:15 INFO: New user 'mary_smith' created.
[python] | 2025-02-12 09:14:42 WARNING: Slow query detected on 'orders' table.
[python] | 2025-02-12 09:22:35 INFO: Database optimization process started.
[python] | 2025-02-12 09:28:50 INFO: Optimization completed successfully.
[python] | Based on the output of the tool call, around 9 AM on February 12th, 2025, on the database hosted on server DEA657FD, the following major events occurred:
[python] |
[python] | 1. At 9:02:28, user 'admin' logged out.
[python] | 2. At 9:07:15, a new user 'mary_smith' was created.
[python] | 3. At 9:14:42, a slow query was detected on the 'orders' table (this may indicate potential performance issues).
[python] | 4. At 9:22:35, a database optimization process started.
[python] | 5. At 9:28:50, the optimization process completed successfully.
~~~
