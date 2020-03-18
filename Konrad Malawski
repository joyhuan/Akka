Back pressure 
Fast Producer 
Slow Subscriber 

What if overflow? 
- Bounded Buffer 
drops msgs + require re-sending

Kernel does this! Routers do this! (TCP)

- Increase buffer size... 


Reactive Streams 
pull-based-backpressure

Standard 
JDK 0 was merged as part of java improvement process jab 266 



Akka Streams & Scala Futures Local abstractions   

As a glue between systems  

Solving distributions 
turns out for source of concurrency 


sources and sinks so data flow from a source to a sink
flow

API
// types: 
Source[Out, Mat]
Flow[In, Out, Mat]  Proper static typing! 
Sink[In, Mat]

// generally speaking, it's always: 
val ready = Source(???).via(fow).map(_ * 2).to(sink)

val mat: Mat = ready.run()

// the usual example:
val f: Future[String] = 
	Source.single(1).map(_.toString).runWith(Sink.head)



The purpose of stream is to never have the entire stream in memory 

key feature: just work on a limited amount of the data so you have bounded memory processing and of course as fast as you can and not faster 

flow control 


Materialization 

blueprint 

when run it, we have some additional steps that other libraries don't have freedom to do they usually construct the running things 
we const the blueprint
then have fused optimized graph which we then execute
run on akka actors 
over a synchronous parts of the graphs 
all the expected performance benefits 


complete HTTP server 
Akka system being both the building block and the glue 

HttpServer 
