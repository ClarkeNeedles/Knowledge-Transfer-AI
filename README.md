# Knowledge-Transfer-AI

[![license](https://img.shields.io/github/license/GitNH27/Knowledge-Transfer-AI)](LICENSE)
[![repo size](https://img.shields.io/github/repo-size/GitNH27/Knowledge-Transfer-AI)]()

---

## 🎥 Demo

A quick preview of the application in action:

[Watch Demo Video](https://drive.google.com/file/d/1xD2CTgI4FeX9NKzK9SEC7dRxyByERnEQ/view?usp=sharing)

---

## 🧠 Overview

Knowledge-Transfer-AI is a full-stack AI-powered learning platform that generates and delivers role-tailored educational content through a structured onboarding system, lecture management interface, and interactive AI-driven learning experience.

It combines:
- React frontend UI
- Custom backend knowledge system (RAG-style architecture)
- Backboard API for AI orchestration
- ElevenLabs API for text-to-speech generation

---

## Table of contents
- [What this project does](#what-this-project-does)
- [Why this is useful](#why-this-is-useful)
- [Key features](#key-features)
- [Tech stack](#tech-stack)
- [Repository layout](#repository-structure)
- [Getting started](#getting-started)
- [Environment variables](#environment-variables)
- [How to use](#how-to-use)
- [System flow](#system-flow)
- [Why this project matters](#why-this-project-matters)
- [Support](#support)
- [License & acknowledgements](#license--acknowledgements)

---

## What this project does

- Generates personalized learning paths based on user role and industry
- Retrieves knowledge using a backend RAG pipeline
- Generates AI explanations and summaries for lectures
- Converts learning content into natural speech using ElevenLabs
- Provides an interactive “Learn” experience for users

---

## Why this is useful

- Rapidly prototype AI-enhanced learning experiences for teams and users
- Role- and industry-aware onboarding flows to tailor content
- Modern frontend stack (React + Tailwind + Material components) for fast UI development
- Clear separation of the UI from API/back-end so you can connect any AI backend or mock service

---

## Key Features

- Role-based onboarding flow for personalization
- Lecture browsing and management system
- AI-generated learning content per lecture
- Text-to-speech narration for lessons
- Backend-driven knowledge retrieval system (RAG)
- Modular and scalable frontend architecture
- External AI service integration (Backboard + ElevenLabs)

---

## Tech Stack

### Frontend
- React
- Vite
- JavaScript (ES6+)
- Tailwind CSS
- Material Tailwind UI

### Backend / Knowledge System
- Custom knowledge ingestion pipeline
- RAG-style retrieval system (chunking + semantic search layer)
- REST API service layer
- Environment-based configuration (VITE_API_URL)

### AI Services
- Backboard API (AI generation / orchestration)
- ElevenLabs API (text-to-speech synthesis)

### Architecture
- RESTful API communication between frontend and backend
- Service-layer abstraction (`src/services/api`)
- Decoupled frontend/backend design
- External AI service integration layer

### Tooling
- Vite build system
- npm / yarn / pnpm
- ESLint
- Git / GitHub

---

## Repository Structure

Important paths (relative links):
* `frontend/react-app/` — Main React application (UI layer). Built with React + Vite + Tailwind + Material Tailwind. Handles onboarding, lectures, and AI learning experience.

  * `frontend/react-app/src/pages/` — Core pages (Onboarding, Lectures, Learn, etc.)
  * `frontend/react-app/src/services/api/` — API abstraction layer for backend + external AI services (Backboard + ElevenLabs)
  * `frontend/react-app/src/main.jsx` — Application entry point
  * `frontend/react-app/src/App.jsx` — Root app structure and routing
  * `frontend/react-app/package.json` — Frontend dependencies and scripts

* `backend/` — Python-based AI knowledge system and API layer (RAG + orchestration backend)

  * `backend/main.py` — Main backend entry point (API server + orchestration logic)
  * `backend/models.py` — Data models / schemas used across ingestion and retrieval system
  * `backend/requirements.txt` — Python dependencies for backend services
  * `backend/sessions.db` — SQLite database for session storage and tracking

* `backend/services/` — Core AI and external service integrations

  * `backend/services/backboard_llm.py` — LLM interface using Backboard API for AI generation
  * `backend/services/backboard_rag.py` — Retrieval-Augmented Generation (RAG) pipeline implementation
  * `backend/services/backboard_service.py` — Core service wrapper for Backboard API orchestration
  * `backend/services/eleven_labs.py` — ElevenLabs text-to-speech integration (voice synthesis)

* `backend/session_cache/` — Temporary runtime/session storage for AI interactions and user sessions

* `README.md` — Main project documentation (overview, architecture, setup, usage)
* `LICENSE` — Repository license file (MIT or specified license)

---

## Getting Started

### Prerequisites
- Node.js 16+
- npm / yarn / pnpm
- Backend API running (or mock server)
- API keys for Backboard + ElevenLabs (if enabled)

---

### Frontend Setup

```bash
git clone https://github.com/GitNH27/Knowledge-Transfer-AI.git
cd Knowledge-Transfer-AI/frontend/react-app
npm install
npm run dev
````

Open:

http://localhost:5173 or similar

---

## Environment Variables

Create a `.env.local` file:

VITE_API_URL=[https://your-backend-api.com](https://your-backend-api.com)

Important:

* Do NOT expose AI API keys in frontend
* Backboard + ElevenLabs keys should remain server-side

---

## How to Use

* Select role in onboarding
* Browse generated lectures
* Open “Learn” page for AI explanations
* Listen to audio narration (ElevenLabs)
* Extend API layer in `src/services/api`

---

## System Flow

1. User completes onboarding (role + industry)
2. Frontend requests personalized content
3. Backend retrieves relevant knowledge via RAG system
4. Backboard API generates AI responses
5. ElevenLabs converts text to speech
6. Frontend renders interactive learning experience

---

## Why This Project Matters

* Demonstrates real-world AI integration
* Combines retrieval + generative AI + speech synthesis
* Shows scalable full-stack architecture
* Mirrors production-grade AI learning platforms

---

## Support

* GitHub Issues for bugs or feature requests
* Frontend docs in `frontend/react-app/README.md`
* Backend modules extend `/backend` directory

---

## License & Acknowledgements

MIT License

Credits:

* Material Tailwind
* Creative Tim templates
* Backboard API
* ElevenLabs
* React + Vite ecosystem
