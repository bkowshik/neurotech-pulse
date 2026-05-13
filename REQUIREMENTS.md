# Neurotech Pulse — Requirements

> Tracking the pulse of neurotechnology — daily signals, weekly synthesis, monthly highlights.

**Live site:** https://bkowshik.github.io/neurotech-pulse/

## 1. Purpose

A curated, Claude-generated newsletter covering **applied neurotechnology** — the companies, products, clinical deployments, and the data science and AI behind them.

**Cutting-edge AI developments in neurotech are the top priority** — foundation models for neural data, brain-to-text and brain-to-speech decoders, multimodal neural LLMs, and the model architectures and datasets driving them.

Industry-leaning, practitioner-focused, research-aware. Published as a Quarto site on GitHub Pages.

## 2. Goals

**Primary** — Build and maintain a structured personal knowledge feed on applied neurotech and the AI/data-science craft underpinning it, so I stay current without drowning in sources.

**Secondary** — Publish it openly so others working at the same intersection — practitioners entering the field, researchers tracking translation, engineers picking up neural data — can use it as a curated jumping-off point.

## 3. Audience

1. **Me, first.** Every editorial decision optimises for my own learning as a data scientist working at this intersection.
2. **Adjacent practitioners** — ML engineers, signal-processing folks, clinical engineers building on or near neural data, with a particular tilt toward the UK ecosystem.
3. **Decision-makers in the field** — anyone scoping a problem, evaluating a technology, or trying to understand where applied neurotech is actually moving.

## 4. Scope

The newsletter sits at the intersection of three threads. Every issue should touch at least two; the **AI & Decoding** sub-thread takes priority over everything else.

| Thread | What it covers |
|---|---|
| **AI & Decoding** *(priority)* | Foundation models for neural data, brain-to-text/speech decoders, neural LLMs, multimodal models, novel architectures, scaling laws for neural data |
| **Industry & Applied** | Companies, products, clinical trials, funding rounds, regulatory milestones (FDA / MHRA / CE), M&A, partnerships |
| **Data Science & Tooling** | Open-source neuro-ML libraries, datasets, benchmarks, MLOps for medical devices, signal processing |
| **Field Context** | UK ecosystem, translational research, clinical deployments, hiring signals |

**In scope**

- Frontier AI applied to neural data — LaBraM, POYO, Neuroformer, BrainBERT, BIOT, NeuroLM, and successors
- Brain-to-text / brain-to-speech systems (Willett / Chang / Meta groups, industry equivalents)
- BCIs (invasive and non-invasive), neural implants, neurostimulation — as deployed or commercialised
- Neuroimaging hardware and software that ships (fMRI, MEG, fNIRS, EEG)
- Open-source tooling — MNE-Python, Braindecode, NeuroKit2, MOABB, NWB, DANDI
- Industry — company news, funding, regulatory, clinical, M&A, hiring
- UK-specific items — labs with industry ties, companies, funding, jobs

**Out of scope**

- Pure basic neuroscience with no translation or AI angle
- Wellness wearables without clinical validation
- Speculative futurism, transhumanism takes
- Pure ML papers with no neural-data application

## 5. Cadences

### Daily
- Aim for ~5 items, each a 1-paragraph summary + source link; strength beats count, no fixed floor
- Sections in priority order: **AI & Decoding** / **Industry** / **Clinical & Regulatory** / **Tools & Data** / **UK** / **Research with applications**
- ≥1 **AI & Decoding** item where the week's signal allows; this is the lede when present
- Target: 300–500 words total
- Time budget: 10–15 min review/edit

### Weekly
- Synthesis of the week's daily posts — 600–900 words
- Identifies 2–3 themes; at least one should connect to AI/ML craft
- Recurring slot: **Frontier Watch** — one model, paper, or technique from the AI-in-neurotech frontier
- "What I'm watching next week"
- Time budget: 30–45 min

### Monthly
- Highlights reel (top 10 stories of the month)
- One deep dive — rotates through:
  - **Frontier Model Spotlight** — a neural foundation model or decoder architecture, dissected
  - **Company Spotlight** — what they build, how, and who they hire
  - **Paper-to-Production** — a research idea that made it into a shipped product
- **UK Jobs & Funding** section — who's hiring (DS/ML roles called out), recent grants, ecosystem signals
- Time budget: 1–2 hours

## 6. Content Sources

The canonical, editable source list lives in [`SOURCES.md`](./SOURCES.md). Organised by the same priority threads as §4. Add, update, or remove sources there without touching this file or `CLAUDE.md` — the brief points to `SOURCES.md`, not vice versa.

Source categories (see `SOURCES.md` for the full list):

1. **AI & Decoding** *(priority)* — arXiv, Hugging Face, lab groups (Chang / Henderson / Meta FAIR), industry AI posts, conference proceedings
2. **Industry & Applied** — direct company blogs first, then trade press, then aggregators
3. **Clinical & Regulatory** — FDA / MHRA / EU MDR, ClinicalTrials.gov, ISRCTN, neural-engineering journals
4. **Data Science & Tooling** — open-source release notes, DANDI / NWB datasets, GitHub trending
5. **UK ecosystem** — UKRI / Innovate UK / ARIA / Wellcome Leap, UK companies, UK university labs
6. **Field context** — top-tier journals and university press rooms

