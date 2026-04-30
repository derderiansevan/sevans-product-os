# PM Context

> Fill in everything marked [FILL IN]. The more specific you are, the better Claude performs.
> Delete this line when done.

- **Role:** [FILL IN — e.g., Senior Product Manager, Group PM, Head of Product]
- **Company:** [FILL IN — e.g., Acme Corp]
- **Product:** [FILL IN — e.g., B2B SaaS platform for procurement teams]
- **Target users:** [FILL IN — e.g., Legal Ops Managers and Procurement Directors at mid-market companies (200-2,000 employees)]
- **Current focus:** [FILL IN — e.g., reducing time-to-value for new customers, Q2 activation initiative]
- **Primary metric:** [FILL IN — e.g., 30-day activation rate, NRR, ARR]
- **Guardrails:** [FILL IN — e.g., no changes that increase churn risk for enterprise tier, must work on mobile]
- **OKRs:** [FILL IN — e.g., O1: Grow NRR to 115% / KR1: Reduce churn to <8% / KR2: Improve activation to 65%]
- **Terminology:** [FILL IN — e.g., we call it "workspace" not "project", "member" not "user", "plan" not "subscription"]

---

## Writing Rules

- Direct, concise, active voice. No filler.
- Lead with the recommendation, then context.
- Audience-match: casual for Slack, structured for docs, precise for specs.
- Banned words: delve, landscape, synergy, leverage, robust, streamline, cutting-edge, seamless, powerful, intuitive.
- Never fabricate data, quotes, or metrics. Use `[NEED: data from X]` for gaps.

---

## Sub-Agent Roles

When I say "review as [role]," fully adopt that perspective.
Personas defined in `.claude/rules/sub-agents.md`.

Available roles: **Engineer** · **Designer** · **Executive** · **Skeptic** · **Customer** · **Data Analyst** · **CPO** · **Marketing Director**

Example: "Review this PRD as an Engineer and a Skeptic."

---

## Skills

Trigger any skill by typing `/skill-name` in Claude Code.

| Skill | Command | What it does |
|-------|---------|--------------|
| PRD Writer | `/prd-writer` | Write PRDs from speclet to full solution review |
| User Stories | `/user-stories` | Create well-scoped user stories, optionally post to GitHub |
| Marketing Brief | `/marketing-brief` | Write structured briefs for features and products |
| Interview Prep | `/interview-prep` | Write a discussion guide and research questions before a user interview |
| Interview Summary | `/interview-summary` | Summarize a single interview transcript into a structured, quotable summary |
| User Research | `/user-research` | Synthesize multiple interviews into ranked findings with confidence levels |
| Competition Analysis | `/competition-analysis` | Analyze competitors with evidence-based product intelligence |
| Customer Docs | `/customer-docs` | Write customer-facing documentation for your Help Center |
| Leadership Report | `/leadership-report` | Write Slack updates for leadership and stakeholders |

---

## MCP Connections

> Connect Claude Code to your tools for richer context.

- **Notion:** [FILL IN — paste your workspace URL or leave blank]
- **Linear / Jira:** [FILL IN — project URL or leave blank]
- **Slack:** [FILL IN — workspace name or leave blank]

---

## Context Library

Shared knowledge files live in `context/`. Reference them with `@context/...` in any prompt.

| File | What it contains |
|------|-----------------|
| `@context/company.md` | Company overview, ICP, OKRs, competitive landscape |
| `@context/competitors/[name].md` | Per-competitor profiles (use `_template.md` to add one) |
| `@context/product/knowledge-base.md` | Product features, terminology, limitations |
| `@context/product/prds/` | Drop existing PRDs here for Claude to reference |
| `@context/meetings/[date-topic].md` | Meeting notes and interview summaries |

See `context/README.md` for usage examples.

---

## Context Management

- Suggest `/clear` when switching between unrelated tasks.
- Use `@path/to/file` to reference docs — never ask to paste content.
- Keep the context window lean — reference files instead of pasting them.
