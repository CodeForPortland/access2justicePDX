---
title: Deploying Locally
description: A step by step explanation on how and what you are doing when deploying the project to your local developing environment.
weight: 10
---

### Scope of this Document

The target audience for this guide are developers new to the concepts held when using **WAMP v2** as the main communication standard and with little to no experience with **microservices**. 

The intent of this guide is provide two things:

- **first** - It will provide an introductory understanding and application of a *microservice architecture* using a *WAMP v2* router to allow a *UI* to communicate with a *microservice*.

- **second** - It will also document how the *WAMP v2* pattern is being utilized in this project and help enable those that wish to contribute. 

I hope to empower these developers by demonstrating how deploy a small *microservice architecture* and show that it is not as intimidating as it can first seem to be. There is not much more daunting than a blank piece of paper.

### Chapters

- [Local Dependencies](dependencies/) - Ensure that your machine has the basic dependencies to run a local version of the *AURA* server/router, and a demo service.
- [Cloning the Repos](cloning/) - Cloning the most recent version of *AURA*, an *authentication service* and the *front end dashboard*.
- [The AURA Router](router/) - About *WAMP v2* and the router and how to start it up.
- [A Microservice](services/) - Connecting the service and registering it as a remote procedure.
- [The User Interface](user-interface/) - Launching the dashboard and calling the *RPC*.
- [Resources and Attributions](resources/) - A listing of the links provided in this guide.