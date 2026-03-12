# OpportunityHub — Setup Guide

A step-by-step guide to running and testing the project locally.

---

## 🛠️ Step 1: Prerequisites

Before starting, make sure you have:
- Node.js v18+
- A Firebase project with Firestore enabled
- A Gemini API key ([get one free here](https://ai.google.dev))

---

## ⚙️ Step 2: Environment Setup

### Backend (`/backend`)

Create a `.env` file in the `backend/` folder:
```
GEMINI_API_KEY=your_gemini_api_key
FIREBASE_PROJECT_ID=your_project_id
```

Also place your Firebase service account file as `firebaseKey.json` in the `backend/` root.  
> ⚠️ Never commit `firebaseKey.json` or `.env` to GitHub — these are in `.gitignore`

### Frontend (`/frontend`)

Create a `.env` file in the `frontend/` folder:
```
VITE_API_URL=http://localhost:8000
```

---

## 🚀 Step 3: Running the Project

### 1. Seed the database (first time only)
```bash
cd backend
node seed.js
```

### 2. Start the backend
```bash
cd backend
npm install
npm run dev
```

### 3. Start the frontend
```bash
cd frontend
npm install
npm run dev
```

App runs at **http://localhost:5173** (or 5174 if 5173 is in use)

---

## 🧪 Step 4: Test Cases

### Test 1 — New User Signup & Onboarding
1. Go to the landing page → click **Get Started**
2. Sign up with any email and password
3. On the onboarding page, select **Web Development** and **Remote**
4. **Expected:** Redirected to Home with relevant opportunities (e.g. "Frontend Developer Intern" with a high match score)

### Test 2 — Opportunity Matching & Links
1. On the Home page, find any opportunity card (e.g. Smart India Hackathon)
2. Check that a **Match Score %** is visible
3. Click **Register Now / Apply Now**
4. **Expected:** Opens the official opportunity website in a new tab

### Test 3 — AI Resume Analyser (Gemini API)
1. Navigate to **Resume Analysis** from the sidebar
2. Paste any resume text in the left box
3. Paste a job description in the right box
4. Click **Analyze Resume Match**
5. **Expected:**
   - Match Score appears
   - Key Strengths lists your technical skills
   - Scope of Improvement lists missing skills
   - Project Ideas suggests what to build next

### Test 4 — Wishlist & Deadline Tracker
1. Bookmark 2–3 opportunities using the bookmark icon
2. Check the **Upcoming Deadlines** sidebar
3. **Expected:** Wishlisted items appear with "X days left", urgent ones highlighted in red

### Test 5 — Returning User Session
1. Log out from the profile menu
2. Log back in with the same credentials
3. **Expected:** Dashboard loads with your previous preferences and wishlist intact
