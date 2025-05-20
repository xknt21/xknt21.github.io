---
date: 2025-04-24T01:06:59+09:00
draft: false
title: '[Group Documentation] May 6 2025'
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
# Summary of Activities
On May 6, our group focused on clarifying key system behaviors and preparing in-depth technical questions for our upcoming consultation with the professor. This work session was dedicated to translating our conceptual design into more concrete technical concerns, especially related to cat image handling, recognition, and re-identification processes.

# Technical Planning and Discussion
We discussed the expected photo upload process from general users, particularly from smartphones. While the feature itself was already listed as a requirement, we focused on exploring the technical details and potential user behaviors.
We identified the need to accept .jpg images from mobile users and started researching what image formats would be optimal for internal processing and model input. We agreed to seek expert input on whether conversion to other formats (e.g., .webp, .tiff) is recommended for performance or quality reasons.
We talked about challenges users might introduce, such as blurry images or inconsistent angles, and decided to ask about data pre-processing techniques to handle these cases effectively.

# Questions for Expert Consultation
We prepared a list of specific technical questions to ask our professor or external advisors. These are aimed at improving the robustness and scalability of our AI system.

## Recognition Dataset Balance
- What ratio of cat images to non-cat images should we aim for when testing the object detection model?

## Re-identification Dataset Requirements
- What is the minimum number of images per individual cat that we should request from shelters?
- Are there specific angles (front, side, top) or lighting conditions that we should prioritize?

## Image Format & Handling
- Users will upload .jpg files. What is the best internal format to convert them to for training and inference?
- What tools or libraries are recommended for handling this conversion efficiently?

## Data Preprocessing
- What preprocessing methods are helpful to deal with partially blurry images?
- What techniques have you personally found essential in preparing data for training image models?

## Model Training Stability
- During training, if the model’s parameters don’t converge, what strategies can be applied?
- If you haven’t encountered this issue, is it mainly because the dataset was sufficiently large?

## Multi-Model Integration Concerns
- We plan to integrate multiple models (e.g., detection and re-identification). What are the typical problems (e.g., latency, conflicts) and how can we prepare for them?

# Key Insights and Planning Outcomes
We realized that designing a user-friendly upload flow is just one side of the challenge — we also need to make sure the image data quality is good enough for reliable recognition.
The importance of dataset quality and structure was emphasized, especially in terms of representing each individual cat adequately for re-identification.
Our upcoming discussions with professors will focus on real-world experiences and best practices, rather than just theoretical knowledge.

# Focus of the Day: Designing User Flow and Shelter Interaction Logic
On May 8, our team focused on designing detailed user workflows for both general users (citizens/volunteers) and shelter/organization staff. This session aimed to visualize how the system will manage image uploads, cat identification, profile handling, and communication between shelters and the app.

## User Flow (Citizens/Volunteers)

### User Entry Options:
- Can start without signing up.
- Optional sign-up flow includes: full name, email, phone number, and password.

### Main Flow:
- User uploads a photo of a stray cat using the app.
- The system performs cat recognition:
  - If a match is found, the user sees the cat’s profile page, which contains:
    - Option to report injured or want to adopt.
  - If no match is found:
    - User is given the option to report a problem.
    - A form allows the user to share location and photo.
    - If signed in, personal info is auto-filled; if not, the user must input:
      - Full name
      - Phone number
      - Email
- The report is sent to the shelter, and a confirmation email is issued to the user’s email address.

## Shelter / Organization Flow

### Designed administrative functions for shelters:
- Add New Cat
- Update Cat Profile

### When updating or adding a profile:
- Upload multiple images (exact number TBD)
- Enter cat details:
  - Approximate age
  - Vaccination status (including date if available)
  - Whether the cat is neutered
- Also discussed the need to specify which shelter/organization owns the profile.
- Edit profile/pics functionality was included for future flexibility.

# Notes and Open Questions
- How many pictures per cat are necessary for reliable re-identification?
- Should vaccination input require both status and date?
- What should the fallback process be when recognition fails repeatedly?

# Outcomes
- Defined end-to-end user flows from photo upload to shelter contact.
- Visualized system branching logic based on recognition results.
- Clarified data requirements for cat profiles from shelters.
- Designed interaction model between general users and shelters through forms and email notifications.
