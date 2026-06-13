# Smart-Hire: Enterprise Backend Core

This directory contains the core enterprise backend architecture for the **Smart-Hire** recruitment platform. Built using **Java and Spring Boot**, this layer orchestrates the core business logic, handles secure database persistence, enforces access control, and integrates with the Python ML routing network.

---

## 🛠️ Backend Tech Stack
* **Primary Framework:** Java, Spring Boot (v3.x)
* **Security & Token Management:** Spring Security & JWT (JSON Web Tokens)
* **Data Access Layer:** Spring Data JPA (Hibernate)
* **Database Engine:** MySQL
* **Build Architecture Tool:** Maven

---

## ⚙️ Core Architectural Modules

### 1. Security & Authentication Layer
* **Role-Based Access Control (RBAC):** Restricts API access points dynamically between `ROLE_RECRUITER` and `ROLE_CANDIDATE`.
* **State-Free JWT Security:** Issues secure tokens upon successful login to authorize subsequent frontend dashboard REST requests.

### 2. Candidate & Resume Pipeline
* **File Processing Controllers:** Provides secure multi-part REST endpoints to ingest uploaded application documents (PDF/DOCX formats).
* **Metadata Persistence:** Maps candidate metrics, extracted skill profiles, and professional credentials cleanly into relational tables.

### 3. Recruiter Job Hub
* **Job Matrix Management:** Controllers to handle the creation, retrieval, updating, and deletion (CRUD) of job parameters and skill criteria.
* **ML Router Orchestration:** Automatically pipes unstructured text data to the Python AI engine and saves the resulting compliance rank.

### 4. Transactional Alerts
* **Notification Logs:** Manages messaging tracking schemas to signal candidate screening status updates or interview confirmations.

---

## 🚀 Local Installation & Setup

To run the backend server on your machine, ensure you have **Java JDK 17+** and **MySQL** installed, then follow these steps:

1. **Database Setup:**
   * Create a database schema in your MySQL instance:
     ```sql
     CREATE DATABASE smarthire_db;
     ```
   * Configure your database credentials inside `src/main/resources/application.properties`.

2. **Run the Application:**
   * Execute the following Maven command inside this folder to compile and boot the application:
     ```bash
     mvn spring-boot:run
     ```

The enterprise server will initialize and listen for incoming frontend REST traffic at `http://localhost:8080`.
