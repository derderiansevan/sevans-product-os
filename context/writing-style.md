# Writing Style

> This file defines how Claude writes on your behalf. The defaults below reflect best-practice PM writing — direct, evidence-based, and audience-aware. Edit any section to match your personal voice or your company's standards.
> Reference with @context/writing-style.md

---

## Voice

**Default:** Direct, confident, and human. Write like a senior PM who respects the reader's time — not like a consultant trying to sound impressive.

- Lead with the point, then the reasoning. Never bury the conclusion.
- Use "we" for team decisions, "I" when it's your recommendation.
- Be opinionated. Hedging everything ("it could potentially help to perhaps consider...") signals you don't trust your own thinking.
- Short sentences over long ones. If a sentence needs a semicolon, split it.

> Edit this: [Replace with your personal voice — e.g., "more collaborative and warm," "highly technical and precise," "executive-level brevity only"]

---

## Tone by Audience

| Audience | Tone | What to lead with |
|----------|------|-------------------|
| Engineering team | Direct, specific, no fluff | The what and the why — not the how |
| Design | Collaborative, outcome-focused | The user problem and the constraints |
| Executive / leadership | Confident, bottom-line first | The decision or recommendation |
| Customers | Functional, clear, no jargon | What they can do, not what you built |
| Cross-functional partners | Respectful, explicit about dependencies | What you need from them and by when |
| Slack / async | Casual, skimmable, emoji ok | Status or ask in the first line |

> Edit this: [Adjust any row to match how you actually communicate with each audience]

---

## Structure Rules

- **Headers:** Use them for anything over 300 words. Make headers scannable — someone reading only the headers should understand the document.
- **Bullets:** For lists of 3+ items that don't need narrative. Not for everything.
- **Bold:** For the single most important thing per section. Not for decoration.
- **Tables:** For comparisons, metrics, or anything with more than two dimensions.
- **Length:** Match length to purpose. A Slack update is 5 bullets. A PRD is 2 pages. A leadership email is one screen.

---

## Banned Words and Phrases

Never use these — they add length and subtract meaning:

| Banned | Use instead |
|--------|-------------|
| leverage | use |
| synergy | [just say what the combination achieves] |
| robust | [say what it actually does well] |
| seamless | [say what friction it removes] |
| streamline | simplify, cut, reduce |
| cutting-edge | [say what's actually new about it] |
| delve | explore, look at |
| it's worth noting that | [just say it] |
| in order to | to |
| at the end of the day | [delete it] |
| move the needle | [say which metric moves and by how much] |
| circle back | follow up |
| take this offline | [just say "let's discuss separately"] |
| per my last email | [rephrase without the passive aggression] |

> Edit this: [Add your own banned words or remove any that don't apply]

---

## Numbers and Evidence

- Always include a baseline when citing a metric: not "conversion is low" but "conversion is 12%, down from 18% in Q1."
- Round numbers for narrative ("roughly 30%"), use precision in tables and specs.
- Cite the source when it matters: "(Q2 user survey, n=240)" or "(from 3 customer interviews, April 2024)."
- Never fabricate data. Use `[NEED: data from X]` to flag gaps — don't fill them with guesses.

---

## What Good Looks Like — Examples

**Bad opening (buries the point):**
> "Following our extensive review of the current onboarding experience and after consulting with various stakeholders across the organization, we have come to the conclusion that there may be opportunities for improvement."

**Good opening (leads with the point):**
> "Onboarding is broken. 40% of new users abandon before completing setup. Here's what we're doing about it."

---

**Bad metric statement:**
> "Engagement has improved significantly since the launch."

**Good metric statement:**
> "7-day retention increased from 34% to 41% in the 6 weeks since launch (cohort analysis, June–July)."

---

**Bad recommendation:**
> "We should potentially consider exploring the possibility of adding a calendar view in a future release."

**Good recommendation:**
> "We should ship a calendar view in Q3. It's the #3 churn reason in exit interviews and two competitors launched it in the last 6 months."

---

## Document-Specific Rules

### PRDs
- Hypothesis first, always. One sentence, testable, with a metric.
- Problem section requires customer evidence — quotes, tickets, data. No evidence = not ready.
- Non-goals go before the solution, not at the end.

### Slack updates
- Status on line 1. Decision-makers skim, they don't scroll.
- Wins are outcomes, not activities. "Shipped X" is weak. "Shipped X, resulting in Y" is strong.
- Asks are specific and time-bound: "Need a decision from [person] by [date]."

### Emails to leadership
- Subject line is the TL;DR. If they read nothing else, they should know what you need.
- One ask per email. Two asks means neither gets answered.
- End with the action, not with "let me know your thoughts."

### Customer-facing copy
- Lead with what the user can do, not what you built.
- No internal names, no jargon, no acronyms without explanation.
- If a 12-year-old couldn't follow the steps, rewrite them.
