# Smart-Hire: Frontend Dashboard Layout

This directory houses the complete user interface layer for the **Smart-Hire** recruitment portal. Designed as a modern, high-performance Single Page Application (SPA), it provides intuitive modules for both HR recruiters and job applicants.

---

## 🛠️ UI Tech Stack
* **Core View Engine:** React.js
* **Styling Framework:** Bootstrap 5 & Custom CSS3
* **Mark-up Structure:** HTML5
* **Routing & Client States:** React Router DOM & React Hooks

---

## 💻 Core UI Modules & Interfaces

### 1. Unified Authentication Gateway
* **Login & Registration Screens:** Secure forms with client-side validation for Recruiters and Candidates.
* **Session Controls:** Manages JSON Web Tokens (JWT) locally to handle protected routing and persistent logins.

### 2. Candidate Portal
* **Dynamic Profile Builder:** Allows candidates to manage personal details and profile inputs.
* **Interactive Drag-and-Drop Uploader:** A responsive dropzone area built to upload resumes (PDF/DOCX formats).

### 3. HR Recruiter Control Panel
* **Job Posting Hub:** Form metrics to submit new job listings, including role titles, core skills, and experience constraints.
* **Applicant Comparison Leaderboard:** A real-time data table displaying calculated match percentages ($0\%$ to $100\%$) and applicant status tags.
* **Data Visualization Dashboards:** Built using graphical elements to track candidate pools and skill density analytics.

---

## ⚡ Local Setup & Deployment

To launch the frontend dashboard locally, make sure you have **Node.js** installed, then run the following commands inside this directory:

```bash
# 1. Install project dependencies
npm install

# 2. Run the application in development mode
npm start
