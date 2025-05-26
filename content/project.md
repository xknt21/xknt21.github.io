---
draft: false
title: 'Project Proposal'
---


# Smart Re-Identification Application for Stray Cats Post-TNR Program

## Overview
This project aims to develop an application capable of re-identifying stray cats that have been released following Trap-Neuter-Return (TNR) programs. By capturing and uploading an image of a cat, users will be able to retrieve associated shelter records if the cat had previously been housed.  
The system primarily addresses challenges related to post-shelter adoption by enabling potential adopters to determine the adoption status of stray cats outside the shelter environment.  
Additionally, it offers broader support for stray cat population management and monitoring initiatives.

**Keywords**: adoption; shelter; stray; re-identification; image recognition; TNR; Trap-Neuter-Return

---

## 1. Problem Statement - Background
Urban animal shelters in many regions are overburdened and face legal or ethical restrictions against euthanizing animals. As a result, many cats that were once sheltered are returned to city streets.  
To control the growing population of stray cats, many governments or organizations implement TNR (Trap-Neuter-Return) programs. However, research has shown that simply implementing those programs is unable to decrease the number of stray cats, and that increasing the adoption rate is still the only approach [1].  
Additionally, the process of adoption has multiple barriers. For example, shelters lose track of these cats after release, making it difficult to monitor their health or facilitate potential adoptions.  
It is essential to lower the barriers to increase the adoption rate [2].  
There's a need for a data-driven system that allows society to stay connected to these animals, even after release.

---

## 2. Vision - Goals

The primary vision of this project is to modernize the management of stray cat populations by introducing a scalable, AI-based re-identification system that can recognize individual stray cats after their release. This system aims to bridge the current welfare gap caused by the inability to track post-release cats, thereby improving both animal welfare and resource efficiency in shelters [10] [11].

We envision a society where stray cats are no longer invisible after neutering and release. Instead, each cat will have a persistent digital profile that shelters and citizens can access, update, and use for health monitoring, rescue operations, and potential adoption promotion. Such visibility can drastically increase rescue rates, reduce redundant neutering operations, and boost responsible citizen participation [11].

A second major goal is to support environmental conservation. By keeping track of stray cat populations and their health, local governments can control ecological impacts caused by stray cats, especially predation on native wildlife [11]. An organized system would also help local governments better allocate public resources, avoiding unnecessary financial waste through smarter capture and treatment strategies [10].

Ultimately, this project aims to serve as a global model. If successful, the solution developed here could be replicated internationally, especially in countries like Japan, Taiwan, Australia, the UK, and the US, where stray cat issues are a major urban problem [7] [8] [9].

Thus, the vision is to create a humane, efficient, and sustainable system that improves the lives of stray cats, supports shelter operations, protects urban biodiversity, and fosters a sense of shared responsibility between citizens and local governments.   

---

## 3. Objectives - Features to be Realized

### 3.1 Promote adoption
Currently, people who wish to adopt cats often need to actively search for adoption information through websites, visit shelters, or attend occasional adoption events.  
Our project addresses this by allowing citizens to simply **take a picture** of a street cat using their smartphones and instantly receive information about the cat’s adoption status.

---

### 3.2 Track post-release wellbeing
After release, monitoring the condition of cats becomes almost impossible under traditional TNR programs. Our application offers a solution by digitally tracking sightings of identified cats. Shelters and citizens can help monitor the cats’ health and general well being over time. Early detection of health issues, injuries or behavioral changes can lead to timely intervention, thus improving overall urban animal welfare.

---

### 3.3 Verify vaccination
Public safety and animal health are critical concerns. Through our system, users can instantly verify a cat’s vaccination status by scanning them. Knowing whether a cat is vaccinated in real time fosters safer interactions and encourages a more positive perception of stray cats in urban environments. It also assists authorities and shelters in managing vaccination schedules effectively .

---

