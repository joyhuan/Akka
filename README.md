# Akka
For OS 

Akka Streams && Reactive Streams

Why back-pressure? 


What is the Actor Model?
Conceptual Model of Concurrent Computation Originated in 1973

Actor Fundamental of COmputation 
Allowed Operations:
- Create another actor
- Send a message
- Designate how to handle message 

Private State 

Lightweight require fewer resources than threads

Isolated do not share memory

State can only be changed by receiving messages 

Can communicate with each other only through messages 
Mailbox/ message queue 

FIFO

Simple immutable data structure 

Can only handle one msg at one time 

Asynchronous 

Have Address of its children
can obtain others' address from message 
can have many addresses 
address != identity

can run locally/remotely 


Fault Tolerance 
Supervisor can restart 

Self-healing systems 

Pros
- easy to scale
- fault tolerance
- geographical distribution
- no share state 

Cons
- susceptible to deadlocks
- mailbox overflowing 


Best known implementation
- Akka
- Elixir
