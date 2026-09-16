# How this repository is maintained

This repo is written to by a scheduled task that runs every morning at 06:00 America/Chicago.

## What changes each morning
- `briefs/YYYY/YYYY-MM-DD.md` — a new file. Never edited after the day it covers.
- `threads/*.md` — **rewritten**, not appended. Each file holds the *current* state of a
  live situation. The history lives in the briefs.
- `concepts/NNN-slug.md` — added when an event makes a new concept necessary.
- `concepts/00-INDEX.md` — updated whenever a concept is filed.

## What a human writes
`notes/` is yours alone. Nothing automated writes there.

## Commit convention
One commit per morning: `brief: YYYY-MM-DD — <headline>`.
Corrections to an earlier brief are marked inside that day's file, not by rewriting history.
