# Competitive Analysis Skill for Claude

A consulting-grade competitive analysis skill for Claude that produces structured, insight-driven analysis modeled on McKinsey/BCG methodology, but the final output is of course not quite that! What you can do here is give Claude a company and a market, then get back a professional PowerPoint deck, a fully-documented Excel data workbook, and actionable strategic recommendations.

NOTE: The goal here is to offer a jump-start to a genreal overview, not be a final destination. It's to offer a strategist or product person a starting place in consideration of next steps. As amazing as AI tool are, we should still be thinking. My goal is making this was to build just a little step-stool for getting to the next level, not a final outocme.

Last Warning: Trust, but Verify! You get a great starting point with this. That's the goal.

This skill should be compatible with free, Pro, Max, Team, and Enterprise plans. Free plan users may experience interruptions on longer analyses due to usage limits. A Pro plan or higher is recommended for best results.

---

# Disclaimer
This skill uses only publicly available data. No guarantees are made as to the accuracy, completeness, or validity of any output. AI-generated analysis can contain errors, outdated information, or misinterpretations even when based on credible sources — all outputs should be verified before use in business decisions. If you extend this skill with data from proprietary or subscription services, you assume full responsibility for compliance with your organization's data use policies and any applicable terms of service.isclaimer: There are no guarantees as to accuracy or validity of any output here. This skill uses only publicly available data. Rich data sources from proprietary services is unavailable to this skill unless you add it based on your own subscriptions. If doing so, you assume any risk regarding your company's policies for using such data.

# Project Suggestion
It might be useful to create a Project that's specific to Competitive Analysis. You an add custom needs like this, without modifying the skill files themselves, which of course you can always do.

Here's an example:
Use the competitive analysis skills for this project.

Consider additional business analysis frameworks that might be appropriate beyond what the skills may include.

Use whatever publicly available data you can reach.

In an appendix, list any other data sources, (up to 10), which might be useful, but were unavailable as they're behind paywalls or subscriptions.


## What This Skill Does

Most competitive analyses are data dumps. This skill enforces a different standard: every finding must answer "So what?", every claim must have a source, and the output must end in a clear recommendation. 

When you trigger this skill, Claude will:

- Define the scope of the analysis with you before doing anything else
- Research each competitor across six dimensions: business model, market position, product capabilities, go-to-market, financials, and strategic direction
- Apply four analytical frameworks: Competitive Positioning Map, Capability Scorecard, SWOT, and Porter's Five Forces
- Synthesize findings into a single strategic narrative with a clear thesis
- Build a professional PowerPoint deck (slide-by-slide blueprint included)
- Build a backup Excel workbook with all data, sources, and confidence ratings documented
- Run a final quality check — including a "CEO Test," "Deleted Data Test," and "Red Team Test" — before delivering

### Output Files

| File | Purpose |
|---|---|
| `[Company]_Competitive_Analysis.pptx` | The main presentation deck |
| `[Company]_Competitive_Data.xlsx` | Full data backup: scoring, financials, sources, sentiment |
| `[Company]_Sources.pdf` *(optional)* | Exported source log |

---

## What's Inside the Skill

```
competitive-analysis/
├── SKILL.md                      ← Master skill: golden rules, workflow, voice guidelines
├── README.md                     ← Internal navigation guide
└── references/
    ├── framework.md              ← All analytical models with construction instructions
    ├── research-guide.md         ← What to research, where, source quality tiers
    ├── slide-blueprint.md        ← Every slide defined: purpose, content, design
    ├── data-tables.md            ← 8-tab Excel backup workbook structure
    └── quality-standards.md     ← Final QA checklist before delivery
```

### The Five Golden Rules

These are enforced on every analysis this skill produces:

1. **Insight Over Information** — Every chart, table, and finding must have a one-sentence conclusion. Raw data with no interpretation is not acceptable.
2. **One Storyline** — The entire analysis supports a single strategic thesis. Everything that doesn't reinforce it gets cut or moved to the appendix.
3. **Evidence-Backed Claims** — No assertion without a source. Every claim is tagged by source type. Estimates are labeled as estimates.
4. **Decision-Ready Output** — The final slide always answers: "What are the 3 things leadership should do next?"
5. **Pyramid Structure** — Lead with the conclusion. Slide titles are findings, not topics.

---

## Requirements

- A Claude account on any paid plan (Pro, Max, Team, or Enterprise) — Skills are also available on the free plan
- Code execution enabled in your Claude settings (Skills require this)
- Claude's built-in **pptx** and **xlsx** skills are used automatically for file output — no separate installation needed

---

## Installation

