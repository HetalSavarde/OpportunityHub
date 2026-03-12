# 🚀 OpportunityHub
### AI-Powered Career Discovery Platform

> Built at **TechSprint Hackathon** · Atharva College of Engineering · Team project — my contributions: backend APIs, Gemini AI integration, Firebase Auth, GCP deployment

[![Node.js](https://img.shields.io/badge/Node.js-18+-6DA55F?style=flat&logo=node.js&logoColor=white)](https://nodejs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=flat&logo=Firebase&logoColor=white)](https://firebase.google.com)
[![Gemini API](https://img.shields.io/badge/Gemini_API-4285F4?style=flat&logo=google&logoColor=white)](https://ai.google.dev)
[![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat&logo=google-cloud&logoColor=white)](https://cloud.google.com)

---

## 1️⃣ What It Does

OpportunityHub is a smart career discovery platform that helps students and professionals find the right opportunities faster. 

The problem it solves: opportunity information is scattered across dozens of platforms, and most discovery tools are generic. OpportunityHub combines structured opportunity data with **AI-powered resume analysis** to deliver personalised, skill-based career recommendations — so users spend less time searching and more time applying.

**[▶ Watch the Demo](https://drive.google.com/file/d/1_qHcVGUvN4GtYu4ZDiO_os9V563NLSFh/view?usp=sharing)**

---

## 2️⃣ Tech Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| Backend | Node.js + Express.js | REST API server |
| Frontend | TypeScript + Vite | UI layer |
| AI | Google Gemini API | Resume parsing, skill extraction, recommendations |
| Auth | Firebase Authentication | Secure login & session management |
| Database | Firestore | Real-time opportunity + user data storage |
| Deployment | GCP Compute Engine + NGINX | Backend hosting & static file serving |
| Storage | Google Cloud Storage | Static assets |

> **Deployment note:** The GCP instance (E2 Micro, Ubuntu) is currently inactive to avoid ongoing costs. The platform was live on Google Cloud Compute Engine with NGINX as a reverse proxy during the hackathon. All deployment configs are available in the repo.

---

## 3️⃣ Key Features

- 🔍 **Smart Opportunity Discovery** — Jobs, internships, hackathons, and events in one place
- 🧠 **AI Resume Analyser** — Upload your resume, Gemini API extracts your skills automatically
- 🎯 **Personalised Recommendations** — Matched to your skill profile, not generic listings
- 📊 **Skill Gap Analysis** — See exactly what skills you're missing for your target roles
- ⭐ **Wishlist & Bookmarks** — Save and track opportunities you're interested in
- ⏰ **Deadline Panic Mode** — Highlights urgent opportunities you're about to miss
- 🔐 **Secure Auth** — Firebase Authentication with session management

---

## 4️⃣ My Contributions

Since this was a hackathon team project, here's specifically what I built:

- Designed and built all **backend REST APIs** (Node.js + Express)
- Integrated **Gemini API** for resume parsing, skill extraction, and gap analysis
- Implemented **Firebase Authentication** and **Firestore** data layer
- Handled full **GCP deployment** — provisioned Compute Engine instance, configured NGINX reverse proxy, managed environment setup on Ubuntu server

---

## 5️⃣ Running Locally

### Prerequisites
- Node.js v18+
- Firebase project (free tier works)
- Gemini API key ([get one free here](https://ai.google.dev))

### Backend
```bash
cd opportunityhub_backend
npm install
npm run dev
```

### Frontend
```bash
cd opportunityhub_frontend
npm install
npm run dev
```

### Environment Variables

Create `.env` in the backend folder:
```
GEMINI_API_KEY=your_key_here
FIREBASE_PROJECT_ID=your_project_id
FIREBASE_PRIVATE_KEY=your_private_key
FIREBASE_CLIENT_EMAIL=your_client_email
FIRESTORE_DATABASE_ID=your_db_id
```

---

## 6️⃣ Future Improvements

- 🔄 Real-time opportunity scraping via third-party APIs
- 📄 PDF resume upload and parsing
- 📈 ML-based opportunity ranking system
- 📊 User analytics dashboard
- 🌍 Multi-language support
- 🤖 Multimodal Gemini models for richer AI feedback

---

## 7️⃣ Impact

- Reduces time spent searching across scattered platforms
- Gives students a clear picture of their skill gaps and preparation path
- Scalable architecture designed for future AI feature expansion
- Built for students, freshers, and early-career professionals
