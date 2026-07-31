---
name: school-me
description: School me on a revenue/GTM tool or capability by researching it into a ground-truth entry for this systems-landscape knowledge base. Trigger on "/school-me", "school me on <tool>", "research <tool> for the landscape", or "school me on the next backlog item". Does honest web research, writes the entry using entries/_TEMPLATE.md, updates BACKLOG.md, and commits. Also handles quick-capture ("add <tool> to the backlog").
---

# school-me

Turns a topic into a finished, honest entry in this knowledge base. The full method and rules live in `AGENTS.md` at the repo root; this skill is the Claude Code door to it. Read `AGENTS.md` and `entries/_TEMPLATE.md` before starting.

## Pick the topic
- If the user named a topic, use it.
- If they said "next" or gave nothing, take the top unchecked item under `## To research` in `BACKLOG.md`.
- If they just want to capture ("add X to the backlog"), add one line under `## To research` in `BACKLOG.md`, at the end of its own priority block (high, then med, then low), and STOP. Do not research.

## Research (honest sourcing)
Do real web research. Prioritize practitioners, independent analysts, and press over vendor pages. Use the vendor's own site only for baseline facts (what modules exist), never for claims about how well it works. Answer, for the tool: what it really is, what it genuinely does well, where it breaks, what it really costs, adoption reality (hype vs real), how it compares to alternatives, and the data/trust posture. Capture specific numbers, dates, and source URLs to cite.

## Write the entry
Fill in EVERY section of `entries/_TEMPLATE.md`. Save to `entries/<short-slug>.md`. Keep it plain-English, mark real vs hype, label estimates and motivated sources honestly, no em dashes, and end with the two or three sharp questions to ask in the room.

## Close out
1. In `BACKLOG.md`, move the topic to `## Done` with a link to the new entry file.
2. Commit: `git add -A && git commit -m "Add depth entry: <topic>"`. Push if a remote is set.
3. Show the finished entry inline so Sarah can react.

## Bar
If a section reads like marketing, it isn't done. The whole value is candor.