**Step 1 — Download the ZIP**

Download `competitive-analysis.zip` from this repository.

**Step 2 — Enable Code Execution in Claude**

Go to **Settings → Capabilities** and make sure **"Code execution and file creation"** is toggled on.

**Step 3 — Upload the Skill**

Go to **Customize → Skills** and upload the ZIP file. Keep the folder structure intact inside the ZIP — Claude needs to find `SKILL.md` inside a `competitive-analysis/` folder.

**Step 4 — Activate It**

After uploading, your skill will appear in the skills list with a toggle switch. Flip it **ON**.

**Step 5 — Start a New Chat**

Skills only activate in conversations started after the toggle is enabled.

> **Team & Enterprise users:** Organization owners can provision this skill for all users via **Admin Settings → Skills**, so every team member gets it automatically without individual uploads.

---

## How to Use It

You don't call the skill manually — Claude loads it automatically when it recognizes the intent. Just describe what you need in natural language.

### Trigger phrases that activate the skill

- "competitive analysis"
- "market landscape"
- "benchmark against competitors"
- "how do we stack up"
- "competitor research"
- "SWOT analysis"
- "Porter's Five Forces"

### Example prompts

A minimal request:
```
Run a competitive analysis of Notion vs. its main competitors in the B2B productivity space.
```

A well-scoped request (recommended — gets better results faster):
```
I need a competitive analysis for my company, Acme Corp. We sell B2B project management 
software to mid-market companies. Main competitors are Asana, Monday.com, and Smartsheet. 
The output will inform our 2026 pricing strategy. Audience is our exec team.
```

For a quick landscape vs. a deep dive:
```
Give me a quick competitive landscape for [Company] — I just need the positioning map 
and scorecard, not the full deck.
```

### Pro tip: Use a Claude Project

If you're doing multiple analyses or returning to this work over time, create a **Claude Project** and add your company background, industry context, and any internal documents as project knowledge. Claude will carry that context into every conversation automatically, so you don't have to re-explain your company each time.

---

## Analytical Frameworks Included

| Framework | Purpose |
|---|---|
| Competitive Positioning Map | Places all competitors visually on strategically chosen axes; reveals white space |
| Capability Scorecard (Heatmap) | Rates every competitor 1–5 on 8–12 buyer-relevant criteria |
| SWOT Analysis | Strengths/Weaknesses/Opportunities/Threats — derived from competitive data, not brainstormed |
| Porter's Five Forces | Structural assessment of the market: rivalry, entrants, substitutes, buyer power, supplier power |
| GTM Comparison | Side-by-side go-to-market analysis: sales motion, channels, pricing model, partnerships |
| Funding & Financial Trajectory | Revenue estimates, growth signals, funding history *(optional, used for investor-facing work)* |
| Customer Sentiment Analysis | G2/Capterra/review mining for top praise and complaint themes *(optional)* |
| Strategic Move Timeline | 12–24 month timeline of significant competitor moves *(optional)* |

---

## The Slide Deck Structure

Every deck produced by this skill follows a defined blueprint:

| Slide | Content |
|---|---|
| 1 | Cover |
| 2 | Executive Summary — key findings as complete insight sentences |
| 3 | Scope & Methodology |
| 4 | Market Overview — size, growth, structural dynamics |
| 5 | Competitive Landscape Map |
| 6–N | Individual Competitor Profiles (one per Tier 1 competitor) |
| N+1 | Capability Scorecard heatmap |
| N+2 | Go-to-Market Comparison |
| N+3 | SWOT Analysis |
| N+4 | Porter's Five Forces |
| N+5 | Strategic Implications |
| N+6 | Recommendations |
| Appendix | Supporting data, Tier 2 competitor profiles, source log |

---

## Suggested Companion Skills

The following additional skills would complement this one if you want to build a full competitive intelligence system. They are not included here but are good candidates for future development:

- **`market-sizing.md`** — TAM/SAM/SOM estimation methodology
- **`customer-voice.md`** — Protocol for mining G2, Capterra, and review sites systematically
- **`financial-signals.md`** — Estimating private company financials from proxy data
- **`gtm-intelligence.md`** — Reverse-engineering competitor go-to-market from public signals
- **`executive-narrative.md`** — Writing guide for consulting-quality strategic prose

---

## Contributing

Contributions welcome. If you improve a reference file, add a new analytical framework, or build one of the companion skills listed above, please open a pull request.

---

## License

MIT License — free to use, modify, and share.

---

*Built as a Claude custom skill using the Agent Skills standard. Compatible with Claude.ai (Pro/Max/Team/Enterprise), Claude Code, and the Claude API.*
