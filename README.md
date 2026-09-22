# AI Tool Hub — Connected

This version connects the React/Vite frontend to an Express backend for:

- OpenAI text generation for AI Chat, Resume, Cover Letter, Interview Prep, Writer, Summarizer and invitation briefs.
- OpenAI image generation for invitation artwork.
- Razorpay order creation and server-side signature verification.
- Email/password signup and login with hashed passwords and JWT sessions.
- Paid plan entitlement after verified payment.
- Invitation Studio: Wedding, Engagement, Birthday and Party packages.

## 1. Install

```bash
npm install
cd server
npm install
```

## 2. Configure server

Copy `server/.env.example` to `server/.env` and add your own credentials. **Never commit `.env` or expose the Razorpay secret in frontend code.**

## 3. Run

Terminal 1:
```bash
cd server
npm run dev
```

Terminal 2:
```bash
npm run dev
```

Frontend: `http://localhost:5173`
Backend: `http://localhost:5000`

## 4. Production

Use HTTPS, a strong random JWT_SECRET, a real database, verified Razorpay webhooks, rate limiting, logging/monitoring, and proper user/role access controls before launch. The included JSON store is a simple starter and is not intended for a high-traffic production database.

## API configuration

`VITE_API_URL` points the frontend to the backend. The backend uses `OPENAI_API_KEY`, `OPENAI_TEXT_MODEL`, `OPENAI_IMAGE_MODEL`, `RAZORPAY_KEY_ID`, `RAZORPAY_KEY_SECRET`, and `JWT_SECRET`.

## Video Editor
The site now includes a browser-based Video Editor. Users can upload a local video, trim start/end points, change playback speed, mute audio, preview the edit, and export a WebM file. The basic editor processes the video locally in the browser and does not upload the source video. More advanced AI video editing (automatic captions, background removal, generative effects, etc.) can be connected later through a server-side video provider.
