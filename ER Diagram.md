# Smart-Hire: Entity-Relationship (ER) Diagram & Data Architecture

This directory contains the detailed structural layout and relational database entities governing the **Smart-Hire** recruitment engine. The database design maps critical connections between system users, job posting metrics, candidates' profile data, and Machine Learning leaderboard indices.

---

## 📊 Entity Relationship Mapping & Cardinality

The system architecture utilizes standard relational matrices, maintaining high data normalization (3NF) across core business workflows:

1. **USERS ↔ CANDIDATE_PROFILES (1-to-1 Relationship)**
   * Each dynamic profile entity strictly maps to a single authenticated user account containing unique security credentials.
2. **USERS ↔ JOB_POSTINGS (1-to-Many Relationship)**
   * An HR Recruiter user can upload and manage multiple structural job openings inside the system tracker.
3. **USERS ↔ RESUME_FILES (1-to-1 Relationship)**
   * Each job candidate account is mapped to their unique multi-part resume document storage profile path.
4. **JOB_POSTINGS ↔ RANKING_REPORTS (1-to-Many Relationship)**
   * Every published job posting aggregates a collection of multiple candidate evaluation matrices and scores.
5. **CANDIDATE_PROFILES ↔ RANKING_REPORTS (1-to-Many Relationship)**
   * A single applicant's structured profile analytics can be scored and evaluated across multiple distinct job applications.

---

## 📐 ER Diagram Structural Attributes

### 1. `USERS` Entity
* `user_id` (INT, Primary Key) — Unique user tracker.
* `email` (VARCHAR) — Security login token.
* `password` (VARCHAR) — Encrypted credential string.
* `role` (ENUM) — Dynamic roles (`HR_RECRUITER`, `CANDIDATE`).

### 2. `JOB_POSTINGS` Entity
* `job_id` (INT, Primary Key) — Unique job vacancy tracker.
* `recruiter_id` (INT, Foreign Key referencing `USERS.user_id`).
* `job_title` (VARCHAR) — Target employment role designation.
* `required_skills` (TEXT) — Mandatory expertise thresholds.
* `min_experience` (INT) — Total target professional experience duration.

### 3. `CANDIDATE_PROFILES` Entity
* `profile_id` (INT, Primary Key) — Parsed resume entity index.
* `user_id` (INT, Foreign Key referencing `USERS.user_id`).
* `full_name` (VARCHAR) — Candidate identity text.
* `extracted_skills` (TEXT) — List of professional skills captured by Spacy NLP.
* `years_of_experience` (INT) — Automated computed duration tracking score.

### 4. `RESUME_FILES` Entity
* `file_id` (INT, Primary Key) — Binary system storage file tracker.
* `user_id` (INT, Foreign Key referencing `USERS.user_id`).
* `secure_file_path` (VARCHAR) — Target path mapping for server object uploads.

### 5. `RANKING_REPORTS` Entity
* `report_id` (INT, Primary Key) — Dynamic scoring computation index.
* `job_id` (INT, Foreign Key referencing `JOB_POSTINGS.job_id`).
* `profile_id` (INT, Foreign Key referencing `CANDIDATE_PROFILES.profile_id`).
* `cosine_similarity_score` (DOUBLE) — Core Python ML calculation output.
* `match_percentage` (DOUBLE) — Scale representation of compliance matrix.
* `rank_index` (INT) — Position indicator inside the HR leaderboard array.

## 🖼️ Visual ER Diagram Layout

![Smart-Hire ER Diagram](./er-diagram.jpg)