### 3.4 Enhance social connection
Often, street cats are viewed as anonymous creatures with little to no personal connection to the human community. By enabling citizens to recognize and learn the stories of individual cats, the application helps to personalize interactions. When people know a cat’s name, history, or past adoption attempts, it can trigger empathy and emotional bonding, promoting a sense of shared responsibility toward these animals and strengthening community ties.


---

## 4. Scope
### 4.1 Issues at Hand Caused by the Major Problem

**Large Number of Stray Cats**
Taiwan faces a major stray animal issue, with over 160,000 stray cats and dogs reported [10]. This number is increasing yearly due to abandonment and unregulated breeding. Globally, the problem is even bigger; for example, the USA alone has an estimated 30–80 million stray cats living on the streets [12]. These high numbers show that stray animals are a long-term and large-scale problem that cities are struggling to manage.

**Shelters Are Overloaded**
In Taiwan, shelters can accommodate only about 3% of stray animals [10]. This means 97% of strays remain outside or are re-released through TNR programs. Overcrowded shelters cannot properly care for the animals, and new arrivals are often turned away. Therefore, SNR becomes a necessary but imperfect solution where the animal is released but loses all official connection to the shelter system.

**Post-Release Cats Are Forgotten**
After being neutered and returned, these cats are no longer tracked by shelters [10]. There’s no monitoring for illnesses, injuries, or changes in behavior. This creates a huge welfare gap — if a cat gets sick or hurt after release, no one notices unless a random citizen reports it. The lack of a reconnection method also limits opportunities for future adoption or rescue.

**Current Tracking Methods Are Weak**
The only current method of identifying TNR cats is through ear-tipping, a practice where a small part of the cat’s ear is clipped to indicate it was neutered [12]. However, ear-tipping does not distinguish individual cats. It tells you the cat has been neutered, but not which cat it is. There is no system to recognize a particular cat or follow its health or status over time.

**Financial Costs Are Huge**
Managing strays without a tracking system is extremely cost-inefficient. Taiwan’s local governments spend millions each year on capturing, neutering, and handling stray animals [3]. Without good tracking, shelters and government workers waste resources by mistakenly re-catching neutered cats or failing to prioritize sick ones. Long term, this drives up costs for cities and leads to inefficient use of public funds.

### 4.2 Benefits to Solving This Problem

**Improves Animal Welfare**
Having a system to identify and monitor released cats would help shelters and citizens quickly detect illnesses or injuries. Sick or hurt cats could be rescued faster instead of being left unnoticed on the streets. This would significantly improve the quality of life for thousands of animals [10].

**Saves Shelter Resources**
Smart re-identification could reduce unnecessary effort for shelters. Instead of capturing cats blindly, they could target cats that need urgent care based on updated information. This means shelters can spend more time and money on treatment, adoptions, and education programs rather than redoing work [10].

**Boosts Cat Adoption Rates**
With a system that can recognize individual cats on the streets, citizens interested in adoption could look up information easily. If a particular stray is healthy and friendly, it would be much easier to promote and find adopters. This could increase adoption rates and reduce the overall stray population [12].

**Protects Other Wildlife**
Stray cats are known to hunt and harm native wildlife, especially birds and small mammals [12]. By keeping better track of stray cats, cities could reduce the ecological impact caused by unmonitored cat colonies, helping to protect biodiversity.

**Uses Modern Technology for Purposes Beneficial to the Environment**
AI-driven re-identification technologies (like Siamese Networks) are already showing success in identifying individual animals [4]. Applying this technology to stray cats offers a practical, scalable solution to a real social problem. It also opens the door for similar smart monitoring systems for other urban animals worldwide.

In summary, this problem is worth solving because, the stray cats at large cause and overload in available shelters, further causing sheltered cats to be forgotten after their release, which is fuelled by the lack of modernization in the methods used to track them. Solving this major problem would improve the welfare of the cats and other animals around them, further saving resources and other local wildlife, along with boosting adoption rates for stray cats. This project encourages the use of modern information systems for this specific purpose as related projects have demonstrated accordingly.

