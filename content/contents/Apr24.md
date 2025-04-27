---
date: 2025-04-24T01:06:59+09:00
draft: false
title: '[Group Documentation] April 24 2025'
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

# Smart Re-Identification Application for Stray Cats Post-SNR Program

## Problem Elicitation / Background  
Urban animal shelters, particularly in regions like Taiwan, are heavily burdened and face legal or ethical restrictions against euthanizing animals. Following the Shelter-Neuter-Return (SNR) program, many cats are released back into the urban environment without systematic tracking, making it difficult to monitor their wellbeing or promote their adoption.  
There is a growing societal need for a solution that maintains a connection with these cats after their return, fostering animal welfare and enabling post-release care and adoption opportunities.

## Related Applications  
Current applications primarily focus on pet identification and lost pet recovery (e.g., PetFinder, PawBoost). However, few address the unique needs of tracking and re-identifying community cats post-SNR programs at a societal scale.  
Additionally, existing apps generally require owners' cooperation, while stray cats post-SNR lack dedicated guardians, highlighting a gap in service.

## Literature Review and Government Reports  
- **Crawford Cat Dataset (Kaggle)**: A dataset containing labeled images of cats, useful for training initial models.  
- **"Siamese Networks for Cat Re-identification" (PapersWithCode)**: Demonstrates the efficacy of Siamese Networks in distinguishing between highly similar individual animals.  
- **Government Reports**: Recent e-petitions in Taiwan indicate increasing public demand for humane stray animal management without euthanasia, emphasizing the importance of SNR initiatives.  
- **Other References**:  
  - [arXiv 2501.02112v1](https://arxiv.org/pdf/2501.02112v1) - Latest methods for animal re-identification.
  - [HAL Archive Paper](https://hal.science/hal-03501010/) - Research on sustainable animal tracking.  
  - [Springer Book Chapter](https://link.springer.com/chapter/10.1007/978-3-030-59612-5_7) - Machine learning for animal welfare solutions.

## Vision and Goals  
- **Promote Adoption**: Maintain adoption opportunities post-release.  
- **Enhance Social Connection**: Build a cat-friendly urban culture through awareness and interaction.  
- **Track Wellbeing**: Monitor health and safety of community cats after release.  
- **Verify Vaccination**: Enable instant verification of vaccination status through recognition.

## Objectives - Features to be Realized  
- Develop a mobile application with real-time cat recognition via camera input.
- Display cat profiles including health, vaccination, and adoption information.
- Geolocation tagging to track areas where cats are frequently sighted.
- User feedback system to report injuries, illnesses, or sightings.
- Dashboards to visualize model performance (precision, recall).

## Scope (How Big the Problem Is)  
Tens of thousands of cats participate in SNR programs annually in Taiwan alone. Urban environments are dynamic and cats are mobile, making continuous manual tracking impossible without technological aid. This project targets urban centers with a dense SNR population, aiming to scale nationally or internationally.

##　Limitations and Risks  
- **Accuracy Challenges**: Recognizing individual cats with subtle visual differences may cause errors.
- **Data Quality**: User-submitted images may be blurry, low-quality, or mislabeled.
- **Privacy Concerns**: Collecting geolocation data needs careful ethical consideration.
- **Adoption Reluctance**: Users may scan cats but few may move forward with adoptions.

## Sustainability (Future Extensions)  
- Integrate with shelter databases for automatic record updates.
- Expand to other species (e.g., dogs in TNR programs).
- Implement reward systems to encourage citizen participation.
- Utilize blockchain for decentralized, transparent health record-keeping.

## Data Acquisition  
- **Sources**: Public datasets, shelter photo archives, user-submitted images.
- **Methods**:  
  - Collaboration with shelters for multi-angle pre-release photos.  
  - Data augmentation techniques to artificially expand datasets.  
  - Web scraping from shelter websites and social media.
  - Preprocessing using OpenCV (cropping, noise reduction, normalization).

## Data Processing  
- Apply image preprocessing (cropping, resizing, normalizing).
- Organize datasets by unique individual cat ID when available.
- Augment data for robustness against lighting and angle variations.

## Data Science Techniques  
- **Recognition Models**:  
  - Convolutional Neural Networks (CNNs) for feature extraction.
  - YOLOv2 and MobileNet for efficient, mobile-friendly detection.
  - Siamese Networks for fine-grained individual cat re-identification.
- **Evaluation Metrics**: Precision, Recall, F1-score, Model Inference Speed.

## Existing Prototypes  
- Siamese Networks for pet re-identification exist but are not widely adopted in stray tracking scenarios.
- YOLO and MobileNet have lightweight mobile-ready models but need fine-tuning for the cat-specific domain.

