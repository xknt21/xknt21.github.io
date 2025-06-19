---
date: 2025-06-10T01:06:59+09:00
draft: false
title: '[Group Documentation] Jun 10 2025'
summary: 
description:
author:
showToc: true
TocOpen: false
hidemeta: false
comments: false
hideSummary: false
ShowReadingTime: true
ShowPostNavLinks: true
---

This week, we worked on completing the diagram involved in the re-identification system for stray cats post-TNR.

## Defined System Overview :
Sorted the basic purpose of the application in order to minimize repetitive medical procedures for stray cats and assist better tracking post-TNR.
Planned out interaction between administrators , volunteers , animal hospitals and central database.    

## Use Case Diagram :
Spotted 19 functional use cases including sign up , upload image , view cat profile , manage ID results.
The use case diagram demonstrated actor-function relationships.   
**Group actors are :**    
Volunteers    
Animal Hospital Staff   
Administrators      

## Sequence Diagram : 
Demonstrated interaction between volunteers and the system for account management operations including sign up , login , modify and delete.
Included system components such as Account Portal , Volunteer DB , and Main Page Interface.

## Activity Diagram :
**The diagram had separate workflow including :**     
Animal Hospital Staff    
Volunteers    

## Class Diagram :
Abstract User class established inheritance structure.     
**Methods included :**    
uploadCatImage()    
verifyDocuments()    
addCatProfile()    
**Specialized classes are :**     
IndividualVolunteer     
OrganizationVolunteer    
HospitalStaff    
Admin

## Functional Specification Tables :
Data inputs and outputs , use cases and comments for each module were defined.    
**Broken down into six system modules:**   
Account Management     
Image Submission and Matching   
Cat Profile Management    
Profile Viewing    
System / User Management    
Report Handling and Match Validation
