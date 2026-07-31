# Systems Radar

An honest map of the revenue and go-to-market systems world, plus the logo library that
illustrates it. Built to close the gap between the tools I have personally run and the full
landscape I am expected to know.

This repo is **public**. Read the scope rules at the bottom before adding anything.

## The map

- **`MAP.md`** — the breadth layer. Every category of tool a revenue/GTM operation can have,
  with a plain description, the trigger for when you actually need one (what breaks without
  it), and the real players. So no whole category blindsides me again.
- **`entries/`** — the depth layer. Ground-truth reads on specific tools and capabilities:
  what they really do against what the marketing says, real cost, where they break.
- **`entries/_TEMPLATE.md`** — the required shape for every entry.
- **`BACKLOG.md`** — the to-research list, kept in priority order.

### How to use it

Point Claude or Codex at this folder and ask across the whole thing, for example:

- "For a usage-based legal-AI company, which categories are non-negotiable and which can wait?"
- "Which AI capabilities actually deliver and which are hype?"
- "What breaks in a company that does not have a metering tool?"

See `AGENTS.md` for the method: how to research a topic into an entry, how to add to the
backlog, and the rules every entry follows. Codex reads `AGENTS.md` automatically. In Claude
Code, run the `school-me` skill, which points at the same instructions.

### Rules for entries

- Ground truth, not vendor copy. If it reads like a website, it is not done.
- Every entry answers: what it really does, what it costs, where it breaks, and the
  two-sentence version I would say out loud if asked cold.
- Real against hype is always marked.

## The logo library

`covers/` holds wide cover images, one per tool. `icons/` holds square icons, one per tool.
Together they are the image host for the Systems & Tools Radar Notion database, and a
general-purpose logo library for decks.

Link to the raw URL:

```
https://raw.githubusercontent.com/sarahcallmesmadds/radar-assets/main/icons/Salesforce.webp
```

Point Claude at a folder path and it can pick the right logo for a deck without you hunting
for one.

### Naming convention

Filenames are the contract. URLs are referenced from Notion and from decks, so **renaming an
existing file breaks live links.** Add new files, do not rename old ones.

1. **TitleCase, underscores between words.** `Google_Drive.png`, `LinkedIn_Sales_Navigator.png`.
   Lowercase brand names that are genuinely lowercase stay as they are: `n8n.png`.
2. **No dots except the extension.** A dot in the name reads as a file extension to some
   tools. Version numbers and dotted brand names use a hyphen: `Opus_4-8.webp`,
   `Otter-ai.jpg`, `Trigger-dev.png`.
3. **No spaces**, ever. They become `%20` in URLs.
4. **Real extension matching real format.** Two files arrived as `.img` and were actually
   AVIF; browsers and Notion will not render a mislabelled file.
5. **One image per tool per folder.** If you have two versions, pick the one that looks
   right at small size and keep the other locally.

## Scope

This repo is public. It holds third-party product logos, and honest research on the tooling
landscape.

**Never in here:** screenshots, personal images, anything showing session or account content,
and the name of any current employer, prospective employer, colleague or customer. An entry
can describe a category or a vendor's product honestly. It cannot say who runs what, or what
is weak about a named company's stack.
