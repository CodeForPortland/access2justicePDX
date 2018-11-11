# Access2Justice 
>by [The Commons Law Center](https://thecommonslawcenter.org) and [Code4PDX](https://codeforpdx.herokuapp.com)

We are a volunteer team of hackers working with [The Commons Law Center](https://thecommonslawcenter.org) to make a difference in reducing the time and money it costs for people to have legal services.

Here you will find information on the current projects, documentation and network status. If you want to **contribute** checkout our [GitHub](https://github.com/CodeForPortland/access2justicePDX/) and our [contribution guide](https://github.com/CodeForPortland/access2justicePDX/).

This current repo is the code base (aka **The WWW**)for the public facing site of the project. It will provide and collect information regarding project progress and releases, documentation, server status, contacts, and contribution information. To get involved with the project checkout the [WWW](https://www.codeforportland.org/access2justicePDX) or read below. :)

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

# Contributing To The WWW

There are multiple ways you can help out. Contributions should be made through **Pull Requests(PRs)**, from a personal fork or from your own branch. Editing the content can be done directly from GitHub, however, any logic contribution is developed and tested first, in your own enviornment, before a *PR* should be made.

## Locally
1. Clone the repo to your local development environment (check below for instructions)

2. Develop/Write - [Hugo](https://gohugo.io) provides static web page generation based on the hierarchy of the information architecture (IA). [Girafe Academy](https://youtu.be/qtIqKaDlqXo) has some great videos on giving a quick overview of the different features *Hugo* provides.

3. Make a PR - Always work in your own branch (or fork). Label your PR's to the <strike>[contribution standards](#)</strike>(comming soon) stated in the contribution guide.

4. Declare your PR - When your *PR* is made, let us know in *Slack*. We are interested in what you did and what you think. :) 

# Local Deploy

1. Make sure you have [Hugo](https://gohugo.io) installed in your local dev environment. 
2. Clone repo
```bash
git clone git@github.com:CodeForPortland/access2justicePDX.git
```
3. Install the theme submodule
```bash
git submodule init
git submodule update
```
4. Launch with **Hugo's** dev server
```bash
hugo -b localhost serve --disableFastRender
```
