# Verified research run

Runs research and comparisons where every fact is sourced, dated and confidence-tagged, and nothing counts until a separate skeptical pass has checked it against the live primary page.

**Type:** Claude Code skill · **Area:** General skills

## What it does

- Frames the question, the decision it feeds, the hard gates and the comparison criteria before searching.
- Finder agents (a cheaper model is fine) search independent slices across at least two source families, with a positive control for any "nothing exists".
- A separate verifier fetches each candidate's live page, confirms it is current and meets the gates, and drops what fails, with reasons.
- Outputs the answer first, then the comparison table, the drop list, unverified leads, and what the run did and didn't prove.

## Guardrails

- Prices, fees and eligibility come from the issuing body's own page, checked this run.
- Read-only: no sign-ups, installs, purchases or contact. Personal details stay out of search queries.

## When it triggers

> Run a research or comparison task where every fact is sourced, dated and confidence-tagged - finder agents propose, a separate skeptical pass checks each item against its live primary page and drops what fails, and any "nothing exists" claim needs a positive control. Use for comparisons (banks, SIM plans, phones, hotels, tools, libraries, GitHub projects), "is there something that already does X", testing the assumption a plan rests on, or any research where a wrong fact would cost money or time.

## What's in this repo

- `SKILL.md`: the skill itself, the file Claude or Codex reads.
- Written to be generic: where the skill relies on the user's own files, it names them by role, not by content.

## Install

```bash
mkdir -p ~/.claude/skills/verified-research-run
curl -fsSL https://raw.githubusercontent.com/adiyt4soni/verified-research-run/main/SKILL.md -o ~/.claude/skills/verified-research-run/SKILL.md
```
