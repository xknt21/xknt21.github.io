---
draft: false
title: 'System Design Document'
---
# **Preface**

### **Version History**

| Version | Date | Description |
| :---- | :---- | :---- |
| 1.0 | June 16, 2025 | Initial version |



## **Introduction**

This is the system design document for the “Re-identification Application for Stray Cats Post-TNR Program,” project which covers the process of abstracting system requirements into an easier format to be translated into code for development. The project aims to offer a streamlined application that can intermediate the process of stray cat management post-TNR which may come in the form of reducing redundant check-ups, provide a convenient recording system for stray cats, and facilitate community members a better means to assist stray cat management. This document consists of various diagrams used to illustrate various processes, interactions, and concepts within the system in a manner that adheres to all kinds of readers.

# **Overview**

## **System Context**

![Imgur](https://imgur.com/hkM1GSN.png)
The system context diagram highlights various interactions between relevant users and core systems within the whole system of the stray cat re-identification app. The diagram provides a simpler method for readers to understand how the distinct components within the whole system interact with each other.

## **Key Components and Their Interaction**

The stray cat re-ID system is designed to coordinate among administrators, volunteers, animal hospitals, and a centralized cat profile database to prevent repeated medical intake of the same stray cat.

### **1\. Administrator → Stray Cat Re-ID System**

The administrator oversees system operations by managing user accounts, verifying registration information, and moderating platform usage. This role involves direct access to administrative functions such as activating or deactivating accounts and monitoring data integrity.

### **2\. Stray Cat Re-ID System → Volunteer**

When volunteers (either individuals or organizations) interact with the system, it first requests relevant user information such as identification details, contact data, and region of operation for proper account handling and authorization.

### **3\. Volunteer → Stray Cat Re-ID System**

Volunteers respond by submitting their user information, including their role, region, and verification. This information is used by the system to support account creation, verification, and later, access to cat profile data for identification or reporting.

### **4\. Stray Cat Re-ID System → Animal Hospital**

The system requests hospital account information to verify the facility's type, services provided, and authorization to access or modify medical data related to stray cats.

### **5\. Animal Hospital → Stray Cat Re-ID System**

Animal hospitals provide their user data upon request. This enables the system to authenticate them and grant access to create, view, or edit cat medical records.

### **6\. Cat Profile Database System → Stray Cat Re-ID System**

The system retrieves cat profile data from the centralized database when performing re-identification or when a user views the cat’s medical history. This ensures accurate matching and informed decision-making by volunteers and hospitals.

### **7\. Animal Hospital → Cat Profile Database System**

Once an animal hospital provides treatment or updates information about a cat, the system stores the updated profile and medical history in the database. This guarantees that future identifications use the most current and complete data.

## **Explanation**

The stray cat re-ID system connects administrators, volunteers, and animal hospitals to manage cat identification and treatment data. All users interact with the system to send or receive information. The system reads from and writes to the cat profile database, ensuring accurate and updated records. It acts as the central hub for coordination and data flow among all components.

# **System Use Cases**

The following use case diagram is used to illustrate the actors relevant throughout this entire project along with their respective use cases. The use cases are used to showcase the various interactions and functionalities that each actor possesses. The diagram assists with abstracting complex user-system interactions and responsibilities into an easy to understand format suitable for any kind of reader. Furthermore, the actors in this diagram will be divided into 3 categories as described in the following manner:

1. **Volunteer**: Includes individual caretakers, rescue groups, and TNR organizations.

2. **Animal Hospital**: Clinics and staff involved in stray cat intake and treatment.

3. **Administrator**: System-level operators responsible for moderation and account management.

### Use Case Diagram

![Imgur](https://imgur.com/RmXyOxz.png)

### Use Case Table

| Number | Name | Description | Associated Functional Requirement(s) |
| :---: | :---: | :---: | :---: |
| U-1 | Sign up | User creates a new account in the system. | FR-1, FR-13 |
| U-2 | Log in | User accesses their account with credentials and recovers the password (if needed). |  FR-5, FR-15 |
| U-3 | Edit Account Details | Users update their account or profile information. | FR-3, FR-13, FR-15 |
| U-4 | Delete Account | User requests to delete their account and associated data. | FR-6 |
| U-5 | Upload Image | User uploads an image of a stray cat for e-identification. | FR-7,  FR-16 |
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

## **Class Interactions**

The actors in this diagram will hold responsibilities for the following interactions:

1. **Volunteer**: Volunteers interact with the system primarily through uploading and scanning cat images for identification. They are responsible for signing up, logging in, and managing their own accounts (U-1 to U-4). After submitting a cat image (U-5), they receive re-identification results (U-6) and can view cat profiles (U-8). If they believe a match is incorrect, they can report it (U-7). Volunteers may also receive notifications from the system (U-17), contributing to data collection and improving identification accuracy through user feedback.

2. **Animal Hospital**: Animal hospital staff are involved in the medical side of stray cat management. They add new cat profiles (U-9) when a cat is taken in for treatment, and update existing records with medical or behavioral information (U-10). When necessary, they can delete outdated or invalid profiles (U-11). Hospital staff may also help verify volunteer or user accounts (U-14), activate them (U-15), and manage cat profile data alongside administrators (U-16). Additionally, they may participate in reviewing and correcting re-identification matches to ensure the system's integrity (U-19).

3. **Administrator**: Administrators oversee the entire system's operation. They manage user accounts, including activating, deactivating, or deleting them (U-12), and validate new user or organization registrations (U-14, U-15). Admins are responsible for managing all cat profile data (U-16), monitoring system usage and analytics (U-13), and receiving and acting on user reports (U-18). They may also send system-wide communications or notifications (U-17), and play a critical role in validating re-identification results to improve reliability and fairness (U-19).

# **Sequence Diagram**

The following sequence diagram illustrates the process of signing up, logging in, modifying account details, and deleting accounts from the system. All of these activities are performed by the volunteer, hence this diagram depicts how a user interacts with the account based functions within the system.



## **Explanation**
![Imgur](https://imgur.com/JLqgW0A.png)

The sequence diagram outlines the interactions between the volunteer, the account portal, the volunteer database, and the core system. The classes are represented in the following manner:

* **Volunteer (Actor)**: Represents the user of the system that performs the functions.

* **Account Portal (Interface)**: Represents the part of the system where all account related matters take place.

* **Volunteer DB (Database)**: Represents the database where all volunteer account information and credentials are stored.

* **Main Page (Interface)**: Represents the part of the system apart from the Account Portal where all non-account related matters take place. This is the part of the system the volunteer is given access to upon logging in.

Each interaction in the diagram is as follows:

1) **Signing Up**: The user accesses the account portal to enter their details including name, address, date of birth, profession, contact information, and other necessary information or documents such as experience in handling stray cats. 

   1) The system checks if the account details are a duplicate in the volunteer database. 

   2) If the account details are new and the volunteer has not already signed up before, the account and its details are appended to the database. If not, an error message will display that the account already exists to the volunteer.

