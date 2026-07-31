# Backlog: topics to research

Add a topic here whenever one occurs to you. One line each, filed at the end of its own priority block (high, then med, then low) so the top unchecked item is always the one most worth doing. The research skill pulls from the top of this list, or you can point it at a specific topic.

Format: `- [ ] Topic name — optional why / angle — priority (high/med/low)`

## To research
- [ ] Enterprise Salesforce (Unlimited edition) — the tier I've never run; what it includes vs the tiers I know, and which limits matter for the systems I run: how many requests other systems may send it per day, how many custom objects, how many test environments, how many automations — high
- [ ] Data Cloud — Agentforce keeps leaning on it; what it really is and does — high
- [ ] Harnesses — the software wrapped around the model that runs its tools, enforces what it may touch, and manages what it remembers; what counts as one, and why people say the harness matters as much as the model — high
- [ ] Skill pack vs plugin — when to bundle skills as a plugin vs just share a folder of skill files, and what the plugin format adds on top — high
- [ ] GitHub setup for the Claude marketplace — one listing file that points at many plugins, vs a repo that is just the plugin itself; whether the repo has to be public; and how an update reaches people who already installed it — high
- [ ] Rollback for skills — how a skill should undo itself: save a copy before changing anything, ship a dedicated off switch, and be safe to run twice by accident. Whether my own skills clear that bar, and whether it belongs in a review checklist — high
- [ ] Data dictionaries and catalogs — the discipline behind writing down what every field means. A dictionary defines the fields; a catalog is the searchable index across all of them. What a good entry holds, who keeps it current, and the standard tools (dbt docs, Atlan, Alation, or plain Notion). I keep rough versions of this already; this is the formal version — high
- [ ] Nue (deep-dive) — the CPQ + billing tool that shows up alongside usage-based billing stacks; what it really does end to end — med
- [ ] Clay — AI enrichment; real vs hype for outbound — med
- [ ] Salesforce certificates — what a certificate does (proves one system's identity to another, like an ID badge they check before trusting each other), where they show up, when they expire and what breaks when they do — med
- [ ] Plugin package anatomy — what is actually inside one: a settings file describing it, the skills themselves, hooks (small scripts that fire automatically at set moments, like every time a file is saved), and commands (the slash shortcuts you type). How it gets bundled into a single file, how versions are tracked, and how that differs between installing it yourself, installing from a marketplace, and an admin pushing it to a whole company — med
- [ ] Skills for Codex vs Claude Code — whether one skill file can serve both, what breaks, and whether anyone has a credible pattern for it. Decision to make: write once for both, or Claude first with notes for Codex — med
- [ ] Skill and plugin moderation — what review exists in Claude's own marketplace, and what a company can enforce internally — med
- [ ] Anthropic's team and enterprise roadmap — shared spaces, switching between workspaces, sharing skills, skills that call other skills, and usage reporting. Which of these would replace something I would otherwise build myself — med
- [ ] Speakeasy and Gram — a control plane is the layer a company puts in front of every AI tool its staff use, so it can see and govern all of it in one place. What one actually records (cost, time taken, who ran what, whether it worked), what it does not (the lessons-learned notes especially), and how the two products differ — med
- [ ] Gong vs the AI-note-taker wave — is conversation intelligence still worth it — low
- [ ] Symlinks — a file that is only a pointer at another file, like a desktop shortcut. When to use one instead of a real copy, how git handles them (it saves the pointer, not the contents), and what breaks if the original moves — low
- [ ] Locally hosting models — running the model on your own machine instead of calling someone else's service over the internet (an API, the hosted version you pay per use), like cooking at home instead of ordering in. What hardware it takes, what tools people use, how much quality you give up against the big hosted models, and when it is a real answer — low

## Done (moved to entries/)
- [x] Agentforce — entries/agentforce.md
- [x] Metering: Metronome vs Orb — entries/metering-metronome-vs-orb.md