---

## 5. Limitations and Risks
This application relies on the shelters or organizations to build up the data of information of cats, which indicates that the cats must be sheltered once to leave the record. Also, it leads to greater costs needed to promote the SNR program.
There is a substantial risk of sharing the location where the cats usually stay as there are perpetrators of cat abuse. It may be more secure if the locations are only shared with the shelter or organizations to be able to perform any rescue if needed. 
As the application requires users to upload and share the location of the photos, there may be potential risk in users’ privacy too.


---

## 6. Sustainability
Initially, the application will be developed from a limited database of stray cat images collected by the team. As the user base grows, the system can implement a feature to identify and re-identify cats not present in the original database. Through repeated sightings and visual pattern matching, the app can gradually assign unique profiles to these cats, allowing the database to expand dynamically. This approach enables the system to adapt to new environments and continuously improve its accuracy through real-world usage and community feedback.

---

## 7. Data Strategy
### 7.1 Data Acquisition

To support the identification and re-identification of stray cats, our team will collect image data from multiple sources, focusing on capturing cats from various angles (ideally 360-degree coverage) to ensure robust pattern recognition. The primary data acquisition methods are as follows:   


 **7.1.1 Using Existing Online Datasets**
First, we will search for publicly available datasets that contain images of cats. Some research communities and open-access repositories provide datasets featuring cats in various environments, which can serve as a foundation for building our database.   

**7.1.2 Directly Contacting Animal Shelters**
To supplement existing datasets, we will directly contact animal shelters and rescue organizations to request access to their photo archives. These institutions often take multiple photos of each animal from different angles for adoption purposes, which would be highly valuable for our re-identification training.   

**7.1.3 Web Scraping from Shelter Websites**
If we are unable to find a sufficient amount of data through existing datasets or direct contact with shelters, we will use web scraping techniques to collect images from the websites of animal shelters. This method will be used carefully, ensuring compliance with legal and ethical standards regarding data collection.   

All images will be preprocessed for quality and privacy compliance.

---

### 7.2 Data Processing - Preprocessing
Collected images will undergo:
- **7.2.1 Cleaning**: Remove blurry, duplicate, or corrupted images.
- **7.2.2 Standardization**: Resize images and normalize pixel values.
- **7.2.3 Annotation**: Add metadata (e.g., unique IDs, shelter info, location).
- **7.2.4 Augmentation**: Apply flipping, rotation, brightness adjustments, and cropping.

Images will be used to train CNNs, creating vector embeddings for rapid matching.

---

### 7.3 Data Science Techniques
 
The following data science techniques will be used to power the smart stray cat re-identification system:   
**7.3.1 Image Preprocessing with OpenCV (Pre-Processing)**   
All collected images will undergo preprocessing steps such as resizing, normalization, noise reduction, and edge detection using OpenCV. These steps will improve the quality and consistency of data used for model training.   
**7.3.2 Feature Extraction Using Convolutional Neural Networks (CNNs) (Extracting features of cats)**   
We will use pre-trained deep learning models such as ResNet or MobileNet for extracting distinguishing visual features like fur pattern, eye shape, and ear position. These models are well suited for image-based classification tasks.   
**7.3.3 Siamese Network for Re-Identification (Recognition)**   
To determine whether two images represent the same cat, we will use a Siamese Neural Network trained with contrastive loss or triplet loss. These models are effective in learning a similarity function and have been used in human and animal re-identification tasks.   
**7.3.4 Unsupervised Clustering (Classifying)**   
When labeled data is insufficient, clustering techniques such as DBSCAN or k-means may be used to group similar cats together based on extracted features.    
Web Scraping as a Last Resort: If the manually collected or community-contributed images prove insufficient, we will utilize web scraping to collect cat images from public forums, social media, and open-source databases. These technologies together create a robust pipeline capable of handling the complexity and variability of real-world stray cat identification.

---

### 7.4 Data Visualization

