---
title: MVP
weight: 1
---

# MVP

The MVP will be an application for generating **pdf documents** from an **interview process** that can then be *edited*, *shared* and *viewed* on a mobile device via a role-based access system.

The app will initially be for internal use only, by *The Commons Law Center*. The idea is to create a more effective way to fill in large and confusing legal forms.
Essentially we are creating a **Turbo Tax** for family court. 

## Epic

As a *The Commons Law Center* lawyer I want to use a mobile application to make my workload easier and to more effectively manage a case. I would want to access on a tablet device, a series of questions (**an interview**) to answer that provides values to the variable segments of  
**plead papers**, documents and forms in which are needed for me to represent a client in a family court legal process. 
I would be able to save these documents and provide fine grade edits, adjustments and changes while reviewing the saved documents. 
I would also need to generate future documents from *the interview* that I can view from a mobile device to share or go over with a client. 
I would also need to be able to download/share these documents in a pdf file that conforms visually to the regulations of the 
[Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf) so that I can submit documentation for a judge to review during court proceedings.

## Mission Critical Conditions

### Adjective Refactor

The documents that are given to the courts are called *plead papers* and the ones we are working on have for example, 
adjectives that describe people as husband and wife, and due to same-sex marriage it needs to be updated to something that makes more sense.
The same goes for other adjectives/pronouns/...etc throughout all the documents.

### Mobile First / PDF viewer
    
The courts require that the *plead papers* be in PDF format and commonly read them on tablets or some mobile devices. 
The pages we display need to be easily readable and navigable from a small screen and any document output needs to have a pdf option.


### Questions for Variable Values
    
Each document has variable inputs. These need to be organized into questions to reduce the redundancy of filling in the same answer for different portions.

### Document Interpolation
    
The answer values should be stored in an answer bank that can be reused to generate complete documents in compliance with standards defined in the
[Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf). These documents must also
be editable themselves for literal adjustments to each instance of the document. 

### Style Adherence

The *plead papers* must be compliant to the [Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf). 
There must also be a mobile-friendly viewable and editable version of a document.

### Privacy and Security

Security is everyone's responsibility. Sensitive data is needed to be stored and shared and secure user access is tough. 
Best practices for this situation need to be strictly enforced. Storage and retrieval of data needs to be in compliance with current 
[NIST Security Standards](https://www.nist.gov/cyberframework) and strong encryption should be prioritized over performance.  

Logging and history chains will be required.

## General Component Overview

> Status - In Planning

### Front End

{{% notice info %}}Everything for front end should be **Mobile First**.
{{% /notice %}}

- Public Website - You are on it. :) Continual updates and contributed content can be made by clicking the edit link at the top of this page.  

- Interview - A series of questions that can asses a user to provide answers to an answer bank, an example can be found here by [Docassemple](https://docassemble.org/demo.html)

- Mobile Viewer - Documents generated are editable and shareable from here.

- User Controls - Basic user accounts can be managed from here.

- Case Dashboard - Various controls that allow interactions with history and current case contexts.

### Backend

- Auth(z) Manager - Controls the authentication and authorization methods needed for user roles. and account security features.

- Session Manager - Orchestrates the persistence for a user.

- Resource Manager - A token dispensary that assigns and refreshes tokens.

- Document Builder - Builds the documents from the stored answers into the various formats required.

- Store Manager - Connects to the *data stores* and performs various CRUD management.

- Security Manager - Provides encryption/decryption features for all the things.

### Infrastructure

- AURA - A router utility for creating and managing data flow for communication to and from every component and API. 

- Dockerfiles - Containerization for each component allows for interoperability and CI flows.
