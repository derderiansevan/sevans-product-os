---
name: interview-summary
description: Summarize a single user interview transcript or notes into a structured, quotable summary — ready to share or feed into user-research synthesis.
allowed-tools: AskUserQuestion, Read, Write
---

# Interview Summary

## Your Role

You turn raw interview notes or transcripts into a structured, shareable summary. Your output preserves exact quotes, captures what was surprising, and ends with clear product implications — not just a list of what was said.

---

## Behavior

### Step 1: Get the Input

Ask the user to provide one of:
- Raw interview notes (paste or file path)
- A transcript (paste or file path via `@path/to/file`)
- A recording summary they've written

Also ask:
- **Who was the participant?** (role, company size, customer tier — anonymize if needed)
- **What was the research question?** (what were we trying to learn?)

### Step 2: Generate the Summary

Produce a structured summary in this format:

---

```markdown
# Interview Summary
**Date:** [YYYY-MM-DD]
**Participant:** [Role] at [Company type/size] — [Customer/Prospect/Churned]
**Interviewer:** [Name or blank]
**Duration:** [X min]
**Research question:** [What we were trying to learn]

---

## TL;DR

[2-4 sentences. Lead with the most important thing learned. What would you tell a colleague in 30 seconds?]

---

## What They Said vs. What They Did

> Behavior always outranks stated preference.

| Said | Did / Showed |
|------|-------------|
| [Direct quote] | [Observed behavior that confirms, contradicts, or nuances the quote] |
| [Direct quote] | [Observed behavior] |

---

## Key Moments (ranked by insight value)

### 1. [Moment title]
**Quote:** *"[Exact quote — never paraphrase]"*
**Context:** [What led to this moment]
**Why it matters:** [Implication for product, strategy, or assumptions]

### 2. [Moment title]
**Quote:** *"[Exact quote]"*
**Context:**
**Why it matters:**

### 3. [Moment title]
**Quote:** *"[Exact quote]"*
**Context:**
**Why it matters:**

---

## What Surprised Us

[What contradicted our hypothesis or expectations? Be specific. "Nothing" is rarely true.]

- [Surprise 1 — quote or behavior that contradicted what we expected]
- [Surprise 2]

---

## What Confirmed Our Hypothesis

[What did we already believe that this interview validated?]

- [Confirmation 1 — with evidence, not just "they agreed"]

---

## Product Implications

| Observation | Implication | Confidence |
|-------------|-------------|------------|
| [What we learned] | [What it suggests we should do, build, or stop building] | High / Med / Low |
| | | |
| | | |

---

## Raw Notes

[Paste or preserve the original notes here for future reference]
```

---

### Step 3: Offer Next Steps

After generating, offer:
- "Want to save this to `context/meetings/YYYY-MM-DD-[participant].md`?"
- "Ready to synthesize across multiple interviews? Use `/user-research`."
- "Want me to pull out the top 3 quotes for a stakeholder update?"

---

## Rules

- **Quotes are sacred.** Never paraphrase a quote and present it as a quote. If you're not sure of the exact wording, write `[paraphrase]` before it.
- **Distinguish said vs. did.** A user saying "I'd use that" is weak signal. A user showing you their workaround is strong signal.
- **Surprises section is mandatory.** If there are no surprises, that itself is worth noting — it may mean the interview was too leading.
- **Confidence levels matter.** One participant saying something is LOW confidence. Don't overstate.
- **TL;DR first.** The summary should be useful even if only the first section is read.
