# GeeseTalk

GeeseTalk is a speech-practice platform that helps users improve speaking skills with structured learning and AI-driven feedback.

## Tech stack

- Frontend: Next.js 15, React 19, Tailwind CSS, Flowbite React, Framer Motion
- Backend: Python Flask, Flask-CORS
- AI / media processing: Google Generative AI SDK, custom audio/video feedback handlers
- Database / Auth (frontend project): Prisma, NextAuth, PostgreSQL-compatible drivers

## Main features

- Landing page and learning experience for speaking practice
- Practice themes: Interview Prep, Casual Talk, Public Speaking, Debates
- Audio upload endpoint for speech analysis and feedback
- Video upload endpoint for mode-based evaluation and response
- Real-time UI interactions and progress roadmap components
- Separate conversational agent prototype in `next-conv-ai`

## Project structure

- `geesehacks2025-nextjs/` – main frontend app
- `BackEnd/` – Flask API with audio/video upload routes and AI feedback
- `next-conv-ai/` – secondary conversational agent Next.js project
- `env_name/` – Python virtual environment for backend dependencies

## Backend capabilities

- `/upload_audio` handles Base64-encoded audio files
- `/upload_video` handles Base64-encoded video files
- Theme-specific processing via `NEW_TEST.py` for interview, casual talk, public speaking, and debate modes

## How to run

1. Install backend Python dependencies:
   ```bash
   cd BackEnd
   pip install -r requirements.txt
   ```
2. Start the Flask server:
   ```bash
   python server.py
   ```
3. Start the frontend app:
   ```bash
   cd geesehacks2025-nextjs
   npm install
   npm run dev
   ```

> Open the frontend at `http://localhost:3000` and connect it to the backend API for audio/video practice.
