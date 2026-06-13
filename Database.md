# Smart-Hire: Relational Database Schema & Architecture

This directory manages the core relational database configurations, structural schemas, and entity relationships for the **Smart-Hire** platform. The system utilizes **MySQL** to maintain data integrity, secure transactional applicant logs, and optimize query paths for candidate ranking leaderboards.

---

## 🛠️ Database Stack
* **Database Engine:** MySQL (v8.0+)
* **ORM Mapper:** Hibernate / Spring Data JPA
* **Schema Design:** 3rd Normal Form (3NF) Relational Grid

---

## 📊 Core Relational Tables & Entities

The platform structures recruitment information across the following core schema matrices:

### 1. `USERS` Table
* **Purpose:** Handles application credentials and role definitions.
* **Core Columns:** `user_id (PK)`, `email (Unique)`, `password (Encrypted)`, `role (HR / CANDIDATE)`, `created_at`.

### 2. `JOB_POSTINGS` Table
* **Purpose:** Stores corporate job parameters uploaded by recruiters.
* **Core Columns:** `job_id (PK)`, `recruiter_id (FK)`, `job_title`, `required_skills`, `min_experience`, `job_description_text`.

### 3. `CANDIDATE_PROFILES` Table
* **Purpose:** Houses structured entity elements parsed from raw resumes via NLP.
* **Core Columns:** `profile_id (PK)`, `user_id (FK)`, `full_name`, `extracted_skills`, `years_of_experience`, `education_metrics`.

### 4. `RESUME_FILES` Table
* **Purpose:** Manages safe system paths and storage links for uploaded documents.
* **Core Columns:** `file_id (PK)`, `user_id (FK)`, `file_name`, `secure_file_path`, `upload_date`.

### 5. `RANKING_REPORTS` Table
* **Purpose:** Logs Machine Learning compliance coefficients and dynamic match results.
* **Core Columns:** `report_id (PK)`, `job_id (FK)`, `profile_id (FK)`, `cosine_similarity_score`, `match_percentage`, `rank_index`.

---

## ⚙️ Data Initialization & Deployment

To build and verify the relational pipeline locally:

1. **Schema Initialization:**
   Log into your local MySQL CLI or workbench tools and run:
   ```sql
   CREATE DATABASE smarthire_db;
   USE smarthire_db;
