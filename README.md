# Prompt Maestro — public web app

A single-page tool: someone opens the link, describes what they want, answers 1–3 quick questions, and gets a copy-ready prompt tuned to their chosen AI model. Built to run on **GitHub Pages**.

## What it does
- Accepts messy/short input — does the thinking for you.
- Asks 1–3 sharp clarifying questions before writing anything.
- Returns a copy-ready prompt in the target model's dialect (Claude, ChatGPT, Gemini, Midjourney, etc.).
- Adds a gentle nudge if your input looks off-track.
- ⓘ buttons on each field explain the best practice.

## v1 key model (important)
GitHub Pages is **static hosting** — there's no server to safely hold a secret API key. So v1 is **bring-your-own-key**: each user opens ⚙︎ API settings once and pastes their own Gemini / Anthropic / OpenAI key (stored only in their browser). Gemini is the most reliable from a website.

> To make it truly keyless ("anyone clicks the link, no key needed"), we add a small serverless proxy later (e.g. a Cloudflare Worker) holding one key you fund, plus a rate limit. That's a planned phase-2 — see DECISIONS.md.

## Deploy to GitHub Pages (≈3 minutes, no coding)
1. Go to https://github.com and sign in (or create a free account).
2. Click **New repository** → name it e.g. `prompt-maestro` → keep it **Public** → **Create repository**.
3. On the repo page click **Add file → Upload files**, drag in this `index.html` (and this README), then **Commit changes**.
4. Go to **Settings → Pages** (left sidebar).
5. Under **Build and deployment → Source**, choose **Deploy from a branch**; pick branch **main** and folder **/(root)**; click **Save**.
6. Wait ~1 minute, refresh. Your live link appears at the top: `https://<your-username>.github.io/prompt-maestro/`.
7. Open it, set your API key once in ⚙︎ settings, and share the link.

## Update it later
Re-upload a new `index.html` via **Add file → Upload files** (or edit in place). Pages redeploys automatically in ~1 minute.

## Files
- `index.html` — the whole app (self-contained).
- `README.md` — this guide.
