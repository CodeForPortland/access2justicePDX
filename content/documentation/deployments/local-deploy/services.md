---
title: A MicroService
description: Registering a microservice does not have to be scary.
weight: 40
---

A **MicroService** can be anything but think of it as a function, and a function should do one thing, and one thing well. [Bob Martin](http://butunclebob.com/ArticleS.UncleBob.SrpInRuby) refers to this paradigm as The Single *Responsibility Principle* and [Coding Horror](https://blog.codinghorror.com/curlys-law-do-one-thing/) call's it *Curly's Law*. 

The *microservice* we are implementing here may not do it well (as of this writing) but it does do only one thing. The basic idea is to break apart the functions of a larger application (usually referred to as a [Monolith](https://en.wikipedia.org/wiki/Monolithic_application)) and turn them into a bunch of small applications that provide single focus functions that work together, independently.

Here we have an *authentication service* and it's purpose in life is to validate the identity of a user via their *credentials*. This one returns a JSON Web Token, or **JWT** pronounced "JAWT", which rhymes with "dot".

## Connecting to the Router

Lets take a look into the files in the `ctl-authentication` project's directory. Consider the following declaration in the `connection.go` [file](https://github.com/CodeForPortland/ctl-authentication-service/blob/master/connection/connection.go).  

```go
const (
	realm = "aura.ctl.public"
	wsAddr   = "127.0.0.1:3131"
	wssAddr  = "localhost:4242"
	tcpAddr  = "127.0.0.1:8001"
	tcpsAddr = "localhost:8101"
	unixAddr = "/tmp/example_aura_sock"
)
```

Here we are declaring the values in which we will use to connect to the router with, if you follow the file's code down you will see a method call... 

`serviceClient, err := NewClient(clientAddrs, clientCfg, "ws")`

Here we are starting a new connection with the router creating a **Client**, it gets passed the values we saw in the last chapter for the *websocket endpoint* `"127.0.0.1:3131"` and the *realm* `"aura.ctl.public"`.

Other languages have differing syntax but the concept is the same, you create a *client* by making a *connection* to *the router* and passing that *connection* into some variable.

## Registering an RPC

Now you will use your client to make a *registration* of the service it provides by registering the **procedure name** with a **handler**.

A **handler** contains the logic of your service and is the entry point for the ambient components to send messages and payloads too. It is what will (or might not) return a response object to the requesting component to process with their *callback* function.

This authentications handler is defined in the `authentication.go` file.

Looking back towards the very top of the `RegisterService()` function we have a *const* declaration, 

```go
const (
    procedureName = "ctl.authentication"
)
```

Needless to say it is the name of our procedure and this is what we will use to trigger this *RPC*.

Now back towards the bottom of `RegisterService()` we are using our *client* to register this procedure with the method call `Register()`,

```go
serviceClient.Register(procedureName, authentication.AuthenticateHandler, nil)
```

This method consumes the *procedure name* and the *handler* and that's it for setting up the registration of an RPC.

## Go Service!

Now open another command prompt and step in the `ctl-athentication` projects root directory and run,

```bash
$ go run main.go 
```
This one two spits out logs to the `STDOut` and you should see something similar to the following...

```bash
NewClient> 2018/11/03 20:52:46 Connected to ws://127.0.0.1:3131/ using json serialization
``` 

Done. phew. And that's all there is to registering an *RPC* with the router.

## Next

Next we will test out our *RPC* by deploying our user interface with the [a2j-front-end_dashboard](https://github.com/CodeForPortland/a2j-front-end_dashboard).
