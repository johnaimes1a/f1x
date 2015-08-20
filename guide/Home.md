# What is F1X #

![](https://github.com/johnaimes1a/f1x/blob/master/guide/logo.png) F1X is open source implementation of FIX Protocol in Java.

## Why ##

Do we need another Java FIX engine when we have [QuickFIX/J](http://www.quickfixj.org/)?

Authors of F1X have been using QuickFIX/J for many years. Unfortunately QuickFIX/J can no longer keep up with modern financial applications - it is too slow and it produces a lot of short-lived objects (garbage). Garbage Collection pauses lead to unpredictable performance.


F1X is:
  * **Garbage-free**. API and implementation provide alloc-free FIX messaging.
  * **Fast** (message encoding/decoding is 10x / 6x [faster](Performance) than QuickFIX/J). For example: NewOrderSingle(D) message encoding takes about 500 nanoseconds, decoding takes around 210 nanoseconds.
  * Supports FIX protocol version 4.1 ... 4.4 (5.0 in near term plans).
  * Multiple FIX sessions with different FIX dialects can be hosted in a single JVM.


## Documentation ##

Read [Quick Start](QuickStart) and [FAQ](FAQ) pages.

Advanced topics:

  * [Session Schedule](SessionSchedule)
  * [Message Logging](MessageLogging)
  * [Message Store](MessageStore)
  * [Writing a FIX Server](FixServer)
  * [Dealing with message gaps](MessageGaps)
  * [Performance](Performance)

## Download ##

Please download project sources and build them using provided Ant / Maven / Grail scripts.

## Third party dependency ##

F1X uses the following software libraries:
  * [Disruptor](http://lmax-exchange.github.io/disruptor/) disruptor buffer is used for asynchronous I/O.
  * [GFLogger](https://bitbucket.org/vladimir.dolzhenko/gflogger/wiki/Home) Garbage Free Logger.
  * [QuickFIX/J](http://www.quickfixj.org/) QuickFIX dictionaries are used to auto-generate standard FIX enumerations and constants.
  * [JUnit](http://junit.org/)

