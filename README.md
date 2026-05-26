# CitySync — AI-Driven Civic Complaint Management System

An AI-powered complaint prioritization platform for urban local bodies,
replacing manual triage with dynamic NLP + ML-based scoring.


---

## The Problem

Municipal complaint systems use first-come-first-served queuing.
A minor paint issue filed in the morning gets resolved before
a burst water main filed hours later — purely due to queue position.

CitySync fixes this with a priority-per-cost scoring model.

---

## How It Works
Citizen Complaint (text + metadata)
↓
NLP Severity Extraction (spaCy)
↓
Feature Vector Construction
↓
ML Priority Scoring (XGBoost)
↓
Dynamic Priority Queue → Municipal Dashboard

---

## Features

- Multi-channel complaint submission (web form)
- NLP pipeline for severity and urgency extraction from free text
- XGBoost priority scoring model with cost-efficiency adjustment
- Real-time re-prioritization based on recurrence and new complaints
- Emergency override capability
- Dashboard with live complaint queue and priority scores

---

## Tech Stack

| Layer     | Technology                        |
|----------|------------------------------------|
| Frontend  | React + Vite + Tailwind CSS       |
| Backend   | Python + FastAPI                  |
| NLP       | spaCy (keyword-based extraction)  |
| ML Model  | XGBoost via scikit-learn          |
| Database  | PostgreSQL (Supabase)             |
| Auth      | Supabase Auth                     |

---

## Running Locally

### Backend
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

### Frontend
```bash
cd frontend
npm install
npm run dev
```

### Environment Variables
SUPABASE_URL=https://yozeywipovqbxtflkrxw.supabase.co
SUPABASE_KEY = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InlvemV5d2lwb3ZxYnh0Zmxrcnh3Iiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTc3NTQ1NjkxMiwiZXhwIjoyMDkxMDMyOTEyfQ.WGNReTX8Go7-p1t0dRumBGN7tVSF2bTkF9Y88zsg-Pg"

## Authors
Joyjeet Adhikary      
Sanjay S         
*Introduction to AI (course project), MIT Manipal*
