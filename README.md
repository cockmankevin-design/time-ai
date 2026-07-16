# Time.AI — do less, finish more

A tiny, mobile-first web app that helps college students manage their time by doing **less**, on purpose. Built as an MVP for FGCU social entrepreneurship (Seth Stewart, Kaleb Davis, Brady N, Kevin C).

**Design challenge:** Expose students to better time-management skills, avoid overplanning, and learn to manage college life properly.

## App structure

Time.AI is a real mobile app shell — five screens behind a bottom tab bar, not a scrolling web page:

| Tab | Contains |
|---|---|
| **Home** | Ask Time.AI (coach), Today's Top 3, Today's plan, Focus session |
| **Sleep** | Check-in, night streak, a "why it matters" tip |
| **Progress** | 7-day overview, stats, insight-to-feature mapping |
| **Profile** | Avatar, personal stats, earned badges, team credits |
| **Settings** | Notifications/sound toggles, focus length, data export/reset, feedback, about |

## How each feature maps to our insight statements

| Feature | Insight it answers |
|---|---|
| **Ask Time.AI** — an AI coach that reads a brain-dump of everything on your plate and picks the 3 that matter, plus on-demand tips | *Planning + Inspiration:* "Students plan too many items in a day" / "have a hard time finding inspiration" |
| **Daily Top 3** — the app physically won't accept a 4th task | *Planning:* "Students plan too many items in a day" / "don't know how to properly use a to-do list" |
| **Today's plan** — time-block calendar for one day only, with a live "Now" marker | *Planning:* "Students don't know how to use their calendar efficiently" |
| **Focus session** — 25-minute phone-face-down timer | *Distractions:* "Students have issues relying on technology too much" / "many vices that cause distractions" |
| **Daily quote** — one motivational quote per day on the home screen | *Inspiration:* "Students use the inspirational quotes around campus to find the energy to be great" |
| **Sleep tab** — daily check-in, streak, and a tip card | *Distractions:* "Students struggle with sleeping" |
| **Progress tab** — tasks done, focus sessions, sleep streak, 7-day view | Gives our team real usage numbers for the pilot |
| **Profile & Settings** | Round out the app-shell feel for the demo; badges and stats are wired to real usage data, not fake numbers |

## Why it's a social venture

Poor time management disproportionately hurts first-generation and working students and is a driver of college dropout. A free, dead-simple habit tool = better academic outcomes = measurable social impact (retention).

## Tech

- One `index.html` — vanilla HTML/CSS/JS, no backend, no login, no build step.
- All data stays on the student's device (`localStorage`). Private by default.
- Works on any phone browser via a link.
- **AI assistant:** the MVP coach runs on-device (rule-based prioritization + coaching) so it works offline and never fails during a demo. v2 roadmap: swap the same chat UI to call the Claude API through a small backend for open-ended conversation.
- **Mobile-first, always:** on an actual phone the app fills the screen edge-to-edge. On a laptop/desktop browser (for demoing to judges from a projector), it renders inside a phone-shaped device frame with a notch, so it's unmistakably a phone app rather than a website.

## Running it

Open `index.html` in a browser, or visit the hosted link (GitHub Pages).

## Metrics

**Outputs** (direct results of our activity)
- Students who try Time.AI (pilot target: 20 classmates in week 1)
- Active users: used the app 3+ days in a week
- Total tasks planned and completed (tracked in-app)
- Focus sessions completed (tracked in-app)
- Days scheduled with time blocks; sleep check-ins logged

**Outcomes** (changes in knowledge, behavior, or skills)
- Task completion rate ≥ 70% — students plan 3 realistic tasks instead of overloaded lists
- +2 points (10-pt scale) on "I feel on top of my day" in pre/post survey
- Focus sessions per user per week trending up — phone-free study becomes a habit
- Daily sleep check-in participation — students connect rest to productivity

**Impact** (sustainable change)
- Reduced academic stress and burnout among regular users
- Improved GPA and course completion
- Higher retention and graduation rates, especially for first-generation and working students
- Sleep and planning habits that persist beyond college

## MVP test plan

1. Share the link with ~20 classmates for one week.
2. Feedback via the Google Form linked in the app footer (set `FEEDBACK_URL` in `index.html`).
3. Success metrics: % who use it 3+ days, average tasks completed, and self-reported "felt more in control of my time."
