---
title: User Manager
description: An orchestrator for initiating session, login and registrations procedures and for providing responses to the front end clients.
weight: 10
---

The user manager provides pipelines and can trigger processes for providing services to a front end client. It has publicly exposed procedures on the public realm though it will be able to make predefined calls to private realm procedures. It's primary service will be to return session tokens.

## Transport

`{message: aura.Message}` is consumed and returned in the `kwargs` of the WAMP v2 invocation call.

## Public Procedures

- Register EndUser - Consumes the credentials supplied by a caller and runs validation processes on the values, checks for namespace availability and delegate's the process for storing the sensitive data. 


- Login/Logout EndUser - Consumes the credentials supplied by a caller and delegates authentication processes on the values. It then generates  or invalidates a session token and returns it to the caller. 

- Validate Session - Provides the publicly exposed interface for session validation.