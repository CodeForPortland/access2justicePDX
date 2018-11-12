---
title: The AURA Router
description: The AURA router is the main hub of communication.
weight: 30
---


## About The Router
 
**AURA** stands for an Agnostic Utility for Remote Applications and in this guide it is synonymous with the term *Router*. It is built using the [Nexus Library](https://github.com/gammazero/nexus/wiki) and implements a [WAMP v2](https://wamp-proto.org) standard for organizing communications between various ambient components.
 This pattern is commonly found in *enterprise* and *IOT* systems, it allows for the decoupling of components to provide an orthogonal approach to development, making it robust to change and allow for a polyglot tech stack.

## About WAMP

{{% notice warning %}}[WAMP](https://wamp-proto.org/index.html) != [WAMP](http://www.wampserver.com/en/) 
{{% /notice %}}

*WAMP v2* utilizes a [PubSub](https://en.wikipedia.org/wiki/Publish–subscribe_pattern) and [RPC](https://en.wikipedia.org/wiki/Remote_procedure_call) pattern that is common in event driven systems. These work right out of the box with **Nexus**, all we really need to do is tell it to setup a *server* and a *realm*.

{{% notice info %}}A **Realm** is another dynamic to an endpoint to allow one connection point multiple or replicated responsibilities. When connecting a component to the router usually using a library like [Crossbar.io](https://crossbar.io), you will need to provide a URL (eg `ws://examplehost:1234`) and a **realm** (eg `aura.a2j.public`). 
{{% /notice %}}

**PubSub** is an **Observer** pattern, which the book [Design Patterns](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612) defines as *...a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically*.
What it does is create a **Topic** which relates to a *value* and can be *observed* by **subscriber**. The topics value can change by *publishing* to it with (I'm sure you guessed it...) a **publisher**. The router allows ambient components to create *topics*, which other ambient components and itself can subscribe or publish too.

**RPC (Remote Procedure Calls)** I like to think of a *remote procedure call* as just a function inside my code that I can call just like any other function I just wrote, but it's not! The logic it uses resides in another code base outside of mine. **AURA** allows a component to **register** a function with a name usually called a *procedure name*. Eg `aura.authenticate`. An ambient component can then make a **call** to the *RPC* which executes that function to return a response to a callback.

One analogy is to think of a *PubSub* as being "**cold**" and a *RPC* as being "**hot**", meaning a *PubSub* pattern will wait for something to happen before it emits anything to it's listeners and an *RPC* is actively called for an expected result right away.

## Go Router!

{{% notice warning %}}AURA is in current development expect the details to not be exact, I will try and keep things updated as I go but the ideas should remain the same.  
{{% /notice %}}


Now, before you launch the router from the `main.go` file, lets look a little into the code. Inside of *main* you will notice the following function call...

```go
aura.NewServer("aura.ctl.public", []string{"*"})
```

Examining the arguments, it might be good to notice the `"aura.ctl.public"` string. This is the realm that the new server is going to use and provide the aforementioned ambient components will connect to. The  other argument is less important for this guide but denotes the `AllowedOrigins` it accepts for components to request a connection from, for development we are using `*` which is a wildcard to allow the various development environment setups to connect without a warning. 

Now open a new bash and step into the AURA project directory we made in the last chapter. 

Run the following commands 
```bash
go get github.com/dgrijalva/jwt-go/...
go get github.com/gammazero/nexus/...
go run main.go
```

Next you should see some logs being sent to the `STDOut`, what we want to see is something similar to this in the logs..

```shell
2018/11/03 20:06:16 Websocket server listening on ws://127.0.0.1:3131/
```

This lets us know that we have an endpoint we can connect to at `ws://127.0.0.1:3131/` and with the realm stated earlier (`"aura.ctl.public"`).

And that's it! You have a WAMP Router running on your machine.

## Next

Now before we launch the user interface lets set up a service and register a **Remote Procedure Call** in the next chapter.