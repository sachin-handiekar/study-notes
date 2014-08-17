# Lesson 2.2 Understand which OS metrics to monitor#

Performance Statistics to Monitor

Performance statistics should be gathered at every level of the software stack including -

* Operating System
	- Hypervisor and virtualization layer if applicable
* JVM  ( including GC )
* Application ( Response time & Througput)

And in some cases, hardware level performance counter metrics should be gathered.

View statistics in an online mode or after the act in an offline mode.

CPU usage, including user CPU , system CPU and idle time

[Define the above CPU time's]

Virtual Memory usage - Java application swapping to real memory


Process behaviour, especially context switching and CPU scheduling and thread migrations.


Disk I/O, if Disk I/O is involved wit the application.

Network I/O, if network traffic is involved with the application.



