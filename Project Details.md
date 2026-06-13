# SMART-HIRE: NLP-BASED RESUME PARSING AND CANDIDATE RANKING SYSTEM
## 1. PROJECT TITLE
**Smart-Hire: NLP-Based Resume Parsing and Candidate Ranking System using Machine Learning**
---
## 2. PROBLEM STATEMENT
Traditional recruitment processes are incredibly time-consuming and prone to human bias. HR managers often have to manually sift through hundreds of resumes (PDF/Word format) for a single job opening, making it easy to miss qualified candidates. There is a critical need for an automated, intelligent system that can parse unstructured resumes, extract key skills/experience using Natural Language Processing (NLP), and rank candidates accurately based on job descriptions.
---
## 3. PROJECT OBJECTIVES
### Primary Objectives:
* Build an automated recruitment platform to parse unstructured resumes in real-time.
* Utilize Natural Language Processing (NLP) to extract entity data like Skills, Experience, Education, and Contact Info.
* Implement Machine Learning algorithms (Cosine Similarity/TF-IDF) to score and rank candidates against specific Job Descriptions (JD).
### Secondary Objectives:
* Provide a clean dashboard for HR/Recruiters to post jobs and view top-ranked candidates instantly.
* Secure applicant data and resume files using industry-standard backend practices.
* Generate analytical reports on the candidate pool for better talent acquisition insights.
---
## 4. MODULE LIST
### Module 1: User & Authentication Management
* **Features:** Secure login and registration for Recruiters/HR and Candidates, role-based dashboards, and JWT authentication.
### Module 2: Resume Ingestion & NLP Parsing
* **Features:** Drag-and-drop resume upload (PDF/Docx), text extraction, and Named Entity Recognition (NER) using NLP to identify skills, experience, and education.
### Module 3: Job Description (JD) Management
* **Features:** HR portal to create, edit, and publish job vacancies with mandatory skills, experience level, and qualification requirements.
### Module 4: ML Ranking & Recommendation Engine
* **Features:** Feature extraction using TF-IDF, similarity scoring between parsed resumes and JDs, and dynamic candidate ranking generation.
### Module 5: Recruiter Analytics & Notification
* **Features:** Interactive charts showing top applicants, automated email notifications to shortlisted candidates, and ranking report downloads.
---
## 5. DATABASE TABLE LIST (Based on 1000119968.jpg Tech Stack)

| S.No | Table Name | Description |
| :--- | :--- | :--- |
| 1 | **USERS Table** | Stores login credentials, roles (HR/Admin/Candidate), and account verification status. |
| 2 | **JOB_POSTINGS Table** | Stores job details posted by HR, including Title, Required Skills, and Min Experience. |
| 3 | **CANDIDATE_PROFILES** | Logs parsed applicant data like Name, Email, extracted Skills, and total Years of Experience. |
| 4 | **RESUME_FILES Table** | Manages metadata of uploaded resumes, including the safe File_Path/URL and Upload_Date. |
| 5 | **RANKING_REPORTS** | Stores ML-generated Cosine Similarity scores, final match percentages, and rank for specific jobs. |
| 6 | **NOTIFICATIONS Table** | Logs automated email/SMS trigger statuses for shortlisting or interview updates. |

---
## 6. EXPECTED OUTCOME
The **Smart-Hire** platform will revolutionize talent acquisition by reducing resume screening time from hours to seconds. By combining powerful Java Spring Boot enterprise backend with Python NLP models, the system ensures a highly scalable, objective, and accurate candidate shortlisting workflow, helping companies hire the right talent instantly.
