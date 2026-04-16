# Building 52: Ole Miss Women's Basketball
**Built by Kris Smith · Ole Miss WBB · 2026 Offseason**

---

## Overview

An interactive D3.js data visualization tracking the construction of Ole Miss Women's Basketball Team 52 through the 2026 transfer portal. Built around Coach Yolett McPhee-McCuin's philosophy: *"We don't rebuild at Ole Miss...we reload."*

Published to GitHub Pages at `theblacktechie.github.io`

---

## File

`building52.html`: single self-contained file, no dependencies beyond CDN-loaded D3 and Google Fonts.

---

## Structure

Three tabbed sections:

**Tab 1: The Reload**
D3 flow visualization showing three columns: Departed (7 graduates + 2 portal exits), The Core (3 returners), and Incoming (6 portal additions). Animated bezier paths connect departed players to their replacements. Below the flow chart: an animated horizontal bar chart showing each commitment by date.

**Tab 2: Where They Came From**
Player cards for all six portal additions with stats from their previous school, position badge, commit date, and editorial POV. International callout highlighting three Canadian-national players: Howard (Vancouver, BC), Anderson (Toronto, ON), and Okokoh (Montreal, QC).

**Tab 3: Team 52 So Far**
Full current roster with returners and portal additions, live portal window notice, and tally bar (3 returning / 6 incoming / 9 on roster / more coming).

---

## Design System

- **Font:** Inter (Google Fonts)
- **Colors:** Off-white background (#F7F5F2), Ole Miss Red (#CE1126) as accent, Ole Miss Navy (#14213D) for containers and returner indicators, Charcoal (#1C1C1C) for primary text
- **Aesthetic:** Athletic minimalist: The Athletic / Sportico editorial influence
- **Palette rule:** Ole Miss colors are accents only, not dominant fills

---

## D3 Usage

- Flow viz: D3 SVG with animated bezier paths (stroke-dasharray/offset technique), animated node reveals with staggered delays
- Timeline: D3 SVG horizontal bar chart with animated width reveals
- Both charts are fully responsive and redraw on window resize
- Tooltips: custom HTML tooltips with touch support for mobile (touchstart/touchend)

---

## Updating the Roster

When a new player commits before April 20, add them to the `incoming` array in the script block:

```js
{ name: "Player Name", pos: "G", from: "Previous School",
  stats: ["Stat line 1", "Stat line 2"],
  date: "Apr XX", dateObj: new Date('2026-04-XX') }
```

Both the flow viz and the timeline bar chart redraw automatically. No other changes needed.

Also update Tab 3 HTML with a new `.roster-player.incoming` row and increment the tally numbers.

---

## Deployment

Drop `building52.html` into the GitHub Pages repo root. No build step required.

**Suggested filename:** `building52.html`
**Suggested URL:** `theblacktechie.github.io/building52`

---

## Roster Reference (as of April 16, 2026)

| Player | Pos | Status | Previous School | Key Stat |
|---|---|---|---|---|
| Sira Thienou | G | Returning | Ole Miss | 10.5 PPG |
| Desrae Kyles | C | Returning | Ole Miss (via CMU) | Developmental big |
| Lauren Jacobs | G | Returning | Ole Miss | #1 recruit, SC |
| Talaysia Cooper | G | Incoming | Tennessee | 16.0 PPG, ESPN #4 |
| Emily Howard | C | Incoming | Boise State (via Liberty) | 58.3% FG peak |
| Maya Anderson | G/F | Incoming | San Jose State | 13.9 PPG |
| Knisha Godfrey | G | Incoming | Florida (via TCU) | SEC veteran |
| Rachael Okokoh | F/C | Incoming | Penn State | Team Canada U17 |
| Jaida Civil | W | Incoming | Tennessee | 5-star, 6.4 PPG |

Portal window closes **April 20, 2026.**

---

*Built by Kris Smith · Ole Miss Women's Basketball · 2026 Offseason · Team 52*
