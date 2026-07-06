# Pregnancy Calculator

A self-contained, client-side pregnancy calculator. No server, no build step —
a single `index.html` with inline CSS and JavaScript.

**Live:** https://idoagv.github.io/pregnancy-calculator/

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

## Deployment
Hosted on GitHub Pages from the `master` branch root. Any push to `master`
redeploys automatically. Never expires.

## History
Ported from a Flask app (the original date logic lived in `calc.py`). The
server-backed patient-save feature was intentionally dropped to make the app
fully static.
