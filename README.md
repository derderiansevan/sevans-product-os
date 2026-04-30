# PM OS for Claude Code

A free operating system for Product Managers using Claude Code on Cursor. Seven skills, eight sub-agent personas, and a context system that makes Claude work the way you think.

**[→ See the full guide and skill reference](https://sevanderderian.github.io/cursor-for-pms)**

---

## What's inside

| What | Description |
|------|-------------|
| **7 Skills** | `/prd-writer`, `/user-stories`, `/marketing-brief`, `/user-research`, `/competition-analysis`, `/customer-docs`, `/leadership-report` |
| **8 Sub-agents** | Engineer, Designer, Executive, Skeptic, Customer, Data Analyst, CPO, Marketing Director |
| **Context system** | One `CLAUDE.md` file where you describe your role, product, users, and writing style |

---

## Prerequisites

- [Cursor](https://cursor.sh) — the AI code editor
- [Claude Code](https://claude.ai/code) — Anthropic's CLI (install: `npm install -g @anthropic-ai/claude-code`)

That's it. No coding required.

---

## Get started in 5 minutes

### 1. Clone the repo

```bash
git clone https://github.com/sevanderderian/cursor-for-pms.git
cd cursor-for-pms
```

### 2. Open in Cursor

```bash
cursor .
```

### 3. Fill in your context

Open `CLAUDE.md` and fill in every `[FILL IN]` field:

```md
- Role: Senior PM at [Your Company]
- Product: B2B SaaS platform for [your users]
- Target users: [specific persona, company size, situation]
- Primary metric: [the number you own]
- OKRs: [current cycle objectives]
- Terminology: [what you call things internally]
```

The more specific you are, the better every skill performs. Claude will use this context automatically.

### 4. Run your first skill

In Cursor's chat panel, type:

```
/prd-writer
```

Claude will ask 2-3 clarifying questions, then generate a full PRD — stage-appropriate, hypothesis-driven, with a built-in checklist.

### 5. Review with a sub-agent

After generating any document, add:

```
Review this as an Engineer and a Skeptic.
```

Claude adopts each persona's lens and flags specific gaps, blockers, and risks.

---

## Skills reference

### `/prd-writer`
Writes PRDs from a one-line speclet to a full solution review. Adapts to your stage (Team Kickoff → Planning Review → Solution Review → Launch Readiness). Asks 2-3 clarifying questions first. Includes hypothesis, problem evidence, success metrics with baselines, non-goals, and rollout plan.

### `/user-stories`
Creates INVEST-compliant user stories with Given/When/Then acceptance criteria. Handles a single feature or decomposes a full product brief into a batch. Optionally posts directly to any GitHub repo via the `gh` CLI.

### `/marketing-brief`
Writes structured briefs for your marketing team: problem statement with customer voice, solution explanation, personas, capabilities, competitive positioning, objection handling, and key numbers. Designed for someone who will be selling the feature.

### `/user-research`
Synthesizes interview transcripts or research notes into structured findings. Ranks by evidence strength, includes confidence levels (High/Med/Low), distinguishes what participants *said* vs. *did*, and ends with prioritized product implications.

### `/competition-analysis`
Produces evidence-based competitor profiles: what they built, three smart decisions, three gaps, and a table of implications (copy / avoid / differentiate). Uses real data from product pages, review sites, and job postings — not opinions.

### `/customer-docs`
Writes customer-facing Help Center articles. Functional, direct, no marketing language. Covers feature explanations, step-by-step guides, and limitation callouts. Adapts length to topic complexity (100–600 words).

### `/leadership-report`
Writes structured Slack updates for leadership and stakeholders. Format: status, wins, risks/blockers, next week's focus, asks. Skimmable, specific, and appropriately brief for async reading.

---

## Sub-agents

Say "review as [role]" after generating any document. Claude fully adopts the persona.

| Role | Lens |
|------|------|
| **Engineer** | Feasibility, state model, edge cases, data integrity |
| **Designer** | Flow integrity, error states, cognitive load |
| **Executive** | Strategic fit, business case, resource vs. return |
| **Skeptic** | Assumptions, failure modes, untested hypotheses |
| **Customer** | Value delivery, adoption friction, trust |
| **Data Analyst** | Measurement precision, baselines, instrumentation |
| **CPO** | Problem validity, solution fit, scope discipline |
| **Marketing Director** | Messaging clarity, buyer relevance, competitive positioning |

---

## Customization

**Add your own terminology** — Edit the `Terminology` field in `CLAUDE.md`. Claude will use your product's language everywhere.

**Connect your tools** — Uncomment the MCP connections in `CLAUDE.md` for Notion, Linear/Jira, or Slack. Claude can then pull context from your actual tickets and docs.

**Modify a skill** — Skills live in `.claude/skills/[skill-name]/SKILL.md`. Open any file and edit the instructions, output format, or checklist to match your team's standards.

**Add a skill** — Create a new folder in `.claude/skills/` with a `SKILL.md` file. Follow the format of any existing skill.

---

## License

MIT — free forever. Fork it, modify it, share it.

Built by [Sevan Anderderian](https://www.linkedin.com/in/sevanderderian/) · [Product community](#) · [Feedback](https://github.com/sevanderderian/cursor-for-pms/issues)
