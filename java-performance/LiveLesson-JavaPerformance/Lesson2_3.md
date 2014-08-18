#Lesson 2.3 JVM Performance Metrics to Monitor#

##Monitoring Garbage Collection##
* Recommend using the following command line options with the Java HotSpot VM to capture garbage collection logs

-XX:+PrintGCDetails
-XX:+PrintGCDateStamps or -XX:+PrintGCTimeStamps
-Xloggc if you'd like to direct output to a log file

* VisualVM's VisualGC to obeserve GC activity in an "online" mode.


##Monitoring application execution time and stopped time##

* To identity when the JVM has stopped application thrads from executing due to a GC event or some other "safepoint" operation.

-XX:+PrintGCApplicationStoppedTime
-XX:+PrintApplicationConcurrentTime

* JIT Compilation
-XX:+PrintCompilation
-XX:+PrintInlining

* Fine tuning JVM heap spaces sizes

-XX:+PrintTenuringDistribution
-XX:+PrintAdaptiveSizePolicy (Parallel GC or G1 only)


