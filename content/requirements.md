---
draft: false
title: 'Requirements Specification'
---

# **Preface**

### **Version History**

| Version | Date | Description |
| :---- | :---- | :---- |
| 1.0 | April 28, 2025 | Finished the initial project proposal with the goal of streamlining and assisting the adoption process of stray cats. |
| 1.1 | May 26, 2025 | Adjusted system structure, goal, and certain features based on interviews conducted with stakeholders. Project now focuses more on preventing hospitals from doing redundant checkups on stray cats. Completed requirements specification.  |

### **Document Conventions**

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119).

This document utilizes a specification convention that separates requirements intended for user-level readers and system-level readers to suit their various reading intentions. Moreover, the document adheres to a prefix convention that follows the following format:

1. **FR-X.x** refers to Functional Requirements with their corresponding branches or sub-requirements. Within each functional requirement, the description shall start with its user requirements, followed by the system requirements.  
2. **NFR-X.x** refers to Non-Functional Requirements with their corresponding branches or sub-requirements.

### **Expected Readership**

This document is intended for various readers who may be involved in the development, deployment, and use of the system as indicated in the table below:

| Intended Reader | Relevant Document Sections |
| :---- | :---- |
| System Developers and Engineers | \- Version History\- Document Conventions\- System Functionality\- Use Cases \- Glossary \- Functional Requirements \- Non-Functional Requirements |
| Project Managers and Coordinators | \- Preface \- Introduction \- Glossary |
| System Analysts and Designers | \- Introduction \- Glossary \- Functional Requirements \- Non-Functional Requirements |
| End Users (Volunteers and Animal Hospital Staff) | \- Introduction \- Glossary |
| Administrators | \- Use Cases \- Glossary \- Functional Requirements |
| Test Engineers | \- System Functionality \- Use Cases \- Glossary \- Functional Requirements \- Non-Functional Requirements |
| Documentation Lead and Team  | \- Preface \- Glossary |

# **Introduction**

This document is the Software Requirements Specification (SRS) for the **"Smart Re-Identification System for Stray Cats Post-TNR Program"** project. It outlines the system's functionality, expected behaviour, and constraints relevant to its deployment and use. The document aims to ensure that all stakeholders or potential users understand what the system will do and how it will operate.

### **Objectives**

The main goal of this system is to prevent redundant medical checkups on stray cats by enabling volunteers and animal hospitals to verify if a cat has already been captured and treated. The system achieves this by using a re-identification system to match submitted photos of stray cats with an existing database. The objectives can be summarised in the following points:

* Prevent the same stray cat from being taken to the hospital multiple times.  
* Assist volunteers by providing quick and reliable re-identification of cats through images.  
* Improve coordination among different users (individual caretakers, organisations, and animal hospitals).  
* Increase efficiency and reduce mistakes in TNR (Trap-Neuter-Return) operations.

### **Scope**

The system will initially target users in the Kansai region in Japan with the capability to accommodate up to 1000 volunteers and 3 animal hospitals. This system will only implement core functions such as photo submission, profile management, and cat profile actions for volunteers and animal hospitals.

### **System Functionality**

* Allow users to upload images of stray cats and receive feedback on possible profile matches.  
* Display cat profiles which include details such as medical history, approximate age, and gender.   
* Enable role-based account types with varying access for volunteers, animal hospitals, and organisations.  
* Allow animal hospitals to make changes and adjustments to cat profiles and medical records  
* Allow users to make suggestions and reports to administrators

### **Intended End Users** 

This system is designed primarily for the following groups who are actively involved in the care and management of stray cats. Each user group interacts with the system in different ways, and their specific needs have been considered in the requirements specification.

1\. **Individual Volunteers**

Individual caretakers or citizens who care for stray cats in their local areas. They will be able to submit cat sightings, upload images, and check for past records to help institutions avoid redundant capture or treatment. They will fall under the volunteer class in the system.

2\. **Animal Rescue Organisations (e.g., TNR Groups, NPOs, Community Members)**

Formal or informal groups involved in TNR (Trap-Neuter-Return) or rescue activities. They use the system for cat status tracking, profile management, and collaboration with animal hospitals. They will fall under the volunteer class in the system.

3\. **Veterinary Clinics and Animal Hospitals**

