---
title: Getting and Going
description: Our kickoff sprint.
date: 2018-11-01
author: Rex
---

# Our Kickoff Sprint 11/01/2018

Almost to the end of our kick off sprint, here's an update on our progress...

## User Stories and Project Tools

Things are still a bit ambiguous as to who is responsible for what and we are granulating our understandings and time availabilities as we go. 
Hats were passed out but all of us are (and encouraged) to wear multiple.
Everyone agreed to use **Google Drive** as our main task board and it's coming together. 
A few modules have completed their user stories and we are scheduled to finish up the rest this weekend at a meet and hack over at Oui Press.


## Creatives

Wireframes have been made for a few facets of the document manager and interview wizard. The WYSIWYG had a few refactorings.

### The Document Management Module

A wireframe depicting a question for the **Interview Wizard** it shows a modal that provides a form for a user to fill out. This will be the primary facility for collecting information for an answer bank which will hold the information that will generate the *plead papers*.
![Wireframe for a question in the interview wizard](/access2justicePDX/images/wireframes-mocks/wizard-question-modal-wireframe.png)

The idea here is to have a *plead paper* be editable after it is generated. The need range for the styling isn't large so the tooling options should not require much space. 
![Wireframe for WYSIWYG](/access2justicePDX/images/wireframes-mocks/wysiwyg-wireframe.png)

This is a mock of the tool bar and its editable section. **Note**: That it's not within the view frames, or control panel that it should be placed in. 
![Mock for WYSIWYG](/access2justicePDX/images/wireframes-mocks/wysiwyg-mock.png)

This is a wireframe of the **control panel** that shows the current document's (aka *plead paper*) meta data.
![Wireframe for Control Panel](/access2justicePDX/images/wireframes-mocks/control-panel-wirefram.png)
  
### Entity Relationship Diagram

This is a first draft of the relations the data will have. It displays aggregated classes on the top two rows and data stores that hold static values on the bottom.
This should give an idea as to how to formulate our data bases and the logic to process that data.
![Wireframe for Control Panel](/access2justicePDX/images/data-graphs/entity-relationship-diagram.png)
 

## Engineering

Work has begun on the **Dashboard Module**, **Interview Wizard**, and **Document Management Module**.

The **Dashboard Module** does not yet support registration but it provides an insight to how it should look and function.

![Dashboard Screen Capture](/access2justicePDX/images/showcase/dashboard.png)

The **Login Component** may be factored out to it's own module however it right now functionally communicates to our [**AURA**](https://www.codeforportland.org/CivicTechLab/posts/agnosticqueries/) router and calls a mock [*Authentication Service*](https://github.com/CodeForPortland/CTL-Authentication-Service)

![Login Screen Capture](/access2justicePDX/images/showcase/login.png)

# Closing Thoughts

Despite the pain points of a new development process and new team, everyone seems eager to contribute and we are looking forward to seeing how our agnostic approach to tech stack contributions evolves.