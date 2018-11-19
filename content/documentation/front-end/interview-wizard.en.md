---
title: Interview Wizard Module
description: An Angular6 Module that provides the interview process that collects personal information.
weight: 20
updatedon: 2018/11/18
---

Consider this the "Turbo Tax"-style front end of the project. The interview wizard is a module that petitioners (and in the case of the MVP, interviewers) can use to fill out petitioner and respondent data.  The data will pull dynamically based on what still needs to be filled out for the user.  

## Features

*Dynamic, Guided Questionnaire* - Guided, responsive user questionnaire for assembling the data needed to populate a variety of family law-based legal documents

*Built-in Legal Logic* - Logic to hide or request all the necessary features needed to handle family law cases comes built in within this module.  This logic is modular and can be swapped out or rewritten to handle different types of legal cases in the future.  All the logic included will (prior to release) be verified by a practicing, accredited legal team to ensure nothing is missing or runs afowl of any existing data handling regulations.

*Help Text* - Tiered help text will be available to any user that does not understand the question.  This will include clarification on which documents to refer to for looking up specific legal items, definition clarification, etc.  

*Flexible Question Flow* - Questions shown are not hard-coded in the application but pull dynamically from an external data store that can recognize and pull the necessary questions depending on the case and legal situation.

*Strong Application-Layer security* - Information deemed sensitive will be sent to the user to view in a identity-safe way (for example, a User's SSN would be displayed as ***-**-0000 with the last 4 zeroes being the last 4 numbers for verification purposes)


## Interface

...coming soon

## Contributors

{{% ghcontributors owner="CodeForPortland" repo="a2j-front-end_interview-wizard" %}}
