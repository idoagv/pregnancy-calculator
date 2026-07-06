# Pregnancy Calculator

A self-contained, client-side pregnancy calculator. No server, no build step —
a single `index.html` with inline CSS and JavaScript.

## Features
- Estimated due date (Naegele's rule, with cycle-length adjustment)
- Current gestational age and trimester
- Days remaining
- Israeli prenatal ultrasound screening windows (passed / current / upcoming)
- Two input modes: by last menstrual period, or by current gestational age
- Hebrew / English with RTL/LTR support (preference saved in `localStorage`)

## Development
It's a single static file. Open `index.html` in a browser, or serve the folder:

```
python -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy to Vercel

This repo is Vercel-ready — it's a static site with no build step, configured
by [`vercel.json`](vercel.json).

**Option A — Dashboard (easiest):**
1. Go to https://vercel.com/new
2. Import the `idoagv/pregnancy-calculator` repository
3. Framework Preset: **Other** (auto-detected). Leave Build Command and Output
   Directory empty.
4. Click **Deploy**. Every push to `master` redeploys automatically.

**Option B — CLI:**
```
npx vercel        # preview deployment
npx vercel --prod # production deployment
```

No environment variables or build configuration are required.

## History
Ported from a Flask app (the original date logic lived in `calc.py`). The
server-backed patient-save feature was intentionally dropped to make the app
fully static.
