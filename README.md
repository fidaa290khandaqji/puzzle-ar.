interactive Math Adventure (Grades 1–4)

A bilingual-ready (AR/EN) web game that builds number sense using visual models, manipulatives, and guided steps. Fast to use, simple to deploy, classroom-friendly.





✨ Features

Grade-aware practice (1 → 4): auto-adjusts difficulty by grade and skill.

Concrete → pictorial → abstract: counters, ten-frames, and equations.

Step-by-step hints: small moves, big wins.

Detailed solutions: show the strategy (counting on/back, number line, decomposition).

Progress & streaks: students see momentum, teachers see mastery.

RTL-first UI: Arabic by default, English toggle supported.

Accessible by design: keyboard, ARIA, and AA contrast.

Deterministic seed mode: lock a seed for live demos or worksheet exports.

🧱 Tech Stack

Runs as plain HTML/JS or React + Vite.

No exotic deps. Keep it simple so it stays maintainable (future-you will say thanks).

🚀 Quick Start
Option A — Plain HTML/JS
git clone https://github.com/<YOUR_ORG>/<REPO_NAME>.git
cd <REPO_NAME>

# Serve locally (any static server works)
python -m http.server 5173
# Visit http://localhost:5173

Option B — React + Vite
git clone https://github.com/<YOUR_ORG>/<REPO_NAME>.git
cd <REPO_NAME>
npm i
npm run dev
# Open the URL shown by Vite (e.g., http://localhost:5173)

# Build & Preview
npm run build
npm run preview


Recommended: Node v18+

📁 Suggested Structure
.
├─ public/                  # static assets (icons, audio)
├─ src/
│  ├─ components/           # UI (Buttons, GradeTabs, CounterRow, etc.)
│  ├─ features/
│  │  ├─ generator/         # question/difficulty engine
│  │  ├─ hints/             # scaffolded steps
│  │  ├─ solution/          # detailed explanation renderers
│  │  └─ scoring/           # streaks, points, mastery logic
│  ├─ i18n/                 # en.json, ar.json
│  ├─ styles/               # global styles + RTL helpers
│  └─ utils/                # RNG with seed, a11y helpers
├─ docs/                    # screenshots, teacher PDF
├─ index.html               # entry (for plain HTML/JS)
└─ vite.config.ts           # if using Vite

🌍 Localization

Default language: Arabic (RTL); English toggle available.

Strings live in src/i18n/en.json and src/i18n/ar.json.

Example:

{
  "title": "Interactive Math Adventure",
  "select_grade": "Select grade",
  "new_question": "New Question",
  "show_solution": "Show Detailed Solution"
}


Minimal RTL helper:

html[dir="rtl"] body { direction: rtl; }
.rtl-flip { transform: scaleX(-1); } /* if you need to mirror icons */

♿ Accessibility

All interactive elements have roles, labels, and visible focus.

Keyboard-first (arrow keys + Enter/Space for counters).

Live feedback uses aria-live="polite".

No color-only signaling; shapes/text back it up.

⚙️ Configuration

Create .env (Vite) to tweak defaults:

VITE_DEFAULT_LANG=ar
VITE_DEFAULT_GRADE=1
VITE_ENABLE_SEED=true
VITE_INITIAL_SEED=20250926

🧪 Tests (optional)
npm run test
npm run test:watch


Focus tests on:

question generator edge cases,

scoring/multipliers,

solution/hint correctness.

🗺️ Roadmap

 Multiplication & division modules

 Teacher dashboard (class codes, CSV export)

 PWA offline mode

 Audio hints / TTS

 More manipulatives (number line, base-ten blocks)

🤝 Contributing

Fork and create a branch: feat/<your-feature>

Keep i18n keys in sync (en.json & ar.json)

Add tests for generator/scoring

Open a PR with screenshots or a short Loom/GIF

📄 License

MIT — see LICENSE.

🙌 Credits

Built with love for learners and teachers.
Product & pedagogy: Fidaa khandagji (SAF Tech)

