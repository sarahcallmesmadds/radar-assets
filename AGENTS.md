# AGENTS.md — how to work in this repo

This is Sarah's personal knowledge base on the revenue and go-to-market systems world. It exists to keep her sharp on tools, systems, and AI in her field, and to be queried with an AI assistant. This file is the shared brain: it works for Codex (which reads AGENTS.md automatically), for Claude Code (via the `school-me` skill, which points here), and for a human.

**This repo is public.** Everything written here is readable by anyone, including the companies it discusses. See "What never goes in here" below before writing an entry.

## What's here
- `MAP.md` — the breadth layer. Every category of revenue/GTM tool, with a plain description, the TRIGGER (when you actually need one / what breaks without it), and the real players.
- `entries/` — the depth layer. Honest, ground-truth reads on specific tools (what they really do vs marketing, real cost, where they break).
- `entries/_TEMPLATE.md` — the required shape for every entry.
- `BACKLOG.md` — the to-research checklist, kept in priority order.
- `covers/` and `icons/` — the logo library, one image per tool. Filenames are a contract: they are referenced by raw URL from Notion and from decks, so never rename an existing file. See the README.

## What never goes in here
The name of any current employer, prospective employer, colleague or customer. An entry may describe a category or a vendor's product honestly. It may not say who runs what, or what is weak about a named company's stack. That reads as research on a target rather than knowledge of a market, and the target can read it.

Also never: screenshots, personal images, and anything showing session or account content.

## Task: add a topic to research later
Add one line under `## To research` in `BACKLOG.md`, at the end of its own priority block (high first, then med, then low):
`- [ ] Topic name — optional why/angle — priority (high/med/low)`
The list stays sorted because the research task takes the top unchecked item, so the top one has to be the one most worth doing. Appending to the end of the whole list would hand the next session the oldest capture instead. That's the whole task. No research, just capture.

## Task: research a topic into an entry
This is the main workflow. Given a topic (either named directly, or the top unchecked item in `BACKLOG.md`):
1. **Research honestly.** Do real web research. Prioritize practitioners, independent analysts, and press over vendor pages. The vendor's own site is fine only for baseline facts, never for claims about how well something works.
2. **Write the entry** by filling in every section of `entries/_TEMPLATE.md`. Save it to `entries/<short-slug>.md`.
3. **Follow the rules** (below).
4. **Update the backlog:** move the topic to the `## Done` section with a link to the new entry.
5. **Commit** with a short message describing the entry added.

## Task: read / query the data
Reading and answering is native to any AI assistant here. Point it at this folder and ask. Good questions to start with:
- "For a [type of company], which categories on the map are non-negotiable and which can wait?"
- "Across the entries, which AI capabilities actually deliver and which are mostly hype?"
- "What breaks in a company that doesn't have a [category] tool?"
- "Summarize the [tool] entry as the two sentences I'd say if asked cold."
Start from `MAP.md` for breadth, then `entries/` for depth.

## The rules (non-negotiable)
- **Ground truth, not vendor copy.** If a section reads like a marketing page, it isn't done.
- **Mark real vs hype** on everything.
- **Label estimates as estimates** and motivated sources (e.g. a competitor's survey) as motivated.
- **Plain English.** No jargon without a short inline definition. Sarah is non-technical.
- **No em dashes** in anything written for Sarah. Use commas, periods, or parentheses. One exception: the `- [ ] topic — why — priority` line format in `BACKLOG.md`, where the dash separates fields rather than punctuating a sentence.
- Every entry ends with the two or three sharp questions to ask in the room when someone says "let's just turn this on."
