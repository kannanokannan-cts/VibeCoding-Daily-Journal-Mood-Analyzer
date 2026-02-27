# CLAUDE.md — Daily Journal & Mood Analyzer App

## Project Context
This is a hackathon project built during DISRUPT! Claude-A-Thon (27 Feb 2026).
Solution Architect: POD5
Use Case: Daily Journal & Mood Analyzer — expanded beyond the brief.

## Design Principle
> "Numbers tell you what. Language tells you why. We give you both — in words."

Never show raw sentiment scores to the user. Always express mood insights in human language.
AI speaks like a thoughtful, honest friend — not a clinical tool.

## Core Features (LOCKED)
1. Journal entry — free-form text
2. Emoji mood picker — user-declared mood
3. Star rating — 1 to 5 stars for the day
4. AI mood analysis — Claude reads the text, returns mood label + human language insight
5. Divergence detection — compare declared mood (emoji/stars) vs AI-detected mood
6. Entry storage — date, time, text, emoji, stars, AI result
7. Dashboard — mood trends over time
8. Insights — weekly digest, trigger words, monthly reflection card

## Reporting Layer (LOCKED)
- Daily: Mood Word of the Day + human language insight + divergence flag
- Weekly: Narrative digest + "your week in 3 words" + pattern observation
- Monthly: Reflection card — emotional arc, one honest observation, one strength, one nudge
- Triggers: Words that appear on low vs high star days — expressed as sentences not lists

## UI Principles
- Entry screen: calm, minimal, journal first
- Post-save: AI insight shown in conversational language
- History: calendar view with emoji per day
- Insights: paragraph-form, no clinical scores
- Non-judgmental tone throughout
- No red/green mood colour coding

## Tech Decisions
- To be confirmed with developer — see Plan.md
- Data stays local (privacy by default)

## Claude Code Behaviour
- Always load this file at session start
- Always read requirements.md before writing any code
- Always check Plan.md for current phase and done-means before proceeding
- Build incrementally — one feature at a time
- Use Plan Mode for any architectural decision
- Log all significant prompts to prompts.md as you go

## File Structure Expected
```
app/
├── projectbrief.md       # DO NOT MODIFY
├── CLAUDE.md             # This file
├── requirements.md       # Extracted requirements
├── Plan.md               # Phased build plan
├── prompts.md            # Prompt log
├── plugin/               # Plugin config (Mission 6)
├── hooks/                # Hook definitions (Mission 6)
├── skills/               # Skill files (Mission 6)
└── src/                  # Application source code
```

## Constraints
- App must run locally without errors
- Do not modify projectbrief.md
- All Claude features must be evidenced in prompts.md
- Plugins, Hooks and Skills must be documented with purpose and outcome
