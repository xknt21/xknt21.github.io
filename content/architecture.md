---
draft: false
title: 'System Architecture'
---
**Introduction**  
This document is based on the high-level description of the software architecture for the “Smart Re-Identification System for Stray Cat Post-TNR Programs” designed to assist volunteers such as individual caretakers, rescue groups, and facilitate the management and adoption of stray cats by identifying previously recorded individuals using AI-powered image recognition.

This document focuses on the architecture and data flow from the perspective of a volunteer account user. It outlines the major components involved in the system and explains how these components interact through a clearly defined pipeline.

All diagrams and descriptions provided in this document highlight the flow of data and responsibilities of each component, emphasizing how a user can upload an image of a stray cat, have it processed through a re-identification model, and receive the most relevant match result. This system aims to support animal welfare efforts by reducing redundant procedures and ensuring better record-keeping of stray cats in the community

**Container Diagram**  
This container diagram illustrates the system's components, how they communicate, and their individual responsibilities. For our system, a volunteer account will be able to access the system through a mobile application. 

![Imgur](https://imgur.com/IhNORuM.png)
The System API communicates with the two software systems and exchanges data with the systems. The first system is the Account Management System which is responsible for the management of accounts as seen in registration and verification. Then, the Re-identification (Re-ID) System is responsible for re-identifying the cats based on user inputs. Moreover, the two software systems interact with different databases. The Account Management System reads from and writes to the User Information Database when users put action on their accounts. The Re-ID system only reads from the Cat Database where all the data, including the feature vectors used for matching and the profile information, is stored.

**Pipe and Filter Diagram**  
This diagram visualizes the process of a volunteer account user uploading an image of a stray cat as the input of the system and receiving the matching result as an output. If the result shows a match, the matching cat profile will be displayed to the user.

![Imgur](https://imgur.com/RYxbQmp.png)

The following table is used to describe the corresponding processes involved throughout the pipe and filter diagram

| Name | Description |
| :---- | :---- |
| Upload Image | An user uploads an image of a stray cat |
| Object Detection | Detects the cat in the image |
| Cropping | The surroundings is cropped off from the image |
| Normalization | The image is adjusted into the size of (224, 224\) pixels |
| Feature Extraction | Extracting the feature vectors from the uploaded images |
| Cat Database | The database stores the images and information uploaded by the animal hospital accounts when adding new cat profiles. It also stores the feature vector extracted from the uploaded image. |
| Re-identification (Re-ID) | This process compares the feature vector of the uploaded image and the feature vectors from the cat database and the cat with the highest confidence score (in decimals with maximum of 1\) will be reflected. |
| Result | If the highest confidence score from the re-ID process is lower than 0.6, the result is a message showing “No matches found”. If the highest confidence score is above 0.6, the confidence score will be shown in natural numbers rounded up to one decimal place with a percentage sign with an additional line of “Very likely match” for confidence scores larger than 0.8 and “Possible match \- needs confirmation” for confidence scores between 0.6 and 0.8. |
| Cat Profile | The cat profile is made up of four to nine images and the information of the cat both stored in the cat database |
| Display Profile | The cat profile will be displayed if the confidence score is higher than 0.6 |

**Technology Stack**  
This Smart Re-Identification System for Stray Cats Post-TNR Program employs a modern, multi-layered architecture that combines mobile development, artificial intelligence, and web services. The frontend is built using react native with expo, providing cross-platform mobile development capabilities for both ios and android devices. In this case, expo is used for rapid prototyping as it is the most suitable considering the project circumstance. The mobile application utilizes typescript for type safety and leverages expo's ecosystem including expo-camera for photo capture, expo-image-picker for gallery selection, and expo-router for navigation. 

The backend is powered by python flask, serving as a RESTful API that handles image processing and cat identification requests. The AI component is built on tensorflow and ultralytics YOLOv8, where YOLOv8 performs cat detection and bounding box extraction from uploaded images, while a custom embedding system processes the cropped cat images to generate feature vectors for matching. The system uses OpenCV for image preprocessing and manipulation, including resizing and color space conversions. 

Data persistence is handled through SQLite for local storage and pickle for storing pre-computed cat embeddings. The communication between the mobile app and backend is facilitated through HTTP REST APIs using Axios for network requests, with the backend running on port 5000 and serving JSON responses. The project also incorporates react navigation for tab-based navigation, expo haptics for tactile feedback, and various UI components from the expo ecosystem. This tech stack enables real-time cat re-identification, medical record management, and user role-based access control, making it suitable for a prototype before expanding or evolving this project out and then deploying it.

