# How this repository is maintained

This repo is written to by a scheduled task that runs every morning at 06:00 America/Chicago.

## What changes each morning
- `briefs/YYYY/YYYY-MM-DD.md` — a new file. Never edited after the day it covers.
- `threads/*.md` — **rewritten**, not appended. Each file holds the *current* state of a
  live situation. The history lives in the briefs.
- `concepts/NNN-slug.md` — added when an event makes a new concept necessary.
- `concepts/00-INDEX.md` — updated whenever a concept is filed.
- `briefs.json` — a new entry prepended. **The site reads this file, not the directory.**
  A brief that is committed but missing from `briefs.json` will not appear on the calendar or
  the back file. Each entry needs `day`, `date` (YYYY-MM-DD), `weekday`, `display`, `headline`,
  `concept`, `standfirst`.

## What a human writes
`notes/` is yours alone. Nothing automated writes there.

## Commit convention
One commit per morning: `brief: YYYY-MM-DD — <headline>`.
Corrections to an earlier brief are marked inside that day's file, not by rewriting history.

## The site

`index.html` is the front page: the latest brief as the lead, a month calendar of published
editions, then the back file. `brief.html?d=YYYY-MM-DD` renders one edition's markdown with
`md.js` and links to the previous and next. `style.css` carries the whole design.

The calendar is built from `briefs.json` at load time. Dates with an edition are links; the
newest is marked in red; months before the first edition and after the current month are not
reachable.
