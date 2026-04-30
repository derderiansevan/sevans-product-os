# PRD: [Feature Name]

**Stage:** <!-- Team Kickoff | Planning Review | Launch Readiness -->
**Author:** [Name]
**Last updated:** [YYYY-MM-DD]
**Status:** <!-- Draft | In Review | Approved | Shipped -->

---

## Hypothesis

> One sentence. Testable. Has a metric. Example:
> "If we add a bulk export feature, Legal Ops users will complete their compliance workflow without leaving the product, reducing churn among the enterprise tier by 10%."

We believe that **[doing X]** will cause **[user segment]** to **[behavior change]**, resulting in **[measurable outcome]**.

---

## Problem

> This section requires customer evidence. No evidence = not ready to proceed.

**What's broken and for whom:**
[Describe the problem in 2–3 sentences. Be specific about which users are affected and in what context.]

**Evidence:**

| Source | Finding |
|--------|---------|
| [Customer interviews, n=X, Month Year] | "[Exact quote from a user]" |
| [Support tickets, last 90 days] | [X tickets with theme Y — link if available] |
| [Data / analytics] | [Metric with baseline, e.g. "42% of users abandon at step 3"] |
| [Sales / CS input] | [Deal blocked / churn reason — specific example] |

**Who is most affected:**
[Primary user persona — be specific. Not "all users." Which segment, in which workflow, at what frequency.]

**Current workaround:**
[What do users do today? Why is it insufficient?]

---

## Non-goals

> What we are explicitly NOT building with this initiative. Define the boundary before the solution.

- We are not building [X] because [reason — sequencing, scope, different team, etc.]
- We are not solving [Y] in this version. [Brief rationale.]
- We are not targeting [user segment Z] with this release.

---

## Success metrics

> Every metric needs a baseline and a time window. No targets without a denominator.

| Metric | Baseline (today) | Target | Time window | Owner |
|--------|-----------------|--------|-------------|-------|
| [Primary metric — behavior change] | [X%] | [Y%] | [e.g. 60 days post-launch] | [PM/Data] |
| [Secondary metric — leading indicator] | [X] | [Y] | [30 days post-launch] | [PM/Data] |
| [Counter-metric — catch regressions] | [X] | No regression | [60 days post-launch] | [PM/Data] |

**How we'll measure:**
[What instrumentation exists? What needs to be built? Who is responsible for the measurement plan?]

---

## Solution

> Write what you're building, not how you're building it. The "how" belongs in the eng spec.

### Overview

[2–3 sentences. What does this feature do? What changes for the user?]

### User flows

**Happy path:**
1. [User starts at — describe the entry point]
2. [User does — describe the action]
3. [System responds — describe the outcome]
4. [User reaches — describe the end state]

**Edge cases and error states:**

| Scenario | Expected behavior |
|----------|-----------------|
| [Empty state / first use] | [What does the user see?] |
| [Error condition] | [What message? What recovery action?] |
| [Partial failure] | [What is preserved? What is lost?] |

### Scope

**In scope:**
- [Feature or behavior 1]
- [Feature or behavior 2]

**Out of scope (this version):**
- [Explicitly deferred item — note why or when]

### Mockups / design links

[Link to Figma or embed screenshots. If not ready, note the open design question blocking this.]

---

## Dependencies

| Dependency | Team / Owner | Status | Date needed |
|------------|-------------|--------|-------------|
| [API / service / data needed] | [Team name] | [Not started / In progress / Done] | [Date] |
| [Design spec] | [Designer name] | [Status] | [Date] |
| [Legal / compliance review] | [Owner] | [Status] | [Date] |

---

## Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| [Technical risk — e.g. performance at scale] | [H/M/L] | [H/M/L] | [What's the plan?] |
| [Adoption risk — e.g. users don't discover it] | [H/M/L] | [H/M/L] | [What's the plan?] |
| [Business risk — e.g. affects enterprise tier] | [H/M/L] | [H/M/L] | [What's the plan?] |

---

## Open questions

| Question | Owner | Deadline |
|----------|-------|----------|
| [Unresolved question blocking design or eng] | [Name or role] | [Date] |
| [Decision needed from stakeholder] | [Name] | [Date] |

---

## Rollout plan

**Target audience at launch:** [e.g. Internal beta → 10% of enterprise accounts → GA]

| Phase | Who | What | Success gate to advance |
|-------|-----|------|------------------------|
| Alpha | [e.g. 3 design partners] | [What they get access to] | [Threshold to move forward] |
| Beta | [e.g. 10% of segment] | [Full feature] | [Metric threshold] |
| GA | All eligible users | [Full feature] | [Metric threshold] |

**Rollback plan:**
[Under what condition do we turn this off? Who makes that call? How quickly can we revert?]

---

## Definition of done

- [ ] Happy path works end-to-end for primary user flow
- [ ] All error states display correctly with recovery paths
- [ ] Empty state is defined and implemented
- [ ] Success metrics are instrumented and confirmed with data team
- [ ] Help Center article drafted and reviewed
- [ ] Stakeholder review completed (PM, Eng lead, Design lead)
- [ ] Launch communication sent to CS / Sales