These facilities use the system to avoid treating the same cat multiple times, access a cat’s vaccination/surgery records, and any necessary documentation. They will fall under the animal hospital class in the system.

### **Use Cases**

#### Use Case Diagram

![Imgur](https://imgur.com/g88nmjg.jpg)

#### User Classes Characteristics

1. **Volunteer**: Includes individual caretakers, rescue groups, and TNR organizations.

2. **Animal Hospital**: Clinics and staff involved in stray cat intake and treatment.

3. **Administrator**: System-level operators responsible for moderation and account management.

#### Use Case Table

| Number | Name | Description | Associated Functional Requirement(s) |
| :---: | :---: | :---: | :---: |
| U-1 | Sign up | User creates a new account in the system. | FR-1, FR-13 |
| U-2 | Log in | User accesses their account with credentials and recovers the password (if needed). |  FR-5, FR-15 |
| U-3 | Edit Account Details | Users update their account or profile information. | FR-3, FR-13, FR-15 |
| U-4 | Delete Account | User requests to delete their account and associated data. | FR-6 |
| U-5 | Upload Image | User uploads an image of a stray cat for re-identification. | FR-7,  FR-16 |
| U-6 | View Matching Result | User receives feedback if the uploaded cat matches an existing record, including confidence score. | FR-8, FR-16 |
| U-7 | Report Incorrect Match | Users report if they think an image matching result is incorrect. | FR-8, FR-12 |
| U-8 | View Cat Profile | User views details and medical history of a cat profile. | FR-9, FR-11 |
| U-9 | Add Cat Profile | Animal hospital staff can create a new cat profile. | FR-10, FR-13 |
| U-10 | Edit Cat Profile | Staff update information for an existing cat profile, including medical/treatment records. | FR-10, FR-11, FR-13 |
| U-11 | Delete Cat Profile | Staff can delete a cat’s profile from the system. | FR-10, FR-15 |
| U-12 | Manage User Accounts | Administrator manages user accounts: view, activate, deactivate, delete, etc. | FR-2, FR-15 |
| U-13 | View System Analytics | System-generated reports/visualizations on statistics and trends viewed by admin. | FR-14 |
| U-14 | Verify Account | Authorized staff review documentation and verify or reject user accounts. | FR-2, FR-4 |
| U-15 | Activate Account | Administrator or staff activates a user account after verification. | FR-2, FR-4 |
| U-16 | Manage Cat Profile | Administrators oversee the addition, editing, or deletion of cat profiles. | FR-10, FR-15 |
| U-17 | Send Mail to Users | System or staff send notifications, messages, or emails to users, maintaining user privacy. | FR-1, FR-3 \- FR-5, FR-8, FR-12 |
| U-18 | Receive User Reports | Administrator receives user-submitted feedback or incident reports. | FR-8, FR-12 |
| U-19 | Manage Re-ID Matches | Authorized personnel review, confirm, or adjust image-based re-identification matches. | FR-8, FR-14, FR-16 |

# **Glossary**

### **General Terms**

| Term | Definition |
| :---: | ----- |
| Confidence Score | A numerical value (typically between 0% and 100%) that indicates how certain the Re-ID model is that a submitted cat image matches an existing profile. |
| Data Anonymization | The process of removing or blurring private and sensitive information (e.g., name, location) to protect user privacy in stored or shared data. |
| Functional Requirements (FR) | Statements that describe specific behaviors, features, or functions the system must perform to meet user needs. |
| Image Validation | A system process that checks if an uploaded image meets required criteria, such as resolution and file format before accepting it. |
| Mobile-Friendly Interface | A user interface designed to be easily usable on mobile devices, ensuring proper layout, touch support, and responsive behavior. |
| Non-Functional Requirements (NFR) | System requirements that define performance, usability, security, and other quality attributes, rather than specific features or functions. |
| Photo Submission Workflow | The sequence of steps a user follows to capture, upload, and submit a cat photo for recognition by the system including prompts like “Take Photo” or “Submit.” |
| Re-Trap Case | A scenario where the same stray cat is unintentionally captured and brought for check-up more than once due to a lack of a tracking system. |
| Recognition Result | The system's output after attempting to match an uploaded cat image to an existing profile, including whether a match was found and the confidence score. |
| Reporting and Visualization | Features that allow users and administrators to monitor system performance and data (e.g., successful matches, system usage) through charts or summaries. |
| System Scalability | The system’s ability to handle increasing amounts of data, users, or image submissions without performance degradation. |
| Timestamp | The recorded date and time at which a specific action (e.g., photo upload, profile update) occurs in the system. |
| User Engagement Prompt | A message from the system encouraging users to take additional actions, such as signing up, reporting issues, or verifying results. |
| User Roles | The different categories of users in the system (e.g., volunteers, animal hospital staff, administrators), each with defined permissions and intended responsibilities. |
| Visual Accessibility | Design features that ensure the interface is usable by people with visual impairments, such as proper color contrast and screen reader compatibility. |

# **Functional Requirements**

### **FR-1 – Account Creation**

Users **MUST** be able to create an account through the application.

**System Requirements**

**FR-1.1** System **MUST** provide a registration interface for new users with required fields based on the following user types.

* **Individual caretaker**: full name, contact information (eg. email, phone number), region of living  
* **Organization**: legal name of organization, type of organization(eg. NPO, community group, rescue team), contact information (eg. link to website, email), mission statement or description of service  
* **Animal hospital**: hospital name, type of facility (eg. general veterinary clinic, emergency hospital, speciality center), physical address, contact information (eg. email, phone number)

**FR-1.2** System **MUST** validate input formats and required fields before allowing account creation.

**FR-1.3** System **MUST** securely store user information, including hashed passwords.

**FR-1.4** System **MUST** notify the user upon successful registration or return appropriate response upon rejection.

### **FR-2 – Account Administration**

Authorized users **MUST** be able to manage user accounts.

**System Requirements**

**FR-2.1** System **MUST** allow administrators to view, activate, deactivate, or delete accounts.

**FR-2.2** System **MUST** restrict administrative capabilities to authorized roles (e.g., administrators, verified staff).

**FR-2.3** System **MUST** log all administrative actions for auditing purposes.

### **FR-3 – Edit Profile**

Users **MUST** be able to update their personal or organizational profile information.  
**System Requirements:**

**FR-3.1** System **MUST** provide an editable user profile interface for personal or organization-specific information.

**FR-3.2** System **MUST** validate updated data before saving changes.

**FR-3.3** System **MUST** allow users to update profile images, contact information, and description fields.

**FR-3.4** System **MUST** notify users when their profile is edited.

### **FR-4 – Account Verification and Activation**

All accounts **MUST** undergo verification before gaining full access.

**System Requirements**

**FR-4.1** System **MUST** require document uploads (e.g., ID, certificates) for verification depending on user type.

**FR-4.2** System **MUST** provide a review interface for authorized personnel to approve or reject verification requests.

**FR-4.3** System **MUST** notify users when verification is completed or requires correction.

**FR-4.4** System **MUST** restrict feature access until the account is verified and activated.

### **FR-5 – Password Recovery**

Users **MUST** be able to recover access to their account if credentials are lost.

**System Requirements**

**FR-5.1** System **MUST** provide a secure password reset mechanism using email or other identity confirmation methods (e.g. phone number).

**FR-5.2** System **MUST** allow users to create a new password after successful identity verification.

**FR-5.3** System **MUST** expire password reset links after a defined duration.

### **FR-6 – Account Deletion**

Users **MUST** be able to delete accounts in accordance with privacy regulations.

**System Requirements**

**FR-6.1** he system MUST support account deletion functionality initiated by the user

**FR-6.2** System **MUST** confirm the deletion request with the user before proceeding.

**FR-6.3** System **MUST** anonymize or remove personal data associated with the deleted account, except data required for legal compliance or auditing.

**FR-6.4** System **MUST** notify the user when the account has been successfully deleted.

### **FR-7 – Photo Upload by Users**

Users **MUST** be able to upload photos of stray cats using their smartphone through the application.

#### **System Requirements**

**FR-7.1**  
The system **MUST** provide an interface that allows users to select an existing image or capture a new one using their device's camera.

**FR-7.2**  
The system **MUST** allow users to optionally attach metadata such as a timestamp to the uploaded image.

**FR-7.3**  
The system **MUST** validate that the uploaded file is in a supported format: .jpg, .jpeg, or .png.

**FR-7.4**  
The system **MUST** validate that the uploaded file meets the minimum resolution requirement of 1280 x 720 pixels. 

**FR-7.5**  
The system **MUST** return an appropriate message if the uploaded file does **not** meet the specified format or resolution criteria.

**FR-7.6**  
The system **MUST** ensure that the uploaded image does not exceed a file size of 5MB.

**FR-7.7**  
The system **MUST** process the uploaded image by testing it against the image-based re-identification model and compute a confidence score against stored cat profiles in the database.

### **FR-8 – Cat Re-identification Result** 

Users **MUST** be able to receive a response indicating whether the uploaded cat matches an existing record in the system.

#### **System Requirements**

**FR-8.1**  
The system **MUST** compare the uploaded image against the cat image database using a trained re-identification model.

**FR-8.2**

The system **MUST** classify re-identification match results into three confidence tiers and respond accordingly:

1. **High Confidence (≥ 80%)**:  
   The system **MUST** indicate that a match was found and show an appropriate interpretation of the confidence score (e.g., "Very Likely Match").

2. **Moderate Confidence (60% to \< 80%)**:  
   The system **MUST** display a warning that the result is uncertain (e.g., "Possible Match – Needs Confirmation").  
   The user **MUST** be given the option to confirm, reject, or report the match.

3. **Low Confidence (\< 60%)**:  
   The system **MUST** notify the user that no reliable match could be found. 

   The user **MUST** be given the option to report the match if they believe that it’s a false re-identification.

**FR-8.3**  
   In all cases where a user uploads an image, the system **MUST** show the numerical confidence score (e.g., “Match Confidence: 76.3%”) alongside the cat’s profile.

**FR-8.4**  
   The system **MUST** log all Re-ID match attempts for details such as confidence score, number of successful matches, and match result to support analytics and future model tuning.

### **FR-9 – Display of Cat Profiles**

When a cat is recognized, the system **MUST** present relevant information about the cat to the user.

System Requirements

**FR-9.1**  
The system **MUST** retrieve and display the following fields from the database for a matched cat:

* **Approximate age**

* **Gender** (e.g., male/female)

* **Vaccination status** (e.g., vaccinated: yes/no)

* **Neuter status** (e.g., neutered: yes/no)

* **Medical history** (e.g. surgery)

**FR-9.2**  
  The system **MUST** display an edit history of the profile and display the following:

* **Hospital name** (e.g. Osaka Animal Hospital)

* **Date** (e.g. 2025年5月25日)

* **Treatment/medical procedure** (e.g. front left leg surgery)

**FR-9.3**  
  The system **MUST** present the above information in a **clear, readable, and mobile-friendly format**, accessible immediately after the recognition result is returned.

### **FR-10 – Cat Profile Management**

**Animal hospital staff** **MUST** be able to create, edit, and delete individual cat profiles within the system. These profiles serve as the foundation for tracking medical status, re-identification accuracy, and adoption readiness.

**System Requirements:**

**FR-10.1**  
The system **MUST** allow hospital staff to create new cat profiles including essential details such as:

* Name or temporary ID

* Pictures

* Physical/medical condition

* Notes or observations

**FR-10.2**  
  The system **MUST** support editing and deletion of existing cat profiles, with proper authentication and role-based access control.

**FR-10.3**  
  The system **MUST** support uploading of **two to nine images** per cat (e.g., front, side, top views) to enhance identification accuracy.

**FR-10.4**  
  The system **MUST** support **tagging** of profiles with relevant attributes such as:

* Spayed/Neutered

* Injured

* Under treatment

* Released

**FR-10.5**  
  Upon profile submission, the system **MUST** return a result indicating whether the cat is already registered. If a match with **a confidence score higher than 60%** is found, the associated **cat profile** must be displayed with the **confidence score**.

**FR-10.6**  
  The system **MUST** allow the administrator to manage all uploaded content in the profile.


### **FR-11 – Medical and Treatment Records**

The system **MUST** enable animal hospital staff to **log and manage medical histories** for each cat, ensuring accurate documentation of treatments and follow-up care requirements.

**System Requirements:**

**FR-11.1**  
The system **MUST** allow authorized staff to record medical details for each cat, including:

* **Vaccinations** (e.g., rabies, FVRCP)

* **Treatments** (e.g., deworming, antibiotics)

* **Surgeries** (e.g., spay/neuter, injury-related procedures)

**FR-11.2**  
  The system **MUST** be able to **flag cats requiring follow-up care** based on predefined timelines (e.g., post-surgery checks, vaccination boosters), and notify staff accordingly.

### **FR-12 – Feedback System**

Users **MUST** be able to report any problems through a form.

**System Requirements:**

**FR-12.1**  
The system **MUST** allow users to input the following:

* Full name

* Contact information (e.g. e-mail address, phone number)

* Feedback
  
**FR-12.2**  
  The system **MUST** send a notification to the administrator if a user submits a form.

### **FR-13 – Data Entry Support**

To streamline hospital operations, the system **MUST** offer convenient and reliable methods for staff to input and manage data, even in field conditions or areas with unstable connectivity.

**System Requirements:**

**FR-13.1**  
The system **MUST** provide **mobile- and tablet-friendly interfaces** for efficient data entry, optimized for use on touchscreen devices.

**FR-13.2**  
The system **MUST** support **offline data entry**, allowing staff to input information without an active internet connection, and **automatically sync** the data once connectivity is restored.

### **FR-14 – Reporting and Visualization**

The system MUST enable administrators to access automatically generated reports and visualizations that present statistics pertinent to cat adoption and related activities within the domain of the application. These capabilities are intended exclusively for administrators to support oversight, analysis, and data-driven management.

**System Requirements:**

**FR-14.1:**  
The system MUST automatically generate up-to-date statistical reports relevant to the application domain. The reports MUST include, but are not limited to, the following metrics:

* Total number of cat profiles in the system  
* Number of high-confidence matches to cat profiles  
* Number of moderate-confidence matches to cat profiles  
* Number of low-confidence matches to cat profiles  
* Number of cats that have been neutered (keep neuter cases)

**FR-14.2:**  
  The system MUST ensure that all generated reports and accompanying visualizations are presented in a clear, accessible, and easily interpretable format suitable for administrative review and analysis.

**FR-14.3:**  
  The system MUST restrict access to these statistical reports and visualizations such that only administrators have the ability to view this critical data.


### **FR-15 – Access Control and Logging**

The system **MUST** enforce role-based access control and maintain a transparent audit trail to ensure data integrity, accountability, and proper authorization across user actions.

**System Requirements:**

**FR-15.1**  
The system **MUST** restrict functionality and editing privileges based on user roles, such as:

* **Administrators**: Full access, including approval and deletion

* **Animal hospital staff**: Profile and medical data management

* **Volunteers**: Viewing and reporting only

**FR-15.2**  
  The system **MUST** log all changes made to cat profiles, including:

* What was changed

* Who made the change

* When the change occurred  
  The system **MUST** display a **modification history** within each profile for transparency and tracking.

### **FR-16 – System Workflow for Image Processing**

The system **MUST** follow a structured and reliable workflow when processing uploaded images to ensure accurate re-identification, appropriate data handling, and timely notifications to relevant stakeholders.

**System Requirements:**

**FR-16.1**  
The system **MUST** process each newly uploaded image by attempting to match it against existing cat profiles using the **Re-Identification (Re-ID) algorithm**.

**FR-16.2**  
If a match is found, the system **MUST** display the **corresponding cat profile** and confidence score to the user who uploaded the image.

# **Non-Functional Requirements**

## **Product Requirements:**

### **Product-Usability**

### **NFR-1 – Guided Submission Workflow**

The system MUST offer a streamlined and user-friendly photo submission flow to guide users through reporting a stray cat.

**System Requirements**

**NFR-1.1**  
 The system MUST display visual prompts and simple call-to-action buttons (e.g., “Take Photo,” “Retake,” “Submit”) at each step of the report process.

**NFR-1.2**  
 The system MUST provide inline guidance or tooltips when the user is entering optional details such as color or injuries.

### **NFR-2 – Recognition Result Clarity**

The system MUST provide clear and concise feedback on whether the uploaded cat photo matches an existing cat.

System Requirements

**NFR-2.1**  
 The system MUST display a message indicating whether a match was found (e.g., “High Confidence Match Found”, “Moderate Confidence Match Found”, or “No Match Found”)  and confidence score ((e.g., “70 % ”)).

**NFR-2.2**  
 The system MUST include a clear visual transition to the cat profile page when a match is successful.

### **NFR-3 – Visual and Mobile Accessibility**

The system MUST be designed for ease of use on a range of screen sizes and meet essential accessibility needs.

**System Requirements**

**NFR-3.1**  
 The system MUST meet at least WCAG 2.2 Level AA compliance standards for visual accessibility.

**NFR-3.2**  
 The system MUST use responsive design techniques to ensure usability across common mobile and desktop devices.

**NFR-3.3**  
 The system SHOULD support touch-optimized components (e.g., large buttons, swipe gestures) for mobile users.

### **NFR-4 – Performance**

The system MUST respond to image upload and recognition tasks within a reasonable timeframe to maintain user engagement.

**System Requirements**

**NFR\-4.1** The system shall allow users to upload an image (≤5MB) within 3 seconds under normal network conditions.

**NFR\-4.2** The system shall process and return cat identification or re-identification results within 10 seconds of image upload.

**NFR\-4.3** The system shall support at least 100 concurrent users performing uploads or profile searches without noticeable degradation in performance.

**NFR\-4.4** Queries such as “cats available for adoption” or “recent rescues” shall return results within 2 seconds.

**NFR\-4.5** All data updates (e.g., new cat entry, image upload) shall reflect across all user views within 5 seconds of submission.

**NFR\-4.6** The application shall maintain 99.5% uptime on a monthly basis.

### **NFR-5 – Space**

The system MUST be installable and operate correctly within 500MB of disk space.

**System Requirements**

**NFR\-5.1** The installation drive MUST have at least 500MB of available disk space prior to installation.

**NFR-5.2** The system SHOULD notify the user if insufficient space is available before installation begins.

## **Product Dependability**

### **NFR-6 – Dependability and System Reliability**
The system MUST ensure stable, secure, and consistent performance for users, particularly in environments with network instability, multiple concurrent users, and critical data operations.

**System Requirements**

**NFR-6.1**  
The system MUST maintain a minimum of 99.5% uptime on a monthly basis to ensure availability to volunteers and shelter staff.

**NFR-6.2**  
The system MUST support a minimum of 1000 concurrent users uploading images or searching profiles without performance degradation.

**NFR-6.3**  
The system MUST allow users to upload images (≤5MB) within 3 seconds under normal network conditions.

**NFR-6.4**  
The system MUST return cat identification or re-identification results within 10 seconds of image upload.

**NFR-6.5**  
The system MUST reflect all data updates (e.g., new cat entry, image upload) across user interfaces within 5 seconds.

**NFR-6.6**  
The system MUST enable offline data entry and automatically sync updates once the device reconnects to the internet.

**NFR-6.7**  
The system MUST store audit logs of critical actions (e.g., data edits, logins) and restrict log access to authorized personnel only.

**NFR-6.8**  
The system MUST support secure session handling, including session expiration after inactivity and secure token regeneration.

### **Product-Efficiency-Security**

### **NFR-7 – Secure User Authentication and Authorization**

The system MUST ensure that only authorized users can access protected resources and perform actions appropriate to their roles.

**System Requirements:**

**NFR-7.1**  
The system MUST enforce secure user authentication using hashed email-password combinations or social login mechanisms (e.g., OAuth2).

**NFR-7.2**  
The system MUST implement Role-Based Access Control (RBAC) to restrict system functions and data access based on user roles (e.g., animal hospital staff, organization representatives, individual caretakers, administrators)

### **NFR-8 – Data Encryption and Protection**

The system MUST protect sensitive data by ensuring it is encrypted both during transmission and when stored.

**System Requirements:**

**NFR-8.1**  
All sensitive data (e.g., user profiles, shelter information, cat images) MUST be encrypted during transmission using TLS.

**NFR-8.2**  
All sensitive data at rest MUST be encrypted using AES-256 or an equivalent standard.

### **NFR-9 – Audit Logging and Monitoring**

The system MUST maintain secure and tamper-resistant logs to track critical system events and ensure accountability.

**System Requirements:**

**NFR-9.1**  
The system MUST maintain tamper-resistant audit logs for critical actions such as login attempts, data edits, and administrative changes.

**NFR-9.2**  
Access to audit logs MUST be restricted to authorized personnel only.

### **NFR-10 – Input Validation and Secure Coding**

The system MUST prevent security vulnerabilities by validating user input and following secure coding best practices.

**System Requirements:**

**NFR-10.1**  
The system MUST validate all user inputs to prevent vulnerabilities such as SQL Injection, Cross-Site Scripting (XSS), and Cross-Site Request Forgery (CSRF).

**NFR-10.2**  
The system MUST use secure coding practices, including prepared statements and input sanitization.

### **NFR-11 – Secure Session Management**

The system MUST manage user sessions securely to prevent unauthorized access and session hijacking.

**System Requirements:**

**NFR-11.1**  
The system MUST implement session expiration after a defined period of user inactivity (e.g., 30 minutes).

**NFR-11.2**  
The system MUST use secure cookie flags and regenerate session tokens upon re-authentication to prevent session hijacking.

### **NFR-12 – User Privacy and Data Control**

The system MUST respect user privacy by allowing control over personal data and preventing exposure of sensitive information.

**System Requirements:**

**NFR-12.1**  
The system MUST provide users with functionality to access, update, and delete their personal data in compliance with privacy laws (e.g., GDPR).

**NFR-12.2**  
The system MUST obtain explicit user consent before collecting or storing any personal data.

**NFR-12.3**  
The system MUST anonymise sensitive metadata, such as precise geolocation and uploader identity, before publicly displaying uploaded images.

**NFR-12.4**  
Location data in user-submitted images MUST be securely stored, and when shared, it MUST be obfuscated or blurred to prevent exact location identification.

## **Organisational Requirements:**

### **Organizational-Environment:**

### **NFR-13 - Execution Environment Compatibility**

The system MUST be accessible on modern smartphones and browsers, and remain usable under poor network conditions.

**NFR-13.1**  
To accommodate diverse user environments, the system MUST be operational on modern smartphone devices (iOS 13+, Android 10+) and desktop browsers (Chrome, Safari, Edge).

**NFR-13.2**  
The system SHOULD maintain functionality under low-bandwidth or unstable network conditions (e.g., public Wi-Fi, 3G), ensuring image submission and basic access are still possible.

**NFR-13.3**  
All computation-heavy processes (e.g., inference, training) MUST be offloaded to cloud servers to minimise local device energy consumption and maintain consistent performance.

### **NFR-14 - Physical Deployment and Geographic Resilience**

The system MUST be deployable in both urban and rural regions and remain reliable during natural disasters.

**NFR-14.1**  
The system SHOULD be deployable across regions with different environmental and legal conditions, and must support geographic scalability (e.g., urban vs. rural shelters).

**NFR-14.2**  
In regions prone to natural disasters (e.g., earthquakes, typhoons), cloud infrastructure MUST support data redundancy and disaster recovery mechanisms.

### **NFR-15 - Environmental Impact & Sustainability**

The system MUST minimise environmental impact by using energy-efficient infrastructure and deleting unnecessary stored data.

**NFR-15.1**  
The system’s cloud services SHOULD utilise energy-efficient infrastructure (e.g., carbon-neutral cloud platforms, auto-scaling containers) to reduce the environmental footprint.

**NFR-15.2**  
Image storage MUST implement automatic cleanup policies, deleting unused or expired data to reduce unnecessary resource consumption and storage costs.

### **NFR-16 - Wildlife & Habitat Sensitivity**

The system MUST NOT be used in protected wildlife zones without permission, and camera data in sensitive areas should be reviewed.

**NFR-16.1**  
To avoid disturbing natural ecosystems, the application MUST NOT be used in protected wildlife zones without proper authorisation.

**NFR-16.2**  
Camera data collection by users in environmentally sensitive areas SHOULD be restricted or flagged for review to ensure compliance with local environmental protection rules.

### **Organizational-Operational**

### **NFR-17 – Access Control and Data Integrity for Cat Records**

The system MUST allow only authorised users to manage cat records and track all changes for accountability.

**System Requirements:**

**NFR-17.1** 

The system MUST allow authorized animal hospital staff to access, edit, and delete cat records, including status updates.

**NFR-17.2** 

The system MUST support Role-Based Access Control (RBAC) to distinguish between animal hospital staff, organizational representatives, individual caretakers, and system administrators.

**NFR-17.3**

The system MUST record all changes to cat profiles for audit and traceability purposes.

### **Organizational-Development**

### **NFR-18 – Maintainability and Scalable Development**

The system MUST be built with widely supported technologies, follow modular and testable code design, and support easy updates with minimal downtime.

**NFR-18.1** 

The system shall be developed using widely supported and maintainable technologies such as Python (backend), TensorFlow (ML), and React Native (mobile frontend), to ensure ease of future development.

**NFR-18.2** 

The system shall follow a modular design to enable future integration with external platforms (e.g., city animal control databases or mapping APIs).

**NFR-18.3** 

All system components shall be accompanied by developer documentation, including API usage, model training setup, and data pipeline configuration.

**NFR-18.4** 

Development shall follow an Agile methodology, with bi-weekly sprints and iterative user feedback.

**NFR-18.5** 

The codebase shall follow industry-standard coding practices with at least 80% unit test coverage.

**NFR-18.6** 

System updates (bug fixes or minor features) shall be deployable with minimal downtime and without requiring rollback of major modules.

## **External Requirements:**

### **Regulatory Compliance**

### **NFR-19 – Regulatory and Ethical Compliance**

The system MUST comply with applicable data protection laws, ethical standards, and local animal welfare regulations in all operating regions.

**System Requirements:**

**NFR-19.1**  
The system MUST comply with GDPR, Japan’s Act on the Protection of Personal Information, and Taiwan’s Personal Data Protection Act.  
**NFR-19.2**  
Explicit user consent MUST be obtained for data collection, processing, and storage, and the purpose MUST be clearly communicated.

**NFR-19.3**  
The system MUST comply with local animal protection laws and MUST NOT promote illegal or unethical behavior (e.g., unauthorized capture or harm).  
**NFR-19.4**  
All identification methods MUST be non-invasive (e.g., photo-based identification only).

**NFR-19.5**  
Usage in sensitive areas (e.g., protected zones) SHOULD be restricted or require coordination with appropriate authorities.

### **Ethical Considerations**

### **NFR-20 – Data Privacy, Security, and Abuse Prevention**

The system MUST protect user privacy, prevent misuse of sensitive data, and uphold transparency and control in data usage.

**System Requirements**

**NFR-20.1**  
Metadata (e.g., GPS info) MUST be stripped from uploaded images to prevent unintentional location exposure.  
**NFR-20.2**  
Location data MUST NOT be publicly accessible and SHOULD be available only to verified shelters or partners.

**NFR-20.3**  
Access to sensitive information (e.g., match/location data) MUST be restricted to authenticated users with proper permissions.  
**NFR-20.4**  
The system MUST include abuse reporting and usage monitoring features to prevent malicious use.

**NFR-20.5**  
Users MUST be informed how their data is used and MUST have opt-in/opt-out controls where applicable.

### **Security & Legal Responsibility**

### **NFR-21 – Security, Accountability, and Legal Safeguards**

The system MUST ensure robust data security, enforce access control, and provide legal safeguards for both users and developers.

**System Requirements**

**NFR-21.1**  
All stored data MUST be encrypted (e.g., using AES-256).  
**NFR-21.2**  
The system MUST implement Role-Based Access Control (RBAC) to restrict sensitive data access.

**NFR-21.3**  
The system MUST implement API authentication, input validation, and rate-limiting to defend against attacks (e.g., SQL injection, DDoS).  
**NFR-21.4**  
Security audits and vulnerability scans MUST be conducted regularly.

**NFR-21.5**  
All significant actions (e.g., uploads, edits) MUST be logged with timestamp and user ID.  
**NFR-21.6**  
Shelters SHOULD be able to export activity logs for compliance and reporting purposes.

**NFR-21.7**  
Users MUST accept the Terms of Use and Privacy Policy prior to accessing the app.  
**NFR-21.8**  
The system MUST provide disclaimers to limit developer liability regarding data accuracy and match reliability.