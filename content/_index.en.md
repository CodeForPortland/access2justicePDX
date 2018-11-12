---
title: "Access2Justice"
---

# Access2Justice

{{% notice warning %}}This project and site is currently in development. Expect features and web pages to be unstable and change without notice.
{{% /notice %}}

We are a volunteer team of hackers working with [The Commons Law Center](https://thecommonslawcenter.org) to make a difference in reducing the time and money it costs for people to have legal services.

Here you will find information on the current projects, documentation and network status. If you want to **contribute** checkout our [GitHub](https://github.com/CodeForPortland/access2justicePDX/) and our [contribution guide](https://github.com/CodeForPortland/access2justicePDX/).

# Support Us

Want to help support this project? We have a [Patreon site](https://www.patreon.com/access2justice/overview) or buy us a beer at one of our coding night's [meetup](https://www.meetup.com/Code-for-PDX/).

# HOW TO GET INVOLVED EASILY AND QUICKLY!

1. Go here: https://www.codeforportland.org/access2justicePDX/project/mvp/

2. Choose which microservice (module) within this project you want to contribute
(Remember: A microservice is basically one mini-app within this larger project.  
All these microservices talk with each other and that makes up the full Access2Justice

3. Check out the service's corresponding Waffle, which is a scrum board that shows outstanding tasks as defined in the GitHub. Talk with [Rex](rex@codeforpdx.org), Esti, or myself if you're not sure where to begin or need clarification on the existing tasks.

4. Set a waffle to in progress and do it!  Then move it to "done" when done and let the corresponding team (front end, back end, civic tech lab) know!

## Front End MicroProjects

### Interview Wizard

This is what the user will see when they will enter their information.  This will guide them through entering the necessary information to generate the documents.

### Document Management Module

The document manager is an interface that will allow the user to search and organize the various documents which have been generated, or they can create a new one. 
This can help them fine-tune documentation as needed beyond what the wizard populates to suit the particulars of the case. 

### Profile Management Module

Profiles represent a person involved to some degree with documents being generated. This interface will provide tooling for organizing those relations.

### Account Manager Module

This interface will be for account managers, to provide access rules to different users, view histories and for basic administrative tooling.

### Dashboard 

A navigation view and landing page that accepts module registration and allows a user to access the different services.

## Repos


|Project | Repo | Board|
|:---|:----:|:---:|
| WWW | [GitHub](https://github.com/CodeForPortland/Access2JusticePDX) | [Waffle.io](https://waffle.io/CodeForPortland/access2justicePDX/join) |
| Dashboard | [GitHub](https://github.com/CodeForPortland/a2j-front-end_dashboard) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-front-end_dashboard/join) |
| Document MGT Module | [GitHub](https://github.com/CodeForPortland/a2j-front-end_document-manager) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-front-end_document-manager/join) |
| Interview Wizard | [GitHub](https://github.com/CodeForPortland/a2j-front-end_interview-wizard) | Not Setup Yet |
| Profile MGT Module | Not Setup Yet | Not Setup Yet |
| Account MGT Module | Not Setup Yet | Not Setup Yet |


## Back End MicroProjects


### Authorization Manager

A token dispensary that grants resource access and privilege.

### Session Manager

A token dispensary that organizes persistence for a user.

### Resource Manager

A token dispensary that assigns and refreshes tokens.

### Document Builder

Builds the documents from the stored answers into the various formats required.

### Stores Manager

Connects to the *data stores* and provides general *CRUD* procedures.

### Security Manager

Provides encryption/decryption features for all the things.

### Validation Manager

Validates various forms, shapes and encodings of data.

### Answer Bank

Sensitive data store that holds the answers pertaining to the variable inputs inside the documents.

### Document Stores

The source documents that provide the templates for documents parsed and generated. May use Amazon RDS. 

### User Stores

Sensitive data stores for user information.

### Assets and Content Stores

General stores for any component.

