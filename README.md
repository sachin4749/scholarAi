<div align="center">

# 📄 ScholarAI

### Format your research paper for submission — without losing your own voice.

A free, client-side manuscript formatting tool that turns a student's draft into a publisher-ready paper for **IEEE, Springer, Elsevier, ACM, and Nature** — complete with citation verification, a submission-readiness checklist, and an AI writing assistant that gives feedback *without* writing the paper for you.

[![Live Demo](https://img.shields.io/badge/demo-live-2563EB?style=for-the-badge)](https://sachin4749.github.io/scholarAi/)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](LICENSE)
[![Made with Vanilla JS](https://img.shields.io/badge/built%20with-vanilla%20JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#-tech-stack)
[![Powered by Supabase](https://img.shields.io/badge/backend-Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)

**[Live Demo](https://sachin4749.github.io/scholarAi/)** · **[Report a Bug](../../issues)** · **[Request a Feature](../../issues)**

</div>

<br>

## ✨ Overview

ScholarAI is a single-page manuscript workbench, built for students preparing their first journal or conference submission. Upload a draft (or start from scratch), and ScholarAI walks you through detecting your paper's structure, filling in author metadata, formatting figures, verifying every citation against CrossRef, and exporting a submission-ready file — all rendered live in your browser, no server-side processing of your manuscript required.

No build step. No framework. One `index.html` file, a Supabase backend for the parts that need one (accounts, cloud sync, storage), and a handful of free public APIs doing the heavy lifting.

## 🚀 Features

### 📝 Manuscript formatting
- Upload `.docx`, `.pdf`, or `.txt`, or paste text directly
- Automatic section detection (Abstract, Introduction, Methods, Results, etc.) with manual override
- Author & co-author metadata extraction, with gaps flagged for you to fill in
- One-click reformatting into **IEEE / Springer / Elsevier / ACM / Nature** layouts
- Drag-and-drop figures with single/two-column layout and captions
- Fully editable structure blocks — nothing is locked once it's detected

### 🔎 Citations & readiness
- Live citation verification against **CrossRef**, with missing DOIs auto-resolved
- Verified / Flagged / Unverified status badges per reference
- A submission-readiness checklist: abstract length, missing sections, figure/reference counts, author completeness

### 📚 Publisher Guidelines
- A built-in guide per publisher: estimated review-to-publish timelines, a step-by-step submission roadmap, and a requirements checklist (abstract limits, reference style, figure resolution)

### 🧭 Topic discovery
- Browse Field → Subfield → Topic via the free **OpenAlex** API to see real related papers, then generate a structured (empty) section outline in your target journal's format — a starting skeleton, not written content

### 🤖 Writing Assistant
- Instant readability scoring (Flesch reading ease & grade level), average sentence length, and a passive-voice heuristic — computed entirely client-side
- Optional grammar & style check via the free **LanguageTool** API (only runs when you click it)
- Optional **AI Feedback** — an LLM comments on clarity, structure, and tone in what you've already written, without rewriting or drafting content for you (see [note below](#-a-note-on-the-ai-features))

### 🔐 Accounts, sync & history
- Email-based auth via Supabase (sign up, log in, forgot/reset password, all with proper validation and password-visibility toggles) — no phone/OTP anywhere
- Guest mode for trying the tool without an account
- Auto-saving drafts, synced to the cloud for logged-in users, with figures uploaded to Supabase Storage rather than bloating the database
- **Work History** — automatic checkpoints of your draft that you can browse and restore

### 💬 VidyaAI Assistant
- A floating help widget with a curated library of preset Q&A covering every part of the workflow, plus free-text fallback

## 🧠 A note on the AI features

ScholarAI's AI-assisted tools are built around one rule: **they critique what you've written — they don't write it for you.** The topic-discovery tool generates an empty outline, not paper content. The Writing Assistant flags issues and describes what kind of change would help, but won't produce replacement sentences you can paste in wholesale. This is a deliberate boundary, not a limitation of the tooling.

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML / CSS / JavaScript — no framework, no build step |
| Backend | [Supabase](https://supabase.com) — Auth, Postgres, Storage, Edge Functions |
| Document parsing | [mammoth.js](https://github.com/mwilliamson/mammoth.js) (`.docx`), [pdf.js](https://mozilla.github.io/pdf.js/) (`.pdf`) |
| Export | [JSZip](https://stuk.github.io/jszip/) for real `.docx` generation |
| Citation data | [CrossRef REST API](https://www.crossref.org/documentation/retrieve-metadata/rest-api/) |
| Topic discovery | [OpenAlex API](https://openalex.org/) |
| Grammar checking | [LanguageTool API](https://languagetool.org/http-api/) |
| AI feedback | Google **Gemini** (free tier) with **Groq** (Llama 3.3) as an optional fallback |


## 🗺️ Possible next steps

- [ ] BibTeX / LaTeX export
- [ ] Private (signed-URL) figure storage as an alternative to the public bucket
- [ ] Server-side rate limiting on AI Feedback

## 🤝 Contributing

Issues and pull requests are welcome. If you're proposing a feature, please keep it in the spirit of the project above — tools that help students do their own work well, not tools that do the work for them.

## 📄 License

Distributed under the MIT License. See `LICENSE` for details (add one if it isn't there yet).

## 👤 Author

**©SK Graphics** — Sachin K. <div>
Built as a submission-formatting tool for students preparing academic papers.
</div>

<div>

⭐ If this helped you get a paper submitted, consider starring the repo.

</div>
