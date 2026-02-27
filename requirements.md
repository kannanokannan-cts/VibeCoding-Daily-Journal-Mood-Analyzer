# Requirements — Daily Journal & Mood Analyzer App

## Source
Derived from: projectbrief.md + Solution Architect design sessions (27 Feb 2026)

---

## Functional Requirements

### FR1 — Journal Entry
- User can write a free-form text journal entry
- Entry is timestamped automatically (date + time)
- User can edit or delete past entries
- Minimum viable entry: text only (emoji and stars optional but encouraged)

### FR2 — Emoji Mood Picker
- User selects one emoji to represent their declared mood
- Emoji set: Happy, Calm, Anxious, Sad, Angry, Energised, Numb, Grateful (minimum 8)
- Selection is visual — large, tappable emoji row
- One selection per entry

### FR3 — Star Rating
- User rates their day 1 to 5 stars
- Visual star selector (not a dropdown)
- One rating per entry

### FR4 — AI Mood Analysis
- On save, Claude analyses the journal text
- Returns: mood label (one word) + human language insight (2-3 sentences)
- Insight tone: thoughtful, warm, honest — not clinical
- Never exposes raw sentiment scores to the user
- Analysis is stored alongside the entry

### FR5 — Divergence Detection
- System compares user-declared mood (emoji + stars) vs AI-detected mood
- If significant divergence detected, surface a gentle observation
- Example: "You picked a happy emoji — but your words suggest you might be carrying more than you're letting on."
- Divergence flag stored per entry (boolean + note)

### FR6 — Entry Storage
- Each entry stores: date, time, text, emoji, star rating, AI mood label, AI insight, divergence flag
- Storage: localStorage (local, private, no backend required)
- Entries persist across sessions

### FR7 — History View
- Calendar view showing one emoji per day at a glance
- Click any day to view full entry + AI insight
- Entries listed in reverse chronological order as fallback

### FR8 — Dashboard / Trends
- Star score trend line over time (last 7 days and last 30 days)
- Emoji frequency breakdown (how often each emoji was used)
- AI mood trend (positive / neutral / negative curve over time)
- All charts minimal and secondary to text insights

### FR9 — Daily Insight (post-save)
- Mood Word of the Day — single human word derived from analysis
- AI insight paragraph shown immediately after saving
- Divergence note (if applicable)

### FR10 — Weekly Digest
- Auto-generated every 7 entries or on demand
- Narrative paragraph: emotional arc of the week
- "Your week in 3 words" — derived from most emotionally significant themes
- Pattern observation: e.g. "You consistently feel worse on Mondays"
- Best moment of the week called out

### FR11 — Trigger Insights
- Words that consistently appear on low-star days
- Words that consistently appear on high-star days
- Expressed as sentences: "Your good days have one thing in common — you got something done."
- Minimum data threshold: 7 entries before trigger insights appear

### FR12 — Monthly Reflection Card
- Generated at end of month or on demand
- Emotional arc summary (paragraph)
- One honest observation
- One strength spotted in the entries
- One gentle nudge forward

---

## Non-Functional Requirements

### NFR1 — Privacy
- All data stored locally — no external database
- No user authentication required (single user app)
- No data sent externally except journal text sent to Claude API for analysis

### NFR2 — Performance
- App loads in under 2 seconds
- AI analysis returns within 5 seconds
- Works on latest Chrome, Firefox, Edge

### NFR3 — Usability
- Mobile-responsive layout
- Accessible: keyboard navigable, sufficient colour contrast
- Entry flow completable in under 2 minutes

### NFR4 — Tone
- Non-judgmental throughout
- No red/green mood indicators
- Language warm, honest, specific — never generic

---

## Out of Scope
- Multi-user support
- Backend server / database
- Native mobile app
- Social sharing
- Therapist/professional integration