2) **Logging in**: 

   1) The user accesses the account portal to enter their details. 

   2) The system then checks whether the account exists and whether the login details are correct. 

   3) If the account does not exist, or if the login information is incorrect, an error message is presented to the volunteer. Otherwise, if successful, the volunteer is provided access to the main page.

3) **Modifying Account Details**: 

   1) The volunteer accesses the main page’s account configuration system to request for modification of account details, where they enter the new details of their account. This is because the volunteer has already logged in at this stage and cannot directly access the account portal. 

   2) The system then redirects to the account portal where the new details are inputted. 

   3) The account portal then accesses the volunteer database where the details are modified. 

   4) Upon modification, messages are sent through the account portal and the main page and directly to the volunteer saying that the account details have been modified.

4) **Account Deletion**: 

   1) The volunteer accesses the main page’s account configuration system to request for account deletion. 

   2) The main page then redirects to the account portal which asks for confirmation from the volunteer for the deletion to be executed. 

   3) If confirmation is received, the account portal accesses the volunteer database to remove the account. If there is no confirmation, no action will take place.

# **Flow Chart (Activity Diagrams)**
![Imgur](https://imgur.com/cGNX15H.png)
![Imgur](https://imgur.com/fqy7GXx.png)

## **Explanation**

**Animal Hospital:** 

This activity diagram shows the steps that staff members at animal hospitals take when using the stray cat re-identification system to add a new cat profile. The user’s connection to an animal hospital is first confirmed. If so, they are requested to upload a photo of the cat. The system then attempts re-identification to see if the cat is already in the database. If a match is found, the hospital staff is given the option to either update the existing profile or skip updating. At this point, the staff will manually review the matched profile. If no match is found, they are told to enter the cat’s information, including its age, gender, medical records, and any other necessary details. Following submission confirmation, the user is given the option to either finish the process or add another cat. This design allows staff to quickly register or update multiple cats while minimizing redundant data entry processes. 

**User:**

This activity diagram shows the re-identification process for volunteers who identify stray cats using the system. The volunteer uploads a picture of the cat to start the process from a camera or from their device’s library. After the image is submitted. The system uses re-identification to search through existing profiles for a potential match. If the system finds a match ( confidence score \>= 80%), it will display the profile of the identified cat to assist the user in verifying and potentially avoiding needless capture or treatment. If no reliable match is found, the system will display “No reliable match can be found” (confidence score \< 60%). If the result is simply uncertain, the system will display the message “Possible Match \- Needs Confirmation”(confidence score: 60% \~ 80%). 

# **Class Diagram:**

![Imgur](https://imgur.com/mJ487Fm.png)

The class diagram above represents the structure and relationships among various entities in a system that supports volunteers, hospital staff, and administrative functions. It demonstrates how different user types extend a common base User class to perform role-specific operations, while the Admin class interacts with users through an association relationship.

Here is a detailed explanation of each class and how they interact to deliver a functional and secure user management system.

**Class Descriptions**

| Class | Description |
| :---- | :---- |
| User | The base class that defines common attributes and core functionalities for all users in the system. It includes:  \- `login()`: Authenticates a user based on credentials and grants access to the system.  \- `register()`: Allows a new user to create an account by providing required personal details.  \- `editAccount()`: Enables users to update their profile information such as email or phone number.  \- `deleteAccount()`: Allows the user to permanently remove their account from the system.  \- `logout()`: Safely logs the user out of their session, ensuring security.  \- `uploadCatImage()`: Lets users upload images of cats (possibly for identification, reporting, or adoption).  \- `viewMatchResults()`: Displays system-generated match results, possibly for adoption or medical treatment matching.  \- `reportProblem()`: Allows users to report issues (technical or content-related) to system administrators. |
| IndividualVolunteer | A subclass of `User`, this class represents a person volunteering on an individual basis. It includes: \- `fullName`: The full legal name of the volunteer. \- `dateOfBirth`: The volunteer’s birth date, possibly used for eligibility verification or age-specific tasks. |
| OrganizationVolunteer | Another subclass of `User`, this class models volunteer organizations. It includes: \- `orgName`: Name of the volunteer organization. \- `orgType`: Type of organization (e.g., non-profit, shelter, rescue group), which can be used for filtering or authorization purposes. |
| HospitalStaff | Inherits from `User` and represents personnel from hospitals or clinics involved in animal care. Unique attributes and functionalities include: \- `hospitalName`: Name of the hospital or clinic the staff belongs to. \- `facilityType`: Type of facility (e.g., veterinary clinic, animal rescue center). \- `availableServices`: Description of medical or support services offered. \- `addCatProfile()`: Allows staff to create a new cat profile with medical or identification information. \- `editCatProfile()`: Enables updating existing cat records (e.g., treatment progress, test results). \- `deleteCatProfile()`: Removes outdated or erroneous cat profiles from the system. |
| Admin | This class is associated with `User` (but not a subclass) and holds elevated privileges for system oversight and maintenance. It includes the following methods: \- `activateAccount()`: Reactivates user accounts that were previously deactivated or newly registered. \- `deactivateAccount()`: Temporarily suspends user accounts (e.g., for investigation or inactivity). \- `banAccount()`: Permanently blocks users who violate terms or abuse the system. \- `deleteCatProfile()`: Removes cat profiles from the system, typically when added incorrectly or deemed inappropriate. \- `sendEmail()`: Sends system-generated or admin-composed emails (e.g., verification, alerts, feedback follow-up). \- `verifyDocuments()`: Used to manually or automatically verify user-uploaded documents, ensuring legitimacy (e.g., proof of identity, authorization letters). |

### **Diagram Explanation:**

This diagram illustrates an inheritance-based relationship, where IndividualVolunteer, OrganizationVolunteer, and HospitalStaff are all subclasses of the abstract User class. The admin class This design allows shared functionality (like login, logout, and account management) to be centralized in one location, reducing duplication and improving maintainability.

Key interactions and design principles include:

* **Polymorphism and Inheritance**: Common operations are defined in the User class and are extended or specialized in the derived classes.

* **Role-specific Responsibilities**: Each subclass defines attributes or methods specific to its purpose, e.g., HospitalStaff manages animal profiles, while Admin controls account statuses.

* **Data Encapsulation:** Each class manages its data fields, ensuring that responsibilities are well-distributed and logically separated.

This class diagram acts as a foundational blueprint for building a scalable, role-based user management system where each type of user has tailored access and capabilities depending on their responsibilities and permissions.

# **Tables**

These tables define the functional modules of the stray cat re-identification system, breaking down the key interactions between system actors (such as volunteers, animal hospital staff, and administrators) and the system itself. Each table outlines a specific feature or process such as user account management, image-based cat re-identification, cat profile handling, profile viewing, and system administration. For each module, the tables clearly present the relevant actors, use cases, data inputs and outputs, and expected system behaviors, along with important notes regarding privacy, access control, and system accuracy. Together, they provide a structured and detailed overview of how the system operates and how different roles interact with it to support accurate identification, data integrity, and volunteer coordination.

## **１Account Management**

| Item | Description |
| :---- | :---- |
| Actors | Volunteer, Administrator |
| Use Cases | \- U-1 Sign Up \- U-2 Log In \- U-3 Edit Account Details \- U-4 Delete Account \- U-14 Verify Account \- U-15 Activate Account |
| Description | Volunteers can create, log into, modify, and delete their accounts. Administrators verify and activate accounts to ensure only authorized volunteers access the system. |
| Data | email address, phone number,  password, user profile information (e.g., name), account status flags (e.g., verified, active) |
| Input | \- Sign-up form with user details \- Login credentials \- Edit/delete requests \- Admin verification actions |
| Output | \- Account created or updated \- Login success/failure message \- Account deletion confirmation \- Account status updated (e.g., activated) |
| Comments | Email verification and admin approval are required to activate accounts. Users cannot access certain features until verified and activated. |

## **2 Image Submission and Matching**

| Item | Description |
| :---- | :---- |
| Actors | Volunteer |
| Use Cases | \- U-5 Upload Image \- U-6 View Matching Result \- U-7 Report Incorrect Match |
| Description | Volunteers upload cat images for re-identification. The system displays potential matches based on image analysis. If the result is incorrect, users can report mismatches to help improve accuracy. |
| Data | Cat image, matching result, report reason |
| Input | \- Image upload via form or camera \- Click to view matching result \- Report form with reason for mismatch |
| Output | \- Matching results with confidence scores \- Confirmation of image upload \- Confirmation that a mismatch report has been submitted |
| Comments | Image quality significantly affects matching accuracy. Reports may be reviewed by admins or used to retrain the model. Duplicate or unclear images may result in no match. |

## **3 Cat Profile Management**

| Item | Description |
| :---- | :---- |
| Actors | Animal Hospital Staff , Administrator |
| Use Cases | \- U-9 Add Cat Profile \- U-10 Edit Cat Profile \- U-11 Delete Cat Profile \- U-16 Manage Cat Profile |
| Description | Animal hospital staff and administrators manage cat profiles, including creation, updating treatment details, and deletion or archival. |
| Data | Cat ID, physical traits, neuter status, medical records, treatment history, images, intake date, location |
| Input | \- Profile registration/edit forms \- Uploads of cat images and treatment details \- Deletion or archival requests |
| Output | \- Confirmation of successful creation/edit \- Updated or removed profile \- Records stored for reference and re-ID matching |
| Comments | Profile data should comply with medical data privacy. Admins can perform overrides or restore deletions. Change logs should be maintained. |

## **4 Profile Viewing**

| Item | Description |
| :---- | :---- |
| Actors | Animal Hospital Staff , Volunteer |
| Use Cases | \- U-8 View Cat Profile |
| Description | Volunteers and hospital staff view existing cat profiles to confirm ID or check medical history |
| Data | Cat profile details including ID, medical history, treatment records, and image set |
| Input | \- Search query (e.g., via ID, matching result) \- Click/view action |
| Output | \- Profile content displayed in structured layout \- Image and medical/treatment info displayed |
| Comments | Although both users can view the profile, animal hospital users have access to making changes to a cat’s profile as previously mentioned. |

## **5.User and System Management**

| Item | Description |
| :---- | :---- |
| Actors | Volunteer |
| Use Cases | \- U-12 Manage User Accounts \- U-13 View System Analytics \- U-19 Manage Re-ID Matches |
| Description | Administrators are able to manage user accounts (e.g., suspending or deleting them), monitor system analytics, and review or correct re-identification matching results. |
| Data | User account data, system logs, match history, usage statistics (e.g., login frequency, number of uploads) |
| Input | \- Admin dashboard actions (e.g., update user status) \- Requests to view reports or logs \- Actions to merge or delete incorrect matches |
| Output | \- Updated user account status \- Visualized analytics (e.g., charts, logs) \- Updated match records |
| Comments | These actions are restricted to administrators. Moreover, manual match management helps correct model misidentifications from user input/reports. Data integrity and audit trails should be maintained. |



## **6 Report Handling and Match Validation**

| Item | Description |
| :---- | :---- |
| Actors | Administrator |
| Use Cases | \- U-12 Manage User Accounts \- U-13 View System Analytics \- U-18 Receive User Reports \- U-19 Manage Re-ID Matches |
| Description | Admins manage user roles, monitor analytics, process reports submitted by users, and adjust or verify cat re-ID results. |
| Data | User credentials, access logs, analytics data, re-ID match logs, user-submitted reports |
| Input | \- Admin actions via dashboard \- Match result corrections \- User report review response |
| Output | \- Account status updates \- Analytics charts and summaries \- Match records corrected or flagged \- Report resolution notices |
| Comments | Admin dashboards support monitoring and system tuning. Match oversight supports model accuracy. Logs and audit trails are crucial for data accountability. |

