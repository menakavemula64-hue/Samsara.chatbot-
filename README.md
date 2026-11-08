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


  Om Namah Shivaya. 🔱