The following data visualization techniques will be used to enhance the smart stray cat re-identification system which will feature a smart mobile application with a built-in cat recognition camera feature:   
**7.4.1 Profile Cards**   
After users submit images of the desired cat, a profile card will present essential information such as the cat’s name, breed (if identifiable), adoption status, last vaccination date (if available), and contact details for the associated shelter. Additionally, users can add additional information regarding the cat that they are reporting during the submission process, be it injuries or concerns which can be seen by other users and community members. Lastly, each cat within the database will have a unique identifier that users can refer to when searching for a specific cat’s profile.    

**7.4.2 Performance Metric Dashboards**  
To maintain the reliability of the system, administrators will have access to dashboards visualizing key performance metrics such as precision, recall, and confidence scores. Bar charts, ROC curves, and simple statistical summaries will be used to monitor system accuracy and minimize false identifications. This internal visualization ensures that the app remains trustworthy for users and allows administrators to spot areas that are of concern such as a certain breed of cat not being optimized or other varying concerns.

---

## 8. Existing Prototypes

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

## 9. Government Reports

- **Problem in Niijima Village (Tokyo)**  
  Rise in stray cats causing complaints. Removal without neutering only relocates the problem [6].

- **Problem in Osaka City**  
  Overpopulation causing public nuisance; responsibility needed when feeding [7].

- **UK Government Report**  
  Difficulty differentiating owned vs unowned cats; microchipping proposed [8].

- **Australia's Stray Cat Impact**  
  Predation on wildlife and disease spread; highlights the human role in cat population issues [9].

---

## 10. Security and Data Privacy
- Data collected with user/shelter consent.
- Stored in a private database accessible only by authorized personnel.
- Anonymized location data.
- Users and shelters can request data removal at any time.

---

## References
[1] Levy, J.K.; Crawford, P.C. Humane strategies for controlling feral cat populations. *J. Am. Vet. Med. Assoc.* 2004.   
[2] Crawford, H.M.; Calver, M.C.; Fleming, P.A. Ethical challenges of TNR. *Animals* 2019.    
[3] Boulaouane, Y. et al. Advancing Pet Biometric Identification. *IEEE Access* 2024.   
[4] Trein, T.; Garcia, L.F. Siamese Networks for Cat Re-Identification. *arXiv* 2025.   
[5] Zhou, J. et al. Feral Cat Recognition with Deep Learning. *Lecture Notes in Computer Science* 2020.    
[6] 新島村 (Tokyo). [Niijima.com](https://www.niijima.com/kurashi/seikatsu/doubutsu/2016-0127-0954-95.html).   
[7] 大阪市. [City of Osaka](https://www.city.osaka.lg.jp/kenko/page/0000020313.html).   
[8] Gov.uk. [Microchipping Cats in England - Summary](https://www.gov.uk/government/calls-for-evidence/microchipping-cats-in-england-call-for-evidence/outcome/summary-of-responses).    
[9] Nou, T. et al. Management of Cats by Local Governments in Australia. [NESP Report](https://www.nespthreatenedspecies.edu.au/media/uaoncte3/tsr-hub-project-7-4-report-the-management-of-cats-by-local-governments-of-australia_final.pdf).    
[10] 台北時報, “Protesters call for controls for strays,” Taipeitimes.com, Oct. 29, 2023. https://www.taipeitimes.com/News/taiwan/archives/2023/10/30/2003808434? (accessed Apr. 27, 2025).    
[11] T. Nou, S. Legge, J. Woinarski, J. Dielenberg, and G. Garrard, “The management of cats by local governments of Australia,” 2021. Available: https://www.nespthreatenedspecies.edu.au/media/uaoncte3/tsr-hub-project-7-4-report-the-management-of-cats-by-local-governments-of-australia_final.pdf    
[12] ASPCA, “Pet statistics,” ASPCA, 2022. https://www.aspca.org/helping-people-pets/shelter-intake-and-surrender/pet-statistics    
‌  

