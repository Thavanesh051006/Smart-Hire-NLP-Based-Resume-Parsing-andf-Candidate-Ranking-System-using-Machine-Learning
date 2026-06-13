# Smart-Hire: NLP-Based Resume Parsing and Candidate Ranking System

## 1. Project Abstract
Smart-Hire is an intelligent recruitment platform designed to automate the manual resume screening process. By leveraging **Natural Language Processing (NLP)** and **Machine Learning (ML)**, the system extracts structured information from unstructured resume files (PDF/DOCX) and dynamically ranks candidates based on their match percentage with job descriptions. This solution aims to reduce recruitment time by 80% and eliminate human bias in talent acquisition.

---

## 2. Problem Statement
* **High Volume:** HR managers struggle to manually screen hundreds of resumes per job opening.
* **Unstructured Data:** Resumes come in various formats, making keyword-based searches inefficient.
* **Human Bias:** Manual screening is prone to subjective bias and fatigue.
* **Delayed Hiring:** The manual process slows down the overall recruitment cycle, leading to the loss of top talent.

---

## 3. Project Objectives
* **Automated Parsing:** Use NLP (SpaCy) to extract skills, experience, and education from resumes.
* **Algorithmic Ranking:** Implement TF-IDF and Cosine Similarity to calculate match scores.
* **Scalable Architecture:** Build a full-stack system using Java Spring Boot and React.js.
* **Data Security:** Ensure candidate privacy using Spring Security and JWT.

---

## 4. System Modules
1. **User Authentication:** Secure JWT-based login for HR and Candidates.
2. **Resume Parser:** NLP engine to extract text and entities (Skills, Experience, etc.).
3. **Job Management:** HR portal to post and manage job requirements.
4. **Ranking Engine:** ML model to score resumes against job requirements.
5. **Analytics Dashboard:** Visual charts to view top-ranked candidates.

---

## 5. Technical Stack
* **Frontend:** React.js, Bootstrap 5
* **Backend:** Java, Spring Boot, Spring Security (JWT)
* **Database:** MySQL
* **AI/ML:** Python (FastAPI, SpaCy, Scikit-Learn)

---

## 6. Machine Learning Logic
1. **Text Extraction:** Raw text is pulled from uploaded documents.
2. **Vectorization:** Text is converted into mathematical vectors using **TF-IDF**.
3. **Similarity Scoring:** **Cosine Similarity** is calculated to find the match percentage between the Resume and Job Description.
4. **Leaderboard:** Candidates are sorted based on their match percentage.

---

## 7. Database Architecture
* **USERS:** Stores credentials and roles.
* **JOB_POSTINGS:** Stores requirements and descriptions.
* **CANDIDATE_PROFILES:** Stores extracted skills and parsed metrics.
* **RESUME_FILES:** Manages file metadata and paths.
* **RANKING_REPORTS:** Stores match scores and rank index.

---

## 8. Impact
* **Efficiency:** Reduces resume screening time by 80%.
* **Objectivity:** Ensures a merit-based, bias-free selection process.
* **Scalability:** Handles a large volume of applications effortlessly.
*
