# Akka HTTP

## Philosophy 
Akka HTTP has been driven with a clear focus on providing tools for building integration layers 
rather than application cores. 
As such it regards itself as a suite of libraries rather than a framework.

In this case the application architecture should be dictated by what makes sense for the core 
not the interface layer.

Akka HTTP is made for building integration layers based on HTTP and as such tries to 
“stay on the sidelines”. Therefore you normally don’t build your application “on top of” Akka HTTP, 
but you build your application on top of whatever makes sense and use Akka HTTP merely for the HTTP 
integration needs.

## Using Akka HTTP 
```
"com.typesafe.akka" %% "akka-http"   % "10.1.11" 
"com.typesafe.akka" %% "akka-stream" % "2.5.26" // or whatever the latest version is
```
Alternatively, 
```
sbt -Dsbt.version=0.13.15 new https://github.com/akka/akka-http-quickstart-scala.g8
```

## Routing DSL for HTTP servers 
The high-level, routing API of Akka HTTP provides a DSL to describe HTTP “routes” and how they should
be handled. Each route is composed of one or more level of Directives that narrows down to handling 
one specific type of request.

## Marshalling 
Transforming request and response bodies between over-the-wire formats and objects to be used in 
your application is done separately from the route declarations, in marshallers, which are pulled 
in implicitly using the “magnet” pattern. 
This means that you can complete a request with any kind of object as long as there is an implicit 
marshaller available in scope.
```
libraryDependencies += "com.typesafe.akka" %% "akka-http-spray-json" % "10.1.11"
```

## Streaming
One of the strengths of Akka HTTP is that streaming data is at its heart meaning that both request and response bodies can be streamed through the server achieving constant memory usage even for very large requests or responses.