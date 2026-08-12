## Todos

- [x] Calibrate blogging tone #todo
- [x] Define key messages and angle for SAP Community audience #todo
- [x] Find and review LinkedIn post (Claude Code + Obsidian) for possible reference #todo
- [x] Research and document exact setup steps (install + JWD config) #todo
- [x] Research AI writing anti-patterns and writing rules #todo
- [x] Research Obsidian context for uninitiated readers #todo
- [x] Draft all blog sections #todo
- [x] Add placeholder for visuals and pictures #todo
- [x] Replace visual placeholders with actual screenshots and cover image #todo ✅ 2026-08-12
- [x] Change to JWD ego perspective #todo
- [x] Review and refine draft #todo
- [x] Publish to SAP Community #todo ✅ 2026-08-12

---

## Meta

- **Target**: SAP Community Blog
- **Status**: Draft ready for final review
- **Audience**: Joule Work Desktop users, SAP customers and partners, developers curious about MCP
- **Tone**: Personal before technical. Understated humour, not jokes. Hook with honest personal context. No corporate gloss. Short tl;dr up front. Vulnerability as credibility. Self-deprecating about side projects. Technical depth that doesn't gatekeep.
- **Perspective**: Blog is written in JWD's voice (first person = JWD). Mathias is referred to in the third person throughout. This creates a deliberate and slightly playful inversion.
- **Tone reference**: "It's Been a Ride" (Medium, 2021) + "Explore Networks using SAP HANA and Cytoscape" (SAP Community, 2021)
- **GitHub**: https://github.com/mkemeter/obsidian-vaultgate-mcp
- **npm**: https://www.npmjs.com/package/obsidian-vaultgate-mcp

---

## Key Messages

1. VaultGate gives Joule Work Desktop access to your personal Obsidian vault, locally and privately
2. Setup takes about ten minutes; no Obsidian community plugins needed
3. Semantic search lets Joule Work Desktop find relevant notes by meaning, not just keywords
4. Everything stays on your machine: no cloud relay, no data egress
5. Routing through Obsidian's application layer is a deliberate safety choice, not a workaround
6. Obsidian becomes ambient context — not a tool you query on demand, but the ground every conversation starts from
7. The real value: making JWD less stateless; it already knows your context before you say a word

---

## Framing Constraints

- **Author position**: Mathias Kemeter is an SAP employee. VaultGate is his personal open source project, not an official SAP product. Must be made clear early.
- **Tone toward JWD**: Accurate and positive. JWD's HTTP-only MCP support and enterprise guardrails are appropriate design decisions. VaultGate is designed *for* this environment.
- **Framing of other tools**: Other Obsidian MCPs exist and work well for stdio clients. This blog is for the JWD use case. No negative positioning.
- **Unique contribution**: JWD-specific Connector setup is not in the GitHub README. This blog fills that gap.
- **Scope**: Only claim what is true of the current release. No overselling maturity.
- **Obsidian sync**: Notes live on the file system — sync/backup/cloud is the user's choice. OneDrive for Business, iCloud, Dropbox, etc. all work.
- **Vibe-coding angle**: VaultGate is managed almost entirely with Claude Code. Building it was Mathias's deliberate education in AI-augmented development. Self-deprecating "ancient developer" framing fits the tone.
- **Authorship claim**: Mathias did not write one word of content. Content is JWD. Curation, direction, correction is Mathias.
- **Naming**: Blog is written in JWD's first-person voice. "I/me/my" = JWD. "Mathias" = third person throughout. Do not use "Joule" alone — different product.
- **Email + Claude Code**: Claude Code *can* access email in some setups. In enterprise environments, IT governance typically prevents it. Frame as a governance boundary, not a technical impossibility.
- **JWD memory claim**: JWD carries standing instructions (e.g. VAULTGATE.md) — do not say "starts from zero." Say it has no memory of the user's *work* — customers, projects, context.

---

## Writing Rules

### Things to cut
- Scene-setting openers ("In today's world…", "Let's explore…", "It's important to note…")
- Hedges with no informational value ("arguably," "generally," "may help") — replace with scope or cut
- Antithesis used for style, not meaning
- Restatements of the previous sentence
- Summarising final sentences — the last sentence of any section should advance, not recap
- Buzzwords with no observable referent ("seamless," "powerful," "robust," "innovative")

### Things to do
- Open every section with the actual point
- Vary sentence length: short for emphasis, longer for mechanism and context
- One paragraph = one job
- Use specifics: names, numbers, constraints, failure modes
- End paragraphs with implication, not recap
- Let some sentences end hard

### Structure principles
- Intro: max two short paragraphs — name the problem, promise the outcome, get out
- Sections: descriptive headings
- Within each section: 2–5 short paragraphs or a focused bullet list, not both
- Setup: numbered steps, one action per step
- Closing: concrete next action, not a summary

---

## Revised Blog Structure

1. **Opening line** (JWD introduces itself)
2. **Introduction** (~130 words)
3. **A note on Obsidian** (~150 words)
4. **The idea: giving me a memory** (~150 words)
5. **What you can do with it** (~200 words + sample prompts)
6. **VaultGate in brief** (~100 words)
7. **Set it up: 6 steps** (~150 words)
8. **How this blog was written** (~200 words)

---

## Knowledge Base

### Obsidian Facts (from Perplexity research)

- Note-taking app storing everything as local, plain Markdown files; no proprietary database
- Sync is the user's choice: notes are on the file system, so OneDrive, iCloud, Dropbox, etc. all work
- ~1.5 million monthly active users (third-party estimate; Obsidian does not publish official numbers)
- ~22% year-over-year growth
- 2,749 community plugins (April 2026)
- Growth entirely through word of mouth; no paid marketing
- Built by ~3 engineers; no analytics collection
- AI advantage: Markdown natively readable/writable by LLMs without API or export; local files = no vendor lock-in
- Obsidian did not add an AI feature to become AI-ready — it already was, by design

### JWD Context (from User Guide)

- JWD is SAP's AI-powered desktop assistant: chat interface enriched with local file access, web search, Outlook email/calendar, MCP Connectors, and Skills
- Available on Windows 11 (64-bit) and macOS 13 Ventura+ (Apple Silicon only)
- MCP integrations are called **Connectors** in JWD — via Extensions nav or input field → Settings → Select Connector → Manage Connectors
- JWD user guide: https://help.sap.com/docs/JOULE_WORK_DESKTOP/3fec5cf19c7040baa71e42a88099180e

### LinkedIn Post (VaultGate Announcement)

URL: https://www.linkedin.com/feed/update/urn:li:activity:7493232678100631552/

Key phrases:
- "The only thing missing in the beginning" — the hook
- "JWD has gotten one of my favorite local assistants" — credibility, not marketing
- "a local server that makes Obsidian's CLI functions accessible via MCP" — use verbatim
- "Using Obsidian and Joule Work Desktop?" — the target reader, stated exactly

### Central Theme

**Making JWD less stateless.** Obsidian acts as persistent ground for every conversation — context that flows in even on topics never explicitly raised. Without VaultGate, JWD is capable but memoryless. With it, every conversation starts from where you already are.

### Origin Story

- Mathias is not a developer anymore. Tried Claude Code out of curiosity.
- Connected it to Obsidian: "perfect power couple" for daily work.
- Entered the JWD beta. Wanted JWD to take the same role.
- JWD is more gated by design — enterprise software, no direct file access appropriate.
- No existing Obsidian MCP worked for HTTP + no-plugins + local-only.
- Mathias built VaultGate using Claude Code. The tool that created the need also built the replacement.
- Building it was a deliberate education in vibe-coding and AI-augmented development — "ancient developer" learning curve.
- First fully AI-augmented project: Claude Code handles GitHub, CI, bug reports end to end.

### Feature Evolution

**Day one**: read, write, search (full-text + semantic).
**Added**: Mac DMG + tray app (background operation); Obsidian URI (open notes mid-conversation).

### Usage Scenarios

- **Email synthesis**: JWD reads Outlook; synthesize emails on a topic/customer, write result into Obsidian note. JWD-specific killer use case.
- **Meeting prep**: pull customer or project notes before a call
- **1:1 prep**: surface colleague notes, action items
- **Knowledge retrieval**: past decisions, project context, meeting outcomes
- **Note capture**: dictate a summary, JWD writes it to the vault

### Setup Reference

1. **Install JWD** — installer from your organisation, sign in via SSO
2. **Install Obsidian** — macOS 13+ (Apple Silicon) or Windows 11
3. **Enable Obsidian CLI** — Settings → General → Command Line Interface → Register CLI
4. **Install VaultGate** — DMG on Mac (includes tray app), or `npm install -g obsidian-vaultgate-mcp`
5. **Add as Connector in JWD** — copy MCP URL from tray app; JWD: input field → Settings → Select Connector → Manage Connectors → add
6. **Add standing instructions** (recommended) — VAULTGATE.md in vault root or point to existing Claude.md

### Resources

- GitHub: https://github.com/mkemeter/obsidian-vaultgate-mcp
- npm: https://www.npmjs.com/package/obsidian-vaultgate-mcp
- JWD user guide: https://help.sap.com/docs/JOULE_WORK_DESKTOP/3fec5cf19c7040baa71e42a88099180e
- LinkedIn announcement: https://www.linkedin.com/feed/update/urn:li:activity:7493232678100631552/

---

## Blog Draft

> [!example] 📷 VISUAL — Cover image
> **Type**: Screenshot or composed image
> **Content**: JWD conversation window open on one side, Obsidian vault open on the other — showing both tools active together. Ideally a real screenshot from your own setup rather than a stock image. The VaultGate tray icon visible in the Mac menu bar would be a nice detail.
> **Alt text**: "Joule Work Desktop and Obsidian open side by side, connected via VaultGate"

![[cover.png]]

Hi, I am Joule Work Desktop, and I am going to show you how to use VaultGate to contextualize my answers with your own thoughts. 👋

---

### Introduction

Mathias is not a developer anymore. That stopped being his job at some point, and he made peace with it. But he kept the habit of trying things in his spare time, which is why he ended up running Claude Code one night out of curiosity. Within a few minutes it was connected to his Obsidian vault, and that combination quickly turned into something he used every day.

When Mathias joined my restricted beta, he wanted the same thing from me. For most things, I was already delivering. One thing was missing: a way for me to read and write his Obsidian notes. So he built one.

VaultGate is also how Mathias educated himself on vibe-coding and AI-augmented development. The project runs almost entirely on Claude Code — GitHub, CI, bug reports, the whole thing. For an ancient developer who had long since stopped writing production code, quite the learning curve.

VaultGate is a local MCP server that connects me to your Obsidian vault. Personal project, open source, not an SAP product. Setup takes less than ten minutes.

---

### A note on Obsidian

Obsidian is a note-taking application that stores everything as plain Markdown files on your device. No proprietary database, no vendor account required. Your notes are files on your file system — how you sync them or back them up is entirely your call. Mathias's vault lives on OneDrive for Business, which is both convenient and compliant.

That was already the reason Mathias chose Obsidian before any of this AI story. Open format, no lock-in, nobody owns his notes except him.

The AI era made it more relevant still. Markdown is what LLMs handle best. An AI can read, parse, search, summarize, and write your notes without a conversion layer, an API, or an export step. Most other note-taking tools require at least one of those. Obsidian did not add an AI feature to become AI-ready. It already was, by design.

An estimated 1.5 million monthly active users, no paid marketing, a team of a few engineers, no analytics collected. If they ever went public, the AI tailwind alone would make Mathias buy the shares.

> [!example] 📷 VISUAL — Obsidian interface
> **Type**: Screenshot
> **Content**: Obsidian editor view showing a vault. 
> **Alt text**: "Obsidian vault with interconnected notes displayed in editor view"

![[obsidian-vault-editor.png]]

---

### The idea: giving me a memory

I am a capable assistant. I can search the web, read your emails, access your calendar, and run tasks. What I do not have is memory of your work. Every conversation begins without knowing your customers, your projects, or what you were working on.

Mathias's Obsidian vault is the opposite of that. It contains meeting notes, customer context, project decisions, and open tasks: things he would otherwise have to reconstruct from scratch every time. When he connected it to Claude Code, the AI stopped working in a vacuum. It was working from the same context Mathias was.

VaultGate does the same for me. Your vault is not a database you query when you remember to. It is context that is present in every conversation, including ones where you never explicitly mention it. Before you type your first message, I already know who you are working with and what is on your plate.

In an enterprise context, this matters more than it looks. Direct file access to sensitive notes carries risk. VaultGate routes everything through Obsidian's application layer rather than the file system. That fits my use of HTTP for Connectors rather than stdio.

> [!example] 📷 VISUAL — Architecture diagram
> **Type**: Simple diagram (can be drawn in Obsidian Canvas, Excalidraw, or any diagramming tool)
> **Content**: Flow showing JWD → VaultGate Connector (HTTP) → VaultGate local server → Obsidian application layer → Vault files on disk → OneDrive sync (optional). Emphasises local-only data path and application layer routing.
> **Alt text**: "Architecture diagram showing JWD connecting to Obsidian via VaultGate over local HTTP"

![[vaultgate diagram.png]]

---

### What you can do with it

I already have access to your Outlook inbox. That is the combination that makes VaultGate interesting.

Ask me to go through recent emails on a customer or project, summarize what has changed, and write the result directly into the relevant Obsidian note. You get an updated note without opening a single email. In principle, a local code assistant can do this too. In practice, enterprise IT governance typically blocks direct access to corporate mail. I come in through the Outlook Connector — a sanctioned path.

Before a customer call, ask me what you have on them. I search your vault and surface the relevant notes. If you want to check something in detail, tell me to open the note in Obsidian. The same pattern works for 1:1 meetings: who did you last talk to, what was unresolved, what did you promise.

If you take notes in Obsidian after meetings, I can write them. Dictate a summary and it lands in the right place, with the right structure, without touching the keyboard.

Here is what Mathias actually says to me:

> *"Go through my recent emails about Acme Corp and update their note with a summary of what has changed."*
>
> *"I have a call with Acme in 20 minutes. What do I have on them?"*
>
> *"What were the open items from my last 1:1 with Sarah?"*
>
> *"What did we decide on the EMEA pricing model?"*
>
> *"Write a meeting note to the Q3 Planning project: we pushed the deadline to September, Anna follows up with procurement."*
>
> *"Open the Acme Corp note in Obsidian."*

Your vault acts as working memory. You stop reconstructing context at the start of every session.

> [!example] 📷 VISUAL — JWD in action
> **Type**: Screenshot
> **Content**: A JWD conversation showing a real interaction with the vault — e.g. JWD surfacing a note in response to a question, or writing a summary back to Obsidian after reading emails. This is the "show don't tell" moment for the use cases described above.
> **Alt text**: "JWD conversation retrieving context from an Obsidian note via VaultGate"

![[jwd-vault-conversation.png]]

---

### VaultGate in brief

VaultGate is a local server that makes Obsidian's CLI functions accessible via MCP. It runs on your machine, binds to localhost, and never sends note content anywhere.

Key properties:
- **HTTP transport**: works with my Connector model; no stdio required
- **Application layer**: reads and writes through Obsidian, not the file system
- **Semantic search**: local embeddings via @xenova/transformers; no network calls
- **Mac tray app**: runs in the background; copy the MCP URL from the menu bar

It also supports full-text search, task management, applying templates, and opening notes in Obsidian mid-conversation.

GitHub: https://github.com/mkemeter/obsidian-vaultgate-mcp

---

### Set it up in 6 steps

Assumes you already have me installed and configured. If not, start with the JWD setup and user guide: https://help.sap.com/docs/JOULE_WORK_DESKTOP

1. **Install Obsidian** if you have not already. macOS 13 Ventura or later (Apple Silicon); Windows 11.
2. **Enable the Obsidian CLI**: Settings → General → Command Line Interface → Register CLI.

> [!example] 📷 VISUAL — Obsidian CLI setting
> **Type**: Screenshot
> **Content**: Obsidian Settings > General > Command Line Interface, showing the Register CLI toggle or button. Removes ambiguity for readers following the steps.
> **Alt text**: "Obsidian settings screen showing the Command Line Interface option"

![[obsidian-cli-setting.png]]

3. **Install VaultGate**: download the DMG for Mac (includes the tray app), or run `npm install -g obsidian-vaultgate-mcp`.
4. **Start VaultGate**: open the tray app from the Mac menu bar. Copy the MCP URL it shows.

> [!example] 📷 VISUAL — VaultGate tray app
> **Type**: Screenshot
> **Content**: Mac menu bar with VaultGate tray icon open, showing the MCP URL. This is the one piece of the setup that has no equivalent in text — readers need to see what they are looking for.
> **Alt text**: "VaultGate tray app in the Mac menu bar showing the local MCP server URL"

![[vaultgate-tray-app.png]]

5. **Add VaultGate as one of my Connectors**: in the conversation input field, click the Settings icon → Select Connector → Manage Connectors → add the URL from step 4.

> [!example] 📷 VISUAL — JWD Connector setup
> **Type**: Screenshot
> **Content**: JWD Manage Connectors screen with VaultGate added and active. Ideally shows the URL field and the connected state.
> **Alt text**: "JWD Manage Connectors screen with VaultGate connector configured"

![[jwd-connector-setup.png]]

6. **Add standing instructions** (recommended): create a `VAULTGATE.md` file in your vault root. Describe your folder structure, naming conventions, and anything you want me to know about how you work. You can also ask JWD to generate this file or point VaultGate at an existing `CLAUDE.md` if you already have one.

Step 6 is the one that makes the difference between a search tool and a context layer. Without it, I can read your notes. With it, I understand them.

---

### How this blog was written

I wrote this post entirely. Mathias provided the guidance — questions, corrections, direction — but did not write one word of content.

1. **Writing rules first.** Before any section was drafted, explicit writing rules and tone guidelines were defined in the project note to counteract the patterns that make AI-generated text unpleasant to read.
2. **Context assembly via Connectors.** Three Connectors provided the factual foundation: the VaultGate GitHub repository (I read the source directly; no description of the project was provided), the JWD user guide as a PDF attachment, and a Perplexity Connector for external research on Obsidian, AI writing patterns, and SAP Community tone.
3. **Knowledge extraction via Q&A.** Origin story, usage scenarios, framing constraints, and setup details were gathered through an interview-style Q&A with Mathias.
4. **Iterative drafting.** Sections were written one at a time, reviewed, and corrected across multiple sessions.
5. **Session continuity via VaultGate.** After each session, I wrote all outputs back to a living project note in Obsidian via VaultGate. At the start of the next session, that note provided full project context through the VaultGate Connector, combined with `VAULTGATE.md` standing instructions. No context was re-established manually between sessions.

Content: mine. Direction: Mathias. His original prose: none.

---

### Full Disclosure

Hi, I am Mathias, and I supported Joule Work Desktop in writing this blog. 👋

I haven't been writing on the SAP Community Pages for quite a while and I don't want to miss the opportunity to add a few personal words. The creation of this blog has been quite exemplary for my JWD + Obsidian usage pattern. Obsidian does not act as pure notebook anymore, but it really became a persistent (shared) memory across my various AI assistants (...don't let JWD know about the others 🤫). To give you some more insight on how the backstage in Obsidian looks like, I am going to share the raw project note that has been used for creating this blog.

Quite honestly, sharing a note from my personal vault on Github feels like dropping my pants in public. Just the right move after publishing my first blog after 4 years of absence on this platform. 🫡

![[Pasted image 20260812174711.png]]

---

## Blog Creation Process Log

- **JWD + Perplexity Connector**: researched VaultGate GitHub presence; found SAP Community posts for tone calibration
- **JWD + VaultGate Connector**: created this note as living knowledge base; updated after every interview exchange
- **Interview-style Q&A in JWD**: gathered origin story, feature evolution, usage scenarios, framing constraints
- **JWD file attachment**: author attached JWD user guide PDF; JWD extracted Connector setup steps and terminology directly from the document
- **Author shared LinkedIn announcement post**: captured as tone anchor and hook source
- **JWD + Perplexity Connector**: researched AI writing anti-patterns and SAP Community blog best practices; writing rules and revised structure added to knowledge base
- **JWD + Perplexity Connector**: researched Obsidian user stats, growth, and AI-native advantages; facts added to knowledge base and woven into "A note on Obsidian" section
- **Author review**: corrected Obsidian section — removed "limitation" framing, reframed sync as user choice (OneDrive for Business example), connected share line to AI tailwind specifically
- **Author review**: added vibe-coding / AI-augmented development angle to introduction; "ancient developer" framing captured in knowledge base
- **Author review**: rewrote "How this blog was written" — factual numbered protocol, VaultGate session continuity step prominent, explicit authorship claim; fixed "Joule" → "JWD" throughout entire draft
- **Author review**: added two new todos — visuals/pictures placeholders and JWD ego perspective pass
- **Visual placeholders added**: cover image, Obsidian UI, architecture diagram, JWD in action, CLI setting, VaultGate tray app, JWD Connector screen — 7 visuals total
- **Author review**: added todo to replace visual placeholders with actual screenshots
- **Perspective pass**: full draft rewritten in JWD's first-person voice; Mathias referred to in third person throughout; opening line added
- **Review pass**: applied fixes including "behind my use of HTTP" phrasing correction
- **Sample prompts added**: 6 example prompts added to "What you can do with it" section, introduced in JWD's voice

---

## Review Notes
