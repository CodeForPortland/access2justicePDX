---
title: Documentation
description: Various guides, references and articles about the project and it's development processes.  
weight: 10
---

Various guides, references and articles about the project and it's development processes.

{{% image src="/images/code4america_wetcode.png" %}}
### [Deploying](deployment/)

- [Local/Development Deployment](deployment/local-deploy/)

## General Component Overview

The application's architecture is a distributed system and will be deployed using the [Civic Tech Labs's](https://www.codeforportland.org/CivicTechLab/) **AURA** project. It is a cluster of independent parts called *components*. 
The goal is to make each service *single purposed* and able to be developed *orthogonally*. 
It also allows the application developers to develop with the language they think works best for that situation. 

The intent is to break down our features into many focused services instead of one or few *monolithic* applications. 


**General Project Waffle** : [https://waffle.io/CodeForPortland/access2justicePDX/join](https://waffle.io/CodeForPortland/access2justicePDX/join)

### [Front End Modules](front-end)

- [Dashboard](front-end/dashboard)
- [Interview Wizard](front-end/interview-wizard)
- [Profiles](front-end/profiles)
- [Document Management](front-end/document-management)

### [Back End Modules](back-end)

- [Document Builder](back-end/document-builder)
- [Stores Manager](back-end/stores)
- [Security Manager](back-end/security)
- [File Service Module](back-end/file-service)

### Infrastructure

- **AURA** - A router utility for creating and managing data flow for communication to and from every component and API. [Waffle](https://waffle.io/CodeForPortland/CTL-AURA/join)  

- **Dockerfiles** - Containerization for each component allows for interoperability and CI flows.

