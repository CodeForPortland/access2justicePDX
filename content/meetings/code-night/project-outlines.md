---
title: Project Outlining 
description: We decided on teams and started breaking down the project into user stories. 
date: 2018-10-24
weight: 10
---

# Introductions

After we began with introductions and discussed the requirements for the project's **MVP**, which can be found on in the Project section.
We video hosted and screen shared for our teammate who could not be there physically and also to compensate for a lack of a projector.
Esti was assigned to be *back end lead* and Claire was assigned to help organize meetings and group work as *project manager*.

# Team Aggregations

We then formed teams based on the focuses we wanted, the assignments were as follows

| Name | Position | Preferred Languages |
|:----|:-----------|:---------|
|Brendan | front end, design, graphic |HTML, CSS, JS |
|Claire	| Project Manager, back end | JS |
|Esti	| Team Lead back end | Pyhton |
|Alex J | full stack | JS, Python, Ruby |
|Alex A | full stack, DevOps | JS, Ruby | 
|Ning	| back end  | JS, Java, ORDB, SQL |
|Rex	| Team Lead full stack, Dev Ops | JS, Go, Java, Python |
|Aidan	| full stack, DevOps| JS, Go, Python, CSS |

# What We Did

We agreed on using **GoogleDrive** as our main project management board and to have the sub teams use the repo's internal tools for focused concerns about the relative code base.

We started analyzing what the project would need and started breaking down the main features of the MVP into concerns for the front and back end.

Some tools were discovered that we thought would be good, a HTML to PDF (Sorry I did not get the tool name), a java library for document processing and [Docassemble](https://docassemble.org/).  

# MVP Granulation 

## Front End

- Dashboard - Needs to provide navigation to major features. 
- Interview UI - A step by step process for building and answer bank for **matters** and **profiles**
- Login - A login for *The Commons Law Center's* staff.
- Profile Manager UI - Profiles need to be searchable and related to matters and sensitive information.
- Document Manager UI - Documents would be organized into document stacks and *matters* which are cases and also related to multiple **profiles**.
- Settings - Basic settings for the applications visuals or configurations.
- Help - A WTF mode.
- About - The 411 on our team and supporters.

## Back End

- Profile Stores - Data stores for profile information, sensitive info, use redaction.
- Profile Index Stores - An index for profile resolution to separate sensitive info from related identities..
- Document Stores - A place to store the portions of a template for document generation.
- Security Module - Handles encryption and integrity checks.
- Authentication Module - Handles credential processing.
- Authorization Module - Handles the resource permissions.
- Store Manager - Handles data store CRUD systems.
- Logger - Provides logs for the system.
- Document Processor Module - Encodes text in to formatted documents. (PDF)

## Homework

Creating user stories and planning to have overviews of the system and data flows in a *UML* format by the time we meet up again in two weeks.
We are hoping to have some boiler plate code down to start integrating into [**AURA**](https://www.codeforportland.org/CivicTechLab/posts/agnosticqueries/).  
The back end team is planning to meet up in between now and our next meet up time and we all agreed to get checks on our work over Slack.