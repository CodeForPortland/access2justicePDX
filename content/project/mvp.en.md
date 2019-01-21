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

# Epic

**The Document Builder.** It will allow a user to provide an interactive guide for interviews to discover the information needed for generating plead documents. A user would be an employee at The Commons Law Center that would need to generate documents needed for specific matters. Profiles would be able to be used to create PDFs and editable documents that can be shared with the judge or a lawyer for a situational triage. It is like The Commons Law Center’s, “Hello”.

## Mission Critical Conditions

### Style Constraints
We have the freedom to make the numbers on the left of the plead documents to make sense. The style needs to be within the constraints described here [Appellate Courts Style Guide](https://www.courts.oregon.gov/publications/Documents/UpdatedStyleManual2002.pdf) so that I can submit the proper documentation for a judge or client to review.

### Adjective Refactor

The documents that are given to the courts are called *plead papers* and the ones we are working on have, for example some adjectives describe people as husband and wife and this is nonsensical for same-sex marriages. 
It needs to be updated to something that makes sense to all points of reference.
The same goes for any other words throughout all the documents.

### Mobile First / PDF viewer

{{% notice info %}}Everything for front end should be **Mobile First**.
{{% /notice %}}
    
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

Security is assured through using secure third party services and tokenizing users access to resources. 
