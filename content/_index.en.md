---
title: "Access2Justice"
---

# Access2Justice

{{% notice warning %}}This project and site is currently in development. Expect features and web pages to be unstable and change without notice.
{{% /notice %}}

# Support This Project

We are a volunteer team of hackers working with [The Commons Law Center](https://thecommonslawcenter.org) to make a difference in reducing the time and money it costs for people to have legal services.

{{% image src="/images/become_a_patron_button@2x.png" link="https://www.patreon.com/join/access2justice?" %}}

Here you will find information on the current projects, documentation and network status. If you want to **contribute** checkout our [GitHub](https://github.com/CodeForPortland/access2justicePDX/) and our [contribution guide](https://github.com/CodeForPortland/access2justicePDX/).


# HOW TO GET INVOLVED EASILY AND QUICKLY!

1. Go here: https://www.codeforportland.org/access2justicePDX/project/mvp/

2. Choose which microservice (module) within this project you want to contribute
(Remember: A microservice is basically one mini-app within this larger project.  
All these microservices talk with each other and that makes up the full Access2Justice

3. Check out the service's corresponding Waffle, which is a scrum board that shows outstanding tasks as defined in the GitHub. Talk with [Rex](rex@codeforpdx.org), Esti, or myself if you're not sure where to begin or need clarification on the existing tasks.

4. Set a waffle to in progress and do it!  Then move it to "done" when done and let the corresponding team (front end, back end, civic tech lab) know!

## Terms

- **MicroProject** - A specific set of features or facilities that need to be developed for the project and can be developed independently (*orthogonally*). 

- **Module** - Enclosed logic that provides inputs and outputs for communicating messages and data.

- **Manager** - Autonomous client that conducts factory processes and pipelines to process data or orchestrate services. 

- **Management** - Interactive client or tool kit for users to provide system engagement. 

- **Service** - Something that takes a request and returns a response.

## Front End MicroProjects

|Project | Repo | Board|
|:---|:----:|:---:|
| WWW | [GitHub](https://github.com/CodeForPortland/Access2JusticePDX) | [Waffle.io](https://waffle.io/CodeForPortland/access2justicePDX/join) |
| Dashboard | [GitHub](https://github.com/CodeForPortland/a2j-front-end_dashboard) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-front-end_dashboard/join) |
| Document MGT Module | [GitHub](https://github.com/CodeForPortland/a2j-front-end_document-manager) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-front-end_document-manager/join) |
| Interview Wizard | [GitHub](https://github.com/CodeForPortland/a2j-front-end_interview-wizard) | Not Setup Yet |
| Profile MGT Module | [GitHub](https://github.com/CodeForPortland/a2j-front-end_profiles) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-front-end_profiles/join) |
| Account MGT Module | Not Setup Yet | Not Setup Yet |

#### Interview Wizard

This is what the user will see when they will enter their information.  This will guide them through entering the necessary information to generate the documents.

#### Document Management Module

The document manager is an interface that will allow the user to search and organize the various documents which have been generated, or they can create a new one. 
This can help them fine-tune documentation as needed beyond what the wizard populates to suit the particulars of the case. 

#### Profile Management Module

Profiles represent a person involved to some degree with documents being generated. This interface will provide tooling for organizing those relations.

#### Account Management Module

This interface will be for account managers, to provide access rules to different users, view histories and for basic administrative tooling.

#### Dashboard 

A navigation view and landing page that accepts module registration and allows a user to access the different services.


## Back End MicroProjects

|Project | Repo | Board|
|:---|:----:|:---:|
| Data Store Manager | [GitHub](https://github.com/CodeForPortland/a2j-back-end_data-store-manager) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-back-end_data-store-manager/join) |
| User Manager | [GitHub](https://github.com/CodeForPortland/a2j-back-end_user-manager) | [Waffle.io](https://waffle.io/CodeForPortland/a2j-back-end_user-manager/join) |
| File Services Module  | Not Setup Yet | Not Setup Yet | 
| Document Builder Module | Not Setup Yet | Not Setup Yet | 
| Security Manager | Not Setup Yet | Not Setup Yet | 

#### User Manager

An orchestrator for initiating session, login and registrations procedures and for providing responses to the front end clients.

#### File Service Module

The client for initiating document builds for providing downloadable or shareable files for a front end client. 

#### Document Builder Module

Builds the documents from profiles and templates into the various documents in the required formats.

#### Data Store Module

Manages the data base connections and provides general and secure *CRUD* tooling for non-public clients.

#### Security Manager

Provides authentication and authorization tokens, also organizes and initiates hashing procedures and encryption/decryption for all the things.

