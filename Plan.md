# Plan.md — Phased Build Plan
## Daily Journal & Mood Analyzer App
**Architect:** POD5 | **Date:** 27 Feb 2026

---

## Phase 0 — Environment Setup
**Done means:**
- [ ] Repo cloned locally
- [ ] CLAUDE.md present and loaded in session
- [ ] requirements.md reviewed by developer
- [ ] Tech stack confirmed and documented here
- [ ] Dev server runs without errors

**Stack Decision (to be confirmed):**
- Frontend: React + Vite (recommended) OR plain HTML/CSS/JS
- Styling: Tailwind CSS (recommended) OR plain CSS
- Storage: localStorage
- AI: Claude API (claude-sonnet-4-6) via Anthropic SDK
- Charts: Chart.js or Recharts (lightweight)

---

## Phase 1 — Project Scaffold
**Done means:**
- [ ] Folder structure created as per CLAUDE.md
- [ ] App renders in browser without errors
- [ ] Routing set up (Entry, History, Insights pages)
- [ ] Basic layout shell with navigation

---

## Phase 2 — Journal Entry Feature (FR1, FR2, FR3)
**Done means:**
- [ ] Text area for journal entry renders correctly
- [ ] Emoji picker shows minimum 8 emojis, one selectable at a time
- [ ] Star rating (1-5) is visual and clickable
- [ ] Save button present and wired up
- [ ] Entry saved to localStorage with date/time/text/emoji/stars
- [ ] Form clears after save

---

## Phase 3 — AI Mood Analysis (FR4, FR5)
**Done means:**
- [ ] On save, journal text is sent to Claude API
- [ ] Claude returns mood label + human language insight (2-3 sentences)
- [ ] Response displayed to user in conversational language (no raw scores)
- [ ] Mood Word of the Day displayed
- [ ] Divergence detection logic implemented
- [ ] Divergence note shown if applicable
- [ ] AI result stored in localStorage alongside entry

---

## Phase 4 — History View (FR6, FR7)
**Done means:**
- [ ] History page shows all past entries
- [ ] Calendar view shows emoji per day
- [ ] Clicking a day shows full entry + AI insight
- [ ] Reverse chronological list as fallback

---

## Phase 5 — Dashboard & Trends (FR8)
**Done means:**
- [ ] Star score trend line renders (7-day and 30-day)
- [ ] Emoji frequency breakdown chart renders
- [ ] AI mood trend curve renders (positive/neutral/negative)
- [ ] All charts load without errors
- [ ] Charts are secondary to text — not dominant in layout

---

## Phase 6 — Insights Engine (FR9, FR10, FR11, FR12)
**Done means:**
- [ ] Daily insight shown post-save (Mood Word + paragraph + divergence)
- [ ] Weekly digest generates after 7 entries (narrative + 3 words + pattern)
- [ ] Trigger insights appear after 7 entries (expressed as sentences)
- [ ] Monthly reflection card generates on demand
- [ ] All output in human language — no clinical scores

---

## Phase 7 — Creative Enhancements (Mission 5)
**Ideas (pick 1-2):**
- Mood-based journal prompts ("You seem anxious — try writing about one thing in your control")
- Export monthly reflection card as PDF
- Streak tracker ("You've journaled 7 days in a row")
- Accessibility audit and polish

**Done means:**
- [ ] At least 1 enhancement implemented and working
- [ ] Enhancement documented in prompts.md

---

## Phase 8 — Plugins, Hooks & Skills (Mission 6)
**Done means:**
- [ ] Plugin configured and connected (e.g. sentiment API via MCP)
- [ ] Hook defined and triggers correctly (e.g. auto-lint on file save)
- [ ] Skill created and invokable (e.g. "generate mood analysis test suite")
- [ ] All three documented in prompts.md with purpose and outcome
- [ ] Plugin config file, hook definition file, skill file all present in repo

---

## Phase 9 — Final Validation & Submission
**Done means:**
- [ ] App runs locally without errors
- [ ] All submission checklist files present
- [ ] prompts.md complete with all missions logged
- [ ] Folder named correctly: DailyJournal-[teamname]-[empid1]-[empid2]-[empid3]
- [ ] Pushed to correct GitHub submission URL (based on location)

---

## Submission Checklist
- [ ] projectbrief.md — do not modify
- [ ] CLAUDE.md
- [ ] requirements.md
- [ ] Plan.md
- [ ] prompts.md
- [ ] Plugin configuration file
- [ ] Hook definition file
- [ ] Skill file
- [ ] Project source code
- [ ] App runs locally without errors
