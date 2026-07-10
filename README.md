# Dog Shelter App

A volunteer shift management tool for a dog rescue shelter in Greece, built to solve a real operational problem I saw firsthand while volunteering there.

[Live demo →](https://ashjstevens.github.io/greek-dog-shelter-ops)

## The problem

The shelter ran on a handwritten daily shift sheet. Feeding times, walk rotations, medication schedules, and which dogs needed extra attention all lived in one person's head or a scrap of paper, redone from scratch each shift. New volunteers had no way to know a dog's harness quirks or medical notes without asking someone in person. Walks weren't tracked, so the same easygoing dogs got walked constantly while nervous or difficult ones got missed. And there was no structured way to flag a dog whose wellbeing was declining.

## My approach

I built a lightweight web app that replaces the shift sheet with something structured, so any volunteer arriving for a shift gets a clear plan rather than relying on memory or word of mouth:

* **Shift plan** – generates a structured plan each shift: cleaning rotation, feeding, walks, and special dog time in the last 30 minutes
* **Dog profiles** – 30+ dogs with feeding schedules, harness notes, walk handling, medications, and RAG wellbeing status (green/amber/red)
* **Walk list** – ordered by longest since last walked, volunteers self-select, each walk attributed to the volunteer who did it
* **Cleaning rotation** – auto-assigns 2 volunteers, avoiding the same person two shifts in a row
* **Special dogs** – weekly assignments of amber/red dogs to volunteers for focused attention
* **Volunteer notes** – quick inline notes on dogs during a shift, without leaving the shift view
* **Shelter map** – clickable enclosure layout showing which dogs are where
* **Rota** – weekly availability grid, tap to toggle
* **AI briefing** – generates a practical shift briefing using the Claude API

Built with HTML, CSS, vanilla JS, and the Claude API (Anthropic). All data stored in localStorage, no backend required, so it was fast to build and easy to hand to volunteers with zero setup.

## What I'd build next

The next phase adds an agent layer on top of the current structure:

* **Proactive alerts** – flags missed medications or dogs not walked in several days, instead of relying on a volunteer to notice
* **Natural language updates** – a volunteer could type "Kermit came out today for the first time" and the agent updates his RAG status and adds a note automatically, rather than filling out a form

This is designed but not yet built. The current version solves the immediate coordination problem; the agent layer is where it would start reducing the mental load on the person running the shelter day to day.