## 7. Tech Stack

| Layer | Tool |
|---|---|
| Site generator | Quarto |
| Hosting | GitHub Pages — https://bkowshik.github.io/neurotech-pulse/ |
| CI/CD | GitHub Actions (Quarto render + Pages deploy) |
| AI author | Claude Code (uses Claude subscription, no API) |
| Editorial brief | `CLAUDE.md` at repo root |
| Post format | `.qmd` files, one directory per post |
| Custom domain | Not planned. GitHub Pages URL is sufficient. |

## 8. Workflow

**Claude generates the posts end-to-end. My role is review, edit, publish — not drafting.**

1. Invoke Claude Code in the repo (or use a Claude Project if not at the terminal)
2. Claude web-searches sources per `CLAUDE.md`, prioritising AI-in-neurotech
3. Claude drafts the full post from the appropriate template
4. Saves to the correct cadence folder with the correct filename pattern
5. I review, edit, commit
6. Push → GitHub Action renders → Pages deploys

No post is ever written manually. If Claude can't find enough material for a daily, the post simply doesn't go out that day — consistency of quality > consistency of cadence.

## 9. Site Structure

```
neurotech-pulse/
├── _quarto.yml                # site config, listings for each cadence
├── CLAUDE.md                  # editorial brief for Claude
├── index.qmd                  # home — combined feed
├── about.qmd                  # about me, why this exists
├── daily/
│   ├── index.qmd              # daily listing page
│   └── 2026-05-13/
│       └── index.qmd          # one daily post
├── weekly/
│   ├── index.qmd              # weekly listing page
│   └── 2026-W20/
│       └── index.qmd          # one weekly post
├── monthly/
│   ├── index.qmd              # monthly listing page
│   └── 2026-05/
│       └── index.qmd          # one monthly post
├── templates/
│   ├── daily.qmd
│   ├── weekly.qmd
│   └── monthly.qmd
└── .github/workflows/
    └── publish.yml
```

### File naming and URLs

| Cadence | Folder name | Example URL |
|---|---|---|
| Daily | `daily/YYYY-MM-DD/` | `…/daily/2026-05-13/` |
| Weekly | `weekly/YYYY-Www/` (ISO week) | `…/weekly/2026-W20/` |
| Monthly | `monthly/YYYY-MM/` | `…/monthly/2026-05/` |

ISO-8601 dates throughout — sortable on disk and in URLs, unambiguous, language-neutral. Each post lives in its own directory with an `index.qmd`, which renders to a clean URL with no `.html` suffix on GitHub Pages.

### Listing pages

- `/` — combined feed, most recent across all cadences
- `/daily/` — daily archive
- `/weekly/` — weekly archive
- `/monthly/` — monthly archive

## 10. Editorial Principles

- **AI angle leads.** When a story involves a model, decoder, or AI technique, that's the lede.
- **Applied over academic.** No translation or AI angle → skip.
- **No hype.** Preprints flagged. Company PR summarised critically, not parroted.
- **Cite primary sources.** Link to the company blog, paper, or filing — not a news write-up.
- **UK angle when present.** Flag UK relevance explicitly.
- **Brevity over completeness.** Better to miss a story than to bloat the post.
- **Voice over neutrality.** Weekly and monthly should sound like me, not a wire service.
- **Skip rather than pad.** No post if no material — see §8.

## 11. Non-Goals

- Not a real-time news service. Daily ≠ instant.
- Not a research review journal. Summaries link out; we do not reproduce paper content at length.
- Not a job board. The UK Jobs section is a monthly digest, not a feed.
- Not monetised. No ads, sponsorships, paywalls.
- Not manually written. See §8.

## 12. Success Criteria

Measured on publishing discipline and editorial coverage, not vanity metrics.

**3 months** — 60+ daily posts, 12 weekly, 3 monthly published. Site live and rendering cleanly. No backlog dread. *Frontier Watch* has covered ≥10 distinct models, papers, or techniques across the AI-in-neurotech frontier.

**6 months** — Cadence held without padding. At least one monthly deep dive from each rotation type (Frontier Model Spotlight, Company Spotlight, Paper-to-Production). The archive is dense enough to be a useful primary reference when I need to recall what happened in the field in a given week.

**12 months** — The site is something I'd treat as a genuine reference myself when reasoning about the field. The archive holds up as an honest record of where applied neurotech moved over the year.

## 13. Open Questions

- RSS feed — enable from day one (Quarto supports natively)
- Analytics — Plausible vs. GoatCounter vs. none
- Newsletter email — Buttondown / Listmonk later, or stay web-only
- Code samples in Frontier Model Spotlights — host inline, link to a separate `neurotech-pulse-notebooks` repo, or both
- Combined feed on `/` — chronological mix of all three cadences, or only show weekly + monthly with daily kept to its own page?
