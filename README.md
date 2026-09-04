# FormFit 🏋️

An AI-powered fitness app that helps you train smarter — with real-time form checking, smart nutrition tracking, and a personal AI coach.

## What it does

- **AI Form Check** — Uses your camera and MediaPipe pose estimation to analyze your exercise form in real time, count reps, score your technique, and flag faults like knee valgus or shallow depth.
- **AI Food Scanner** — Take a photo of your meal and Claude AI identifies the food and estimates calories, protein, carbs, and fats automatically.
- **AI Coach** — Chat with a Claude-powered coach that knows your stats, split, and recent workouts. Ask about form, plateaus, recovery, or nutrition.
- **Fitness Score** — A composite score out of 100 based on body composition, strength, consistency, and form quality. Tracks your progress over 8 weeks.
- **Workout Planner** — Built-in training splits (PPL, Upper/Lower, Bro Split, Full Body, and more) with a 29-exercise library including form cues and demo GIFs.
- **Nutrition Tracker** — Daily macro and calorie tracking with TDEE-based targets that adjust based on your goal (cut / maintain / bulk).
- **Analytics** — Training heatmap, muscle group activation breakdown, and a strength plateau forecast.
- **Recovery Tracker** — Log sleep, soreness, and energy levels to get a daily readiness recommendation.
- **Achievements** — Unlock badges for streaks, form quality, and consistency milestones.

## Tech Stack

- **Frontend:** React Native (Expo) — runs on iOS, Android, and Web
- **Backend:** FastAPI + MongoDB
- **AI:** Claude Sonnet 4.6 (coach chat and food photo analysis)
- **Pose Engine:** MediaPipe running in a WebView

## Setup

**Backend**
```bash
cd backend
pip install -r requirements.txt
# add MONGO_URL, DB_NAME, JWT_SECRET, EMERGENT_LLM_KEY to backend/.env
uvicorn server:app --reload --port 8001
```

**Frontend**
```bash
cd frontend
yarn install
# set EXPO_PUBLIC_BACKEND_URL in frontend/.env
yarn start
```
