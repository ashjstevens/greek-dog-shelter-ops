# Dog Shelter App

A volunteer shift management tool built for a dog rescue shelter in Greece, based on a real operational problem I spotted while volunteering there.

**[Live demo →](https://ashjstevens.github.io/greek-dog-shelter-ops)**

## What it does

Replaces the handwritten daily shift sheet with a structured, AI-assisted tool:

- **Shift plan** — generates a structured plan each shift: cleaning rotation, feeding, walks, and special dog time in the last 30 mins
- **Dog profiles** — 30+ dogs with feeding schedules, harness notes, walk handling, medications, and RAG wellbeing status (green/amber/red)
- **Walk list** — ordered by longest since last walked, volunteers self-select, each walk attributed to the volunteer who did it
- **Cleaning rotation** — auto-assigns 2 volunteers, avoiding the same person two shifts in a row
- **Special dogs** — weekly assignments of amber/red dogs to volunteers for focused attention
- **Volunteer notes** — quick inline notes on dogs during a shift, without leaving the shift view
- **Shelter map** — clickable enclosure layout showing which dogs are where
- **Rota** — weekly availability grid, tap to toggle
- **AI briefing** — generates a practical shift briefing using the Claude API

## Built with

HTML · CSS · Vanilla JS · Claude API (Anthropic)

All data stored in localStorage. No backend required.

## Agentic extension (designed, not yet built)

The next phase would add an agent layer: proactive alerts for missed medications or dogs not walked in several days, and natural language updates to dog profiles ("Kermit came out today for the first time" updates his RAG status and adds a note automatically).
