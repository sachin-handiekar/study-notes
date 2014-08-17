# Java HotSpot VM Components #

3 major sub-systems :

1. VM runtime
2. Garbage Collector / Memory Manager
3. JIT Compiler


## VM Runtime ##

Responsible for command line option parsing, JVM life cycle, exception handling, fatal error handling, class loading, interpreter, Java native interface, thread management and synchronization.

## Garbage Collector / Memory Manager ##

Responsible for Java object memory management including allocation and reclamation.

A garbage collector can influence the performance and responsiveness of a Java application.

The HotSpot JVM has four different garbage collectors (generational garbage collectors)

Two are stop the world.

Other two are a combination of stop the world and a mostly concurrent garbage collector.

Stop the world GC

* Stops all the Java application threads

Mostly-concurrent GC

* Concurrently executes while the Java application is running.

A generational garbage collector partitions the Java heap into two or more regions / generations.


Young generation vs old generation.

* young generation is for newly allocated objects
* Old generation is for longer lived objects

Longer the object lives, it gets moved to old generation.


Permanent generation (Java 6 & 7)

* Holds the class data strucutures

Peramanent Generation (Java 8)

* Eliminated in favour of a metaspace



### Serial Garbage Collector  ###

* Single threaded stop the world young generation collector
* Single threaded stop the world old generation collector
* Tends to have the smallest footprint

### Throughput Garbage Collector (Parallel Garbage collector  ###

* Multithreaded stop the world young generation collector

Server class machine default collector

* Multithreaded young generation and old generation collector

Server Class machine

* 2 GB or more of RAM
* 2 or more virtual processors

### Concurrent Garbage Collector (CMS)  ###
* Multithreaded stop the world young generation collector
* Mostly concurrent old generation collector


### G1 Garbage Collector  ###

* Supported as of Java HotSpot 7 update 4
* 