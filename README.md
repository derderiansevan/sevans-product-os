# PM OS — Claude Code for Product Managers

A free, open-source operating system for Product Managers using Claude Code on Cursor. Set it up once. Claude knows your product, your users, your writing style, and your standards — permanently.

**[→ Full guide and skill reference](https://derderiansevan.github.io/sevans-product-os)**

---

## What's inside

| | |
|--|--|
| **12 Skills** | Slash commands for every core PM workflow |
| **8 Sub-agents** | Expert review personas on demand |
| **Context library** | Your product, users, competitors, and docs — loaded once, used everywhere |
| **Writing style** | Pre-filled PM defaults, fully editable |

---

## Why this exists

Most PMs use Claude like a search engine. They get generic output, spend an hour fixing it, and re-explain their context in the next chat.

PM OS changes the starting point:

| Task | Without PM OS | With PM OS |
|------|--------------|------------|
| **PRD** | Generic doc, made-up metrics, no customer evidence | Hypothesis-driven, evidence-backed, stage-appropriate — in minutes |
| **User stories** | Vague, untestable, no acceptance criteria | INVEST-compliant with Given/When/Then, posted to GitHub if needed |
| **Leadership report** | 30 min from scratch every Friday | 2 min with `/leadership-report` — status, wins, risks, ask |
| **Customer docs** | Wrong terminology, marketing-speak | Matches your UI language, functional, Help Center-ready |
| **Marketing brief** | Feature-first, generic personas | Customer pain first, real competitors named, 3 positioning statements |
| **Customer feedback** | Transcripts skimmed, signals lost | Structured findings with exact quotes, confidence levels, implications |

---

## Prerequisites

- [Cursor](https://cursor.sh) — the AI code editor
- [Claude Code](https://code.claude.com/docs/en/quickstart) — Anthropic's official CLI

No coding required.

---

## Get started in 5 minutes

### 1. Install Claude Code and log in

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Then authenticate:

```bash
claude
```

### 2. Clone the repo

```bash
git clone https://github.com/derderiansevan/sevans-product-os.git
cd sevans-product-os
cursor .
```

### 3. Fill in your context

Open `CLAUDE.md` and fill in every `[FILL IN]` field:

```
Role:         Senior PM at Acme Corp
Product:      B2B SaaS platform for procurement teams
Target users: Legal Ops Managers at mid-market companies
OKRs:         Grow NRR to 115% / Reduce churn to <8%
Terminology:  "workspace" not "project", "member" not "user"
```

Then open `context/writing-style.md` — pre-filled with PM defaults, edit to match your voice. Fill in `context/company.md` and `context/product/knowledge-base.md` for richer output.

### 4. Run your first skill

In Cursor's chat panel:

```
/prd-writer
```

Claude asks 2–3 clarifying questions, then generates a full PRD — hypothesis-driven, stage-appropriate, with a built-in checklist.

### 5. Get expert review

After generating any document:

```
Review this as an Engineer and a Skeptic.
```

Claude adopts each persona and flags specific blockers, risks, and gaps.

---

## Skills

| Skill | Command | What it produces |
|-------|---------|-----------------|
| PRD Writer | `/prd-writer` | Hypothesis-driven PRDs from speclet to solution review |
| User Stories | `/user-stories` | INVEST-compliant stories with acceptance criteria, optional GitHub post |
| Marketing Brief | `/marketing-brief` | Pain-first briefs with personas, positioning, and objection handling |
| Interview Prep | `/interview-prep` | Discussion guides with open-ended questions and a hypothesis to challenge |
| Interview Summary | `/interview-summary` | Structured transcript summary with exact quotes and product implications |
| User Research | `/user-research` | Findings from multiple interviews ranked by evidence strength |
| Competition Analysis | `/competition-analysis` | Evidence-based competitor profiles with copy/avoid/differentiate implications |
| Customer Docs | `/customer-docs` | Help Center articles — functional, direct, no marketing language |
| Leadership Report | `/leadership-report` | Slack updates: status, wins, risks, next steps, ask |
| Roadmap | `/roadmap` | RICE/ICE prioritization and narratives for team, exec, or customers |
| Release Notes | `/release-notes` | Customer-facing or internal changelogs from a PRD or feature list |
| Exec Presentation | `/exec-presentation` | Slide narrative for QBRs, board updates, and roadmap reviews |

---

## Sub-agents

Say `review as [role]` after any output. Claude fully adopts the persona.

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

## Context library

```
context/
├── writing-style.md          ← Voice, tone by audience, banned words — pre-filled, editable
├── company.md                ← Company overview, ICP, OKRs, competitive landscape
├── competitors/
│   ├── _template.md          ← Copy to add a competitor profile
│   └── [competitor].md
├── product/
│   ├── knowledge-base.md     ← Features, terminology, limitations
│   └── prds/                 ← Drop existing PRDs here
└── meetings/
    ├── _template.md          ← General meeting notes
    └── [YYYY-MM-DD-topic].md
```

Reference any file in a prompt with `@context/...`:
```
Write a PRD using @context/company.md and @context/product/knowledge-base.md
```

---

## Customization

**Edit a skill** — Skills live in `.claude/skills/[name]/SKILL.md`. They're plain markdown — open and edit freely.

**Add a skill** — Create `.claude/skills/[name]/SKILL.md` and follow the format of any existing skill.

**Edit a sub-agent** — Personas live in `.claude/rules/sub-agents.md`. Add new ones or adjust the lens of existing ones.

**Change your writing style** — Edit `context/writing-style.md`. Changes apply to every skill automatically.

---

## License

MIT — free forever. Fork it, modify it, share it.

Built by [Sevan Derderian](https://www.linkedin.com/in/sevanderderian/) · [Feedback](https://github.com/derderiansevan/sevans-product-os/issues)
