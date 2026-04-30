# Context Library

This folder is your shared knowledge base. Fill it in once — Claude reads it automatically when you reference files with `@context/...`.

---

## Structure

```
context/
├── writing-style.md        ← Voice, tone by audience, banned words, document-specific rules
├── company.md              ← Company overview, ICP, OKRs, positioning, competitive landscape
├── competitors/
│   ├── _template.md        ← Copy this to add a new competitor profile
│   └── [competitor].md     ← One file per competitor
├── product/
│   ├── knowledge-base.md   ← Product features, terminology, limitations, recent changes
│   └── prds/               ← Drop existing PRDs here for Claude to reference
└── meetings/
    ├── _template.md        ← Copy this for any meeting notes
    └── [YYYY-MM-DD-topic].md
```

---

## How to use it

**Reference any file in a prompt:**
```
Write a PRD for @context/product/prds/onboarding-v2.md
```
```
Analyze @context/competitors/ironclad.md and update our differentiation strategy
```
```
Summarize the key decisions from @context/meetings/2024-04-15-roadmap-review.md
```

**The skills reference context automatically:**
- `/competition-analysis` reads competitor files if you reference them
- `/prd-writer` will pull from `knowledge-base.md` if you tell it to
- `/interview-summary` suggests saving output to `meetings/`

---

## Filling priority order

1. **`writing-style.md`** — already pre-filled with PM defaults, edit to match your voice
2. **`company.md`** — fills in the strategic context behind every skill output
2. **`product/knowledge-base.md`** — makes customer docs and PRDs accurate
3. **`competitors/`** — one file per main competitor, use `_template.md`
4. **`product/prds/`** — drop in your most important existing PRDs
5. **`meetings/`** — use `_template.md` for any meeting, `/interview-summary` for user calls
