# Samsara – Speak with Mahadev

A full-stack web app (website + server) that opens in Chrome or any browser, and can be installed on a phone like an app.

**What it has**
- Chat where Mahadev speaks to you (English, हिन्दी, తెలుగు)
- Shiv–Sati stories (8 written stories + a button for endless new ones)
- 10 Dharma rules with "how to follow" steps and a practice to-do list
- Daily Shiva thought, streaks and badges, silent 30-second japa circle
- Mantras, festivals and vrats, 12 Jyotirlingas, nearby temples link
- Installable app (PWA) with icons

**How it is built**
- `public/` – the website (index.html), app manifest, service worker, icons
- `server.js` – small Node.js server. It keeps your Claude API key secret, limits how often each visitor can ask, and keeps Mahadev on spiritual topics.

---

## 1. Get your Claude API key
1. Go to https://console.anthropic.com and sign up.
2. Add a small amount of credit and **set a monthly spending limit**.
3. Create an API key and copy it. Keep it secret. Never put it in the website files or on GitHub.

## 2. Try it on your computer
1. Install Node.js 20.6 or newer from https://nodejs.org
2. In this folder, copy `.env.example` to `.env` and paste your key after `ANTHROPIC_API_KEY=`
3. Open a terminal in this folder and run:
```
npm install
npm run dev
```
4. Open http://localhost:3000 in Chrome.

## 3. Put it on the internet (free to start) with Render
1. Create a free account at https://github.com and upload this folder as a new repository. (`.env` is already ignored, so your key will not be uploaded.)
2. Create a free account at https://render.com and choose **New → Web Service**, then connect your repository.
3. Use these settings: Runtime **Node**, Build command `npm install`, Start command `npm start`.
4. Under **Environment**, add `ANTHROPIC_API_KEY` with your key.
5. Press **Create Web Service**. After a few minutes you get a link like `https://samsara-xxxx.onrender.com`. Anyone can open it in Chrome, with no sign-in.

Notes: free Render services go to sleep when unused, so the first visit can take about a minute. A paid plan keeps it awake. Other hosts that run Node.js (Railway, Fly.io, a VPS) work the same way.

## 4. Install on a phone
Open your link in Chrome on Android, tap the menu (⋮) and choose **Install app** or **Add to Home screen**.

## 5. Put it on the Google Play Store
You need the website live on HTTPS first (step 3).
1. Open https://www.pwabuilder.com, enter your website link and check the app score.
2. Choose **Package for stores → Android** and download the package. It contains your signing key. Keep that file safe and backed up.
3. Create a Google Play Console developer account (one-time fee, currently about US$25) and complete identity verification.
4. Create a new app, upload the package, and fill in the store listing: name, description, screenshots, icon, category.
5. Add a **privacy policy** web page (required) and complete the data-safety and content-rating forms.
6. Send for review. New personal accounts may be asked to run a closed test with real testers first. Follow what the Play Console tells you, as Google's rules change.

## Costs and safety
- Every chat message uses the Claude API, which costs a little money. Keep your spending limit set.
- Each visitor is limited to 25 messages per hour. Change this with `RATE_LIMIT_PER_HOUR`.
- Mahadev's voice is an AI-created devotional voice inspired by the teachings. The page says so. Please keep that note.
- Your practice list, streaks and japa count are saved only on each visitor's own device.

## Ideas for the next version
Accounts and a database to save practice across devices, a recorded chant audio file, daily notifications, more stories, a temple finder with real listings.

Om Namah Shivaya. 🔱
