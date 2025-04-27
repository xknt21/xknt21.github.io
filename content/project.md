---
draft: false
title: 'Project Proposal'
---


# Smart Re-Identification Application for Stray Cats Post-SNR Program

## Overview
This project aims to develop an application capable of re-identifying stray cats that have been released following Shelter-Neuter-Return (SNR) programs. By capturing and uploading an image of a cat, users will be able to retrieve associated shelter records if the cat had previously been housed.  
The system primarily addresses challenges related to post-shelter adoption by enabling potential adopters to determine the adoption status of stray cats outside the shelter environment.  
Additionally, it offers broader support for stray cat population management and monitoring initiatives.

**Keywords**: adoption; shelter; stray; re-identification; image recognition; SNR; Shelter-Neuter-Return

---

## Problem Statement - Background
Urban animal shelters in many regions are overburdened and face legal or ethical restrictions against euthanizing animals. As a result, many cats that were once sheltered are returned to city streets.  
To control the growing population of stray cats, many governments or organizations implement TNR (Trap-Neuter-Return) or SNR (Shelter-Neuter-Return) programs. However, research has shown that simply implementing those programs is unable to decrease the number of stray cats, and that increasing the adoption rate is still the only approach [1].  
Additionally, the process of adoption has multiple barriers. For example, shelters lose track of these cats after release, making it difficult to monitor their health or facilitate potential adoptions.  
It is essential to lower the barriers to increase the adoption rate [2].  
There's a need for a data-driven system that allows society to stay connected to these animals, even after release.

---

## Vision - Goals
> **(EXAMPLE ONLY)**  
> This system aims to empower cities to leverage agile principles in utilizing human capital to foster a thriving, dynamic workforce ecosystem.  
> In this ecosystem, individuals are empowered to acquire new skills and smoothly transition between jobs to meet evolving and emerging career demands, ensuring a workforce that is both adaptable and responsive to the city’s needs.

---

## Objectives - Features to be Realized

### Promote adoption
Currently, people who wish to adopt cats often need to actively search for adoption information through websites, visit shelters, or attend occasional adoption events.  
Our project addresses this by allowing citizens to simply **take a picture** of a street cat using their smartphones and instantly receive information about the cat’s adoption status.

---

### Track post-release wellbeing
Our application offers a solution by digitally tracking sightings of identified cats.  
Shelters and citizens can help monitor the cats’ health and general well-being over time.

---

### Verify vaccination
Through our system, users can instantly verify a cat’s vaccination status by scanning them.  
Knowing whether a cat is vaccinated fosters safer interactions and encourages a more positive perception of stray cats.

---

### Enhance social connection
By enabling citizens to recognize and learn the stories of individual cats, the application personalizes interactions.  
When people know a cat’s name, history, or past adoption attempts, it can trigger empathy and emotional bonding.

---

## Scope
> **(EXAMPLE ONLY)**  
> A single metropolitan area will be covered for the prototype.  
> A limited subset of occupational segments will be covered based on available data for the prototype.

---

## Limitations and Risks
- Requires prior shelter records; only cats previously sheltered can be recognized.
- Risks of cat abuse if cat locations are publicly shared; better to restrict location info to shelters.
- Potential risks to user privacy due to location data sharing.

---

## Sustainability
Initially, the application will be developed using a limited database.  
As the user base grows, the system will identify and assign profiles to new cats, gradually expanding its database dynamically through real-world use.

---

## Data Acquisition

- **Using Existing Online Datasets**: Search for publicly available cat image datasets.
- **Directly Contacting Animal Shelters**: Request access to photo archives.
- **Web Scraping from Shelter Websites**: Scrape images carefully, respecting legal standards.

All images will be preprocessed for quality and privacy compliance.

---

## Data Processing - Preprocessing
Collected images will undergo:
- **Cleaning**: Remove blurry, duplicate, or corrupted images.
- **Standardization**: Resize images and normalize pixel values.
- **Annotation**: Add metadata (e.g., unique IDs, shelter info, location).
- **Augmentation**: Apply flipping, rotation, brightness adjustments, and cropping.

Images will be used to train CNNs, creating vector embeddings for rapid matching.

---

## Data Science Techniques

- **Image Preprocessing**: OpenCV for resizing, normalization, etc.
- **Feature Extraction**: CNN models like ResNet or MobileNet.
- **Siamese Network for Re-Identification**: Using contrastive/triplet loss.
- **Unsupervised Clustering**: DBSCAN or k-means if labeled data is insufficient.
- **Web Scraping**: As a last resort.

---

## Data Visualization

- **Profile Cards**: Display cat details, health status, sighting timeline, etc.
- **Map-Based Geolocation Visualization**: Interactive map for last known cat locations.
- **Performance Metric Dashboards**: Visualize metrics like precision, recall, and confidence scores.

---

## Existing Prototypes

- **Boulaouane et al. (2024)**  
  _Unified Pet Biometric Identification Framework (Petnow App)_  
  Focused on owned pets; had issues under poor image conditions [5].

- **Trein and Garcia (2025)**  
  _Siamese Networks for Street Cat Re-Identification (Hello Street Cat Initiative)_  
  Realistic street cat re-ID but limited flexibility [4].

- **Zhou et al. (2020)**  
  _Web Application for Feral Cat Recognition_  
  Autonomous monitoring system, but not user-interactive [3].

---

## Government Reports

- **Problem in Niijima Village (Tokyo)**  
  Rise in stray cats causing complaints. Removal without neutering only relocates the problem [6].

- **Problem in Osaka City**  
  Overpopulation causing public nuisance; responsibility needed when feeding [7].

- **UK Government Report**  
  Difficulty differentiating owned vs unowned cats; microchipping proposed [8].

- **Australia's Stray Cat Impact**  
  Predation on wildlife and disease spread; highlights the human role in cat population issues [9].

---

## Security and Data Privacy
- Data collected with user/shelter consent.
- Stored in a private database accessible only by authorized personnel.
- Anonymized location data.
- Users and shelters can request data removal at any time.

---

## References
1. Levy, J.K.; Crawford, P.C. Humane strategies for controlling feral cat populations. *J. Am. Vet. Med. Assoc.* 2004.
2. Crawford, H.M.; Calver, M.C.; Fleming, P.A. Ethical challenges of TNR. *Animals* 2019.
3. Boulaouane, Y. et al. Advancing Pet Biometric Identification. *IEEE Access* 2024.
4. Trein, T.; Garcia, L.F. Siamese Networks for Cat Re-Identification. *arXiv* 2025.
5. Zhou, J. et al. Feral Cat Recognition with Deep Learning. *Lecture Notes in Computer Science* 2020.
6. 新島村 (Tokyo). [Niijima.com](https://www.niijima.com/kurashi/seikatsu/doubutsu/2016-0127-0954-95.html).
7. 大阪市. [City of Osaka](https://www.city.osaka.lg.jp/kenko/page/0000020313.html).
8. Gov.uk. [Microchipping Cats in England - Summary](https://www.gov.uk/government/calls-for-evidence/microchipping-cats-in-england-call-for-evidence/outcome/summary-of-responses).
9. Nou, T. et al. Management of Cats by Local Governments in Australia. [NESP Report](https://www.nespthreatenedspecies.edu.au/media/uaoncte3/tsr-hub-project-7-4-report-the-management-of-cats-by-local-governments-of-australia_final.pdf).

