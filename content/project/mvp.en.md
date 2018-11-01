---
title: MVP
weight: 1
updatedon: 2018-11-01
---

The MVP will be an application for generating **pdf documents** from an **interview process** that can then be *edited*, *shared* and *viewed* on a mobile device via a role-based access system.

The app will initially be for internal use only, by *The Commons Law Center*. The idea is to create a more effective way to fill in large and confusing legal forms.
Essentially we are creating a **Turbo Tax** for family court. 

## Terminology

- **Plead Papers** - Documents standardized in a legal style that is acceptable in court. [Example](https://drive.google.com/file/d/0B84afZwP6zYZR0JqVE5RaFBNZDFPMDFHdG03V2JkQi1Hbjhz/view?usp=sharing)

- **Interview** - A process of questions and answers that develops information on a given subject. 


## Epic

As a *The Commons Law Center* lawyer I want to use a mobile application to make my workload easier and to more effectively managed. I would want to access the application and my data on a tablet device. 
One feature I would expect is a series of questions called **an interview**. Providing answers will populate variables inside the documents I need filled with values relative to the questions the interview process asks.
I could then generate **plead papers**, documents and other filled forms in which I need to properly manage a case in a family court, legal process. 
Also in the future I would be able to use the data I stored to further generate other documents I will need. When I review the documents generated I can also provide additions, edits, and adjustments to each document independently and save those versions. 
Generating a document I would then be able to share as a **PDF file** that conforms visually to the regulations of the 
[Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf) so that I can submit the proper documentation for a judge  or client to review.

## Mission Critical Conditions

### Adjective Refactor

The documents that are given to the courts are called *plead papers* and the ones we are working on have, for example some adjectives describe people as husband and wife and this is nonsensical for same-sex marriages. 
It needs to be updated to something that makes sense to all points of reference.
The same goes for any other words throughout all the documents.

### Mobile First / PDF viewer
    
The courts require that the *plead papers* be in a PDF format. They are commonly read on tablets (or a mobile devices.) 
The pages we display need to be easily readable and navigable from a small screen and any document output needs to have a pdf option.


### Questions for Variable Values
    
Each document has variable inputs and some are repetitive or require the same logical input. 
These need to be organized into questions to reduce the redundancy of filling in the same answer for different portions of the documents.

### Document Generation and Editing
    
The answer values should be stored in an answer bank that can be reused to generate complete documents in compliance with standards defined in the
[Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf). These documents must also
be editable themselves for textual adjustments to any instance of the document. 

### Style Adherence

The *plead papers* must be compliant to the [Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf). 
There must also be a mobile-friendly viewable and editable version of the document.

### Privacy and Security

Security is everyone's responsibility. We will be required to process and store sensitive data and provide secure user data flows. 
This is tough and avenues for easily and safely reporting security concerns, events and incidents will be in place. 
A response plan should be maintained and security communication channels available publicly.  

Best practices for this situation need to be strictly enforced and proper defense posture assumed. Storage and retrieval of data needs to be in compliance with current 
[NIST Security Standards](https://www.nist.gov/cyberframework) and strong encryption should be prioritized over performance.  

Logging and user history chains will be required.

## General Component Overview

> Status - In Planning

The application's architecture is a microservice system and will be deployed using the [Civic Tech Labs's](https://www.codeforportland.org/CivicTechLab/) **AURA** project. It is a cluster of independent parts called *components*. 
The goal is to make each service *single purposed* and able to be developed *orthogonally*. 
It also allows the application developers to develop with the language they think works best for that situation. 

The intent is to break down our features into many focused services instead of one or few *monolithic* applications. 

### Front End

{{% notice info %}}Everything for front end should be **Mobile First**.
{{% /notice %}}

- **Public Website** - You are on it. :) Continual updates and content contributions can be made by clicking the edit link at the top of this page.  

- **Interview Wizard** - The interview wizard is an interface for a question and answers process. This will provide a user to provide values for the variable inputs that are needed in a generated document. A great example is provided by [DocAssemble](https://docassemble.org/demo.html).

- **Document Management Module** - The document manager is an interface that will allow the user to search and organize the various documents which have been generated, or they can create a new one.

- **Account Management Module** - This interface will be for account managers, to provide access rules to different users, view histories and reset credentials.

- **Profile Management Module** - Profiles represent a person involved to some degree with documents being generated. This interface will provide tooling for organizing those relations.

- **Dashboard Module** - The landing page for the application. It will control the login and service/module registrations to allow a user to navigate to different features.

### Backend

- **Auth(z) Manager** - Controls the authentication and authorization methods needed for user roles. and account security features.

- **Session Manager** - Orchestrates the persistence for a user.

- **Resource Manager** - A token dispensary that assigns and refreshes tokens.

- **Document Builder** - Builds the documents from the stored answers into the various formats required.

- **Stores Manager** - Connects to the *data stores* and performs various *CRUD* management.

- **Security Manager** - Provides encryption/decryption features for all the things.

- **Validation Manager** - Validates various forms, shapes and encodings of data.

- **Answer Bank** - Sensitive data store that holds the answers pertaining to the variable inputs inside the documents.

- **Document Stores** - The source documents that provide the templates for documents parsed and generated.

- **User Stores** - Sensitive data stores for user information.

- **Assets and Content Stores** - General store any component.


### Infrastructure

- **AURA** - A router utility for creating and managing data flow for communication to and from every component and API. 

- **Dockerfiles** - Containerization for each component allows for interoperability and CI flows.
