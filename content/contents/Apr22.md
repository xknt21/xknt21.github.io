---
date: 2025-04-22T01:06:59+09:00
draft: false
title: '[Group Documentation] April 22 2025'
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
# Recognition Application for Cats after SNR Program   
## Problem Statement     
Urban animal shelters in many regions—such as Taiwan—are overburdened and face legal or ethical restrictions against euthanizing animals. As a result, many cats undergo SNR (Shelter, Neuter, Return) programs and are returned to city streets. Post-release, shelters lose track of these cats, making it difficult to monitor their health or facilitate potential adoptions. There's a need for a data-driven system that allows society to stay connected to these animals, even after release.   
 
## Data Acquisition   

### Sources of Data:   
Existing public cat image datasets such as the [Crawford Cat Dataset on  Kaggle](https://www.kaggle.com/datasets/crawford/cat-dataset/data).   
Photos taken by animal shelters before cats are released (multiple angles per cat).   
Optional: user-submitted photos via mobile apps for additional training and validation.   

### Data Collection Methods:   
Collaborate with animal shelters to collect and organize multi-angle images of cats pre-release.
Apply data augmentation techniques to increase dataset size and variety.
Use OpenCV or other preprocessing libraries to clean and normalize the dataset (e.g., cropping, resizing).
Web scraping from shelter websites, google photos where we can see users upload photos and reviews, SNS.   
### Analytical Tools and Techniques:   
Implement Convolutional Neural Networks (CNNs) to enable visual recognition of individual cats.
Test models like YOLOv2 or MobileNet for real-time, efficient image recognition on mobile devices.
Apply noise reduction, normalization, and image labeling to ensure dataset quality.
Use Siamese Networks or re-identification models to distinguish similar-looking cats.   

### Model Evaluation:   
Split the dataset into training and testing sets.
Measure inference precision and performance to evaluate the model’s effectiveness.


## Data Presentation

### Visualization and Engagement Strategies:   
* Develop a mobile application with a built-in cat recognition camera feature.
* Upon recognition, the app shows a profile of the cat (name, breed, last vaccination, adoption contact info).
* Include adoption status, last known health updates, and geolocation tagging.
* Visualize model performance with metrics such as precision and recall via dashboards.   

## User Experience Features:     

* Citizens can scan street cats using their phones to learn more or adopt.
* Shelters can track the reappearance of released cats and monitor wellbeing.
* Build a feedback loop where users can report injuries or concerns about specific cats.   

## Objective/Goals   

### Promote Adoption:    
Enable adoptions even after cats are released from shelters.   
### Enhance Social Connection:    
Create a cat-friendly environment by integrating cats into the urban social fabric.   
### Track Post-Release Wellbeing:    
Monitor the condition of cats after release to improve urban animal welfare.   
### Verify Vaccination Status:    
Instantly identify if a cat has been vaccinated, promoting safe and informed interactions between humans and cats.         
 
## Target Clients and Users

### Primary Clients:   
Animal shelters and SNR programs.
### End Users:   
Citizens, animal lovers, and potential adopters.`   


## Research References:
https://www.kaggle.com/datasets/crawford/cat-dataset/data 
https://arxiv.org/pdf/2501.02112v1
https://hal.science/hal-03501010/
https://link.springer.com/chapter/10.1007/978-3-030-59612-5_7
https://paperswithcode.com/paper/siamese-networks-for-cat-re-identification

###  Notes:
There are websites/community pages, where people post their cats with multiple pictures of the same cat, and refer to the syllabus on what to do next. For now, writing a good project proposal
- Problem elicitation/background
- Related application
- Literature review/government reports/any papers

# Brainstorming notes: (Participatory Budgeting System)
## Decide Madrid:
Link:
https://decide.madrid.es/ 
https://congress.crowd.law/files/decide-madrid-case-study.pdf (further details and documentation)	
Explanation: Website where you can make proposals, vote in citizen consultations, propose, support, or vote on projects with participatory budgets, decide on municipal regulations, and open debates to exchange opinions with other people.
## Consul:   
Link:
https://consulproject.nl/en/ (Website)
https://consulproject.nl/assets/documents/consul_executive_dossier_nl.pdf (further details and documentation)
Explanation: 
Consul is the most comprehensive digital tool for citizen participation, enabling an open, transparent and democratic government.
### Ideas:
We could potentially introduce a system that filters out non-sense inputs from the citizens.
Another idea is to create an approval system using a machine learning model or NLP model to filter out suggestions that are most likely not approved by the government or implement a system where a certain suggestion must reach a certain threshold to either be implemented or suggested in the first place. 


# Low-Light Area Detecting Software:

## Problem Statement:

Inadequate street lighting poses serious risks to public safety, including increased crime rates, higher chances of accidents, and reduced visibility for pedestrians and vehicles. Many urban and suburban areas lack comprehensive monitoring systems to identify regions with poor night-time illumination. Manual surveys are time-consuming, costly, and often outdated by the time they are compiled. There is a pressing need for an automated, scalable solution that can analyze geotagged nighttime imagery to detect and map low-light areas. 
## Objective Statement:
This software aims to utilize machine learning and image processing techniques to identify underlit regions using publicly available or crowdsourced street-level images and generate a dynamic heatmap to aid city planners and safety authorities in prioritizing lighting improvements.
## Data Acquisition:
Data will be obtained from open-source street view images available through sources like Google StreetView API. 
Further, we will be able to train a machine learning model to detect the presence of street lamps using images present on the Open Source Image Dataset V7 by Google Developers. 
The images from that dataset will be used for all the training, validation, and testing processes. As for the geotagged images, we will primarily use StreetView API, and we will also collect a few images ourselves.
## Data Processing:
Image processing will be used in this project idea for detecting streetlights. First the image will be segmented, and then the model will detect the presence of the streetlight. The YOLOv8 pretrained machine learning model will be used for this purpose.
## Data Sources:
Google StreetView API: https://developers.google.com/maps/documentation/streetview/overview
Open-Source Image Dataset V7:
https://storage.googleapis.com/openimages/web/index.html

## Similar Idea:
https://umap.openstreetmap.fr/ja/map/map_285407#16/34.9972/138.4414
## Task: (Until April 24, 2025)
Project proposal, it has to have the problem definition , related applications and literature or governmental report. Data or method..how it should be established.
Literature survey with similar applications and mention pros and cons. Make sure that everyone is on the page about the idea . Decide what we actually want to do. 


![Imgur](https://i.imgur.com/Oy0vVLG.jpg)   