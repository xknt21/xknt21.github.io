---
date: 2025-04-24T01:06:59+09:00
draft: false
title: '[Group Documentation] May 13 2025'
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
On May 13, our team focused on two major tasks:
- Finalizing the interview questions for animal shelters and organizations.
- Mapping responsibilities and categorizing non-functional requirements (NFRs) for each team member, aligned with key stakeholders.

---

# Interview Question Design – Animal Shelter Staff
We brainstormed and refined a comprehensive list of questions to ask shelter staff in our upcoming interviews. These questions aim to deepen our understanding of real-world workflows, adoption procedures, and the shelter’s technical readiness to collaborate with our system.

## Key Question Categories:

### Shelter Operations & Policy
- Do you assign IDs to every cat?
- Do you track released cats, and how?
- What criteria determine whether a cat is adoptable or released?
- How do you intake stray cats and prepare them for adoption?

### Adoption Process
- What are the main steps from visitor to legal adoption?
- What is the most common reason for returned adoptions?
- How long does a typical adoption take?

### Data Collaboration & Technical Feasibility
- Are you open to uploading images to a system like ours?
- How tech-friendly are your staff? Could mobile uploads help?
- Do you already collect multi-angle photos? If not, is it feasible?
- How much time would it typically take to register one cat?
- What metadata (age, vaccination, neutering, etc.) is stored?

### Communication Preferences
- Would you prefer direct contact with users or filtered communication via the app?
- How should the app handle messaging between your staff and adopters?

---

# NFR & Stakeholder Responsibility Assignment
We held a group planning session to assign stakeholders (RE) and non-functional requirement (NFR) categories to team members. These assignments were based on relevance to our system and individual roles. This also involved grouping NFRs into three main categories:

## Stakeholders (RE – Requirements Elicitation)
- A: General Citizens / Volunteers – **Jocelyn**
- B: System Administrator – **Anoma**
- C: Animal Shelter Staff – **Jonathan**
- D: External Ethics & Law – **Kanato**
- E: Performance & Adoption Process – **Parth**
- F: Local Governments – **Yukiya**
- G: System Developers/Engineers – **Ryusei**

## Non-Functional Requirement Categories:

### Product-Related
- Usability (**C**)
- Efficiency (**B**)
- Dependability (**B**)
- Security (**G**)
- Performance (**E**)
- Space optimization (**A**)

### Organizational
- Environmental fit (**F**)
- Operational ease (**A**)
- Development feasibility (**F**)

### External
- Regulatory requirements  
- Ethical and legal considerations (**D**)  
- Security/safety compliance (**D**)

This mapping will support a more structured approach during system modeling, requirement verification, and documentation.

---

We have talked about the interview questions for stakeholders.
