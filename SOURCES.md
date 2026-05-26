# Sources

Canonical list of sources for Neurotech Pulse. Organised by editorial priority thread (see `CLAUDE.md` for priorities). Edit freely — add, update, remove. The brief points here, not vice versa.

**Conventions:**
- One source per bullet. Primary sources first.
- Include a URL where useful, plus a one-line note on *what it covers*.
- Mark UK-specific sources with 🇬🇧.
- Mark anything paywalled with **(paywall)**.
- Remove a source if it goes dark, paywalls everything, or starts publishing slop.

---

## 1. AI & Decoding *(top priority)*

**Discovery feeds (highest signal — check these first)**
- [HuggingFace — Papers](https://huggingface.co/papers) — daily ML paper digest with code links; high recall on neural-FM releases
- [arxiv-sanity-lite](https://arxiv-sanity-lite.com/) — saved keyword queries against arXiv. Build queries for: "EEG foundation model", "neural decoder", "brain-to-text", "neural foundation model", "spike forecasting"
- arXiv keyword searches as a manual fallback — e.g. [EEG foundation model](https://arxiv.org/search/?query=EEG+foundation+model&searchtype=all), [brain decoder](https://arxiv.org/search/?query=brain+decoder&searchtype=all)
- Google Scholar alerts — same keyword set as arxiv-sanity-lite, catches the journal-side
- [Papers With Code — EEG](https://paperswithcode.com/task/eeg), [neural decoding leaderboards](https://paperswithcode.com/search?q=neural+decoding) — surfaces new SOTA with code attached
- [GitHub topic: eeg](https://github.com/topics/eeg), [bci](https://github.com/topics/bci), [brain-computer-interface](https://github.com/topics/brain-computer-interface) — sort by recently updated / stars this week

**HuggingFace organisations to watch** *(orgs that have shipped a neural FM at least once — add new ones on first release)*
- [Zyphra](https://huggingface.co/Zyphra) — ZUNA (380M EEG masked-diffusion autoencoder, Feb 2026) and follow-ons
- [brain-bzh](https://huggingface.co/brain-bzh) — REVE (EEG FM pretrained on 25k subjects) and the IMT Atlantique pipeline
- Static search backup: [HF models — eeg](https://huggingface.co/models?search=eeg), [HF datasets — eeg](https://huggingface.co/datasets?search=eeg)

**Preprint & journal indices (firehose backstops)**
- arXiv [cs.LG new submissions](https://arxiv.org/list/cs.LG/new), [q-bio.NC new submissions](https://arxiv.org/list/q-bio.NC/new), [cs.CL new submissions](https://arxiv.org/list/cs.CL/new) — thousands/day; only useful via saved queries above
- [bioRxiv neuroscience](https://www.biorxiv.org/collection/neuroscience) — applied / industry-affiliated only
- [OpenReview](https://openreview.net/) — neuroscience/BCI-tagged submissions
- [Cell Reports](https://www.cell.com/cell-reports/home), [Cell](https://www.cell.com/cell/home), [Nature Neuroscience](https://www.nature.com/neuro/), [Science Advances](https://www.science.org/journal/sciadv), [Journal of Neural Engineering](https://iopscience.iop.org/journal/1741-2552)

**Lab groups**
- [Chang Lab](https://changlab.ucsf.edu/) — UCSF, brain-to-speech
- [Henderson Lab / Willett](https://nplab.stanford.edu/) — Stanford, BrainGate, inner speech
- [Meta FAIR brain group](https://ai.meta.com/research/) — non-invasive decoding
- Pandarinath, Cunningham, Kording labs — neural foundation models, computational tooling
- [Brain-BZH](https://brain-bzh.github.io/) — IMT Atlantique, EEG foundation models (REVE)
- European applied-neuro labs to sweep — Donders (Nijmegen), MPI Tübingen, ETH Zürich neuroengineering, EPFL (Micera), KU Leuven (CORTEG)

**AI labs with neural-data work** *(watchlist — generalist AI shops pivoting into neural data; expand on first release)*
- [Zyphra](https://www.zyphra.com/) — shipped ZUNA Feb 2026. Foundation-model lab, not a neuro lab — the kind of org the lab-groups bucket misses by construction
- Add new entries the first time a generalist AI lab ships anything trained on neural data, even if it's a one-off

**Conferences**
- NeurIPS NeuroAI workshops, ICLR, ICML neural-data papers, Cosyne, IEEE NER, IEEE BCI Society

**Industry AI work**
- [Neuralink updates](https://neuralink.com/updates/) — decoder posts
- Synchron, Precision Neuro AI integrations — watch company blogs (see Industry section)

---

## 2. Industry & Applied

**Company blogs (direct)**
- [Neuralink](https://neuralink.com/blog/)
- [Synchron](https://synchron.com/news)
- [Paradromics](https://www.paradromics.com/news)
- [Precision Neuroscience](https://precisionneuro.io/news/)
- [Blackrock Neurotech](https://blackrockneurotech.com/insights/)
- [Motif Neurotech](https://motifneuro.com/news/)
- [Inbrain Neuroelectronics](https://www.inbrain-neuroelectronics.com/news)
- [Onward Medical](https://onwd.com/news/)
- [Cortical Labs](https://corticallabs.com/news.html)
- [Cumulus Neuroscience](https://www.cumulusneuro.com/) 🇬🇧 — Belfast, at-home clinical EEG headset; pharma & dementia-study partnerships, peer-reviewed neuroplasticity validation
- [Flow Neuroscience](https://www.flowneuroscience.com/blog/) 🇬🇧 — UK/Sweden, at-home tDCS for depression; FDA-cleared FL-100, NHS deployments
- [Neurable](https://www.neurable.com/) — consumer-form-factor BCI (EEG headphones, HyperX gaming headset); licensing model for wearables

**Trade press**
- [STAT News — neurotech](https://www.statnews.com/category/tech/) **(paywall — headlines free)**
- [Endpoints News](https://endpts.com/) **(paywall — headlines free)**
- [FierceBiotech](https://www.fiercebiotech.com/)
- [MedCity News](https://medcitynews.com/)
- [MedTech Dive](https://www.medtechdive.com/)
- [Medical Device Network](https://www.medicaldevice-network.com/)
- [NeuroNews International](https://neuronewsinternational.com/)

**Funding & deals**
- [BusinessWire — health](https://www.businesswire.com/portal/site/home/?ndmViewId=news_view&newsLang=en) — press releases
- Crunchbase neurotech tracker — manual sweep

---

## 3. Clinical & Regulatory

- [FDA device approvals](https://www.fda.gov/medical-devices/products-and-medical-procedures/device-approvals-denials-and-clearances) — 510(k), De Novo, PMA
- [FDA Breakthrough Devices](https://www.fda.gov/medical-devices/how-study-and-market-your-device/breakthrough-devices-program)
- [MHRA news (UK)](https://www.gov.uk/government/organisations/medicines-and-healthcare-products-regulatory-agency) 🇬🇧
- EU MDR / CE-mark registries
- [ClinicalTrials.gov](https://clinicaltrials.gov/) — neurotech trial registrations
- [ISRCTN Registry](https://www.isrctn.com/) 🇬🇧 — UK trials
- [IEEE TNSRE](https://www.embs.org/tnsre/), [Brain Stimulation](https://www.brainstimjrnl.com/), [Journal of Neural Engineering](https://iopscience.iop.org/journal/1741-2552)

---

## 4. Data Science & Tooling

- [MNE-Python releases](https://github.com/mne-tools/mne-python/releases)
- [Braindecode releases](https://github.com/braindecode/braindecode/releases)
- [NeuroKit2 releases](https://github.com/neuropsychology/NeuroKit/releases)
- [MOABB](https://github.com/NeuroTechX/moabb)
- [NWB / DANDI Archive](https://dandiarchive.org/) — datasets
- [GitHub trending — neuroscience topic](https://github.com/topics/neuroscience)
- HuggingFace dataset releases (see AI & Decoding)

**Living surveys / awesome-lists** *(community-maintained reading lists; treat as continuously-updated survey papers)*
- GitHub search: [awesome BCI](https://github.com/search?q=awesome+bci&type=repositories), [awesome EEG](https://github.com/search?q=awesome+eeg&type=repositories), [awesome NeuroAI](https://github.com/search?q=awesome+neuroAI&type=repositories)
- When a high-quality list surfaces, pin it here by name and check its commit log monthly

---

## 5. UK ecosystem 🇬🇧

**Funders**
- [UKRI](https://www.ukri.org/news/)
- [Innovate UK](https://www.ukri.org/councils/innovate-uk/news/)
- [ARIA — Precision Neurotechnologies](https://aria.org.uk/opportunity-spaces/scalable-neural-interfaces/precision-neurotechnologies/)
- [ARIA — Massively Scalable Neurotechnologies](https://aria.org.uk/opportunity-spaces/scalable-neural-interfaces/massively-scalable-neurotechnologies/)
- [MRC](https://www.ukri.org/councils/mrc/news/)
- [Wellcome Leap](https://wellcomeleap.org/news/)

**Companies**
- [BIOS Health](https://www.bios.health/)
- [MintNeuro](https://mintneuro.com/)
- [Cogitat](https://www.cogitat.io/)
- [Galvani Bioelectronics](https://www.galvani.bio/)
- [Neurokopia](https://www.neurokopia.com/)
- [Cumulus Neuroscience](https://www.cumulusneuro.com/) — Belfast, clinical at-home EEG (also in Industry company blogs)
- [Flow Neuroscience](https://www.flowneuroscience.com/) — UK/Sweden, at-home tDCS depression device (also in Industry company blogs)

**Labs with industry partnerships**
- Imperial, UCL, Oxford, Cambridge, Edinburgh — neurotechnology / bioelectronics groups

**Hiring signals**
- LinkedIn UK neurotech postings (manual sweep, monthly)

---

## 6. Field context / research with translation

- [Nature](https://www.nature.com/), [Nature Biomedical Engineering](https://www.nature.com/natbiomedeng/), [Nature Neuroscience](https://www.nature.com/neuro/)
- [Science](https://www.science.org/), [Science Advances](https://www.science.org/journal/sciadv), [Science Translational Medicine](https://www.science.org/journal/stm)
- [bioRxiv — neuroscience](https://www.biorxiv.org/collection/neuroscience) — industry-affiliated submissions only
- University press rooms — UCSF, Stanford, Hopkins, MIT, Caltech, Imperial 🇬🇧, UCL 🇬🇧, Oxford 🇬🇧, Cambridge 🇬🇧

---

## 7. Newsletters & aggregators *(use as leads, not citations)*

- [Neurotechnology by Naveen Rao (Substack)](https://neurotechnology.substack.com/) — fortnightly notables
- [IEEE Pulse](https://www.embs.org/pulse/)
- [HuggingFace Papers](https://huggingface.co/papers) — daily ML paper digest (also listed in section 1 as a discovery feed; high enough recall on neural FMs to belong in both places)

**Curated neuroAI accounts (X / Bluesky)** *(leads only — names to search; verify handle before relying on it)*
- Patrick Mineault — neuroAI commentary, tooling
- Iulia Comsa — neural data + ML
- Konrad Kording — applied neuro + ML methods
- Andreas Tolias — neural foundation models
- Eli Shlizerman — neural decoding methods
- Cosyne / NeurIPS NeuroAI workshop accounts — release announcements during and after events

**Note:** Newsletters and accounts are lead sources only — *follow the link to the primary source before citing*.
