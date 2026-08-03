# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project status

There is no application code in this repository — no `composer.json`, `package.json`, `.gitignore`, or framework files exist. This is currently a **content/collateral repo** for Novaji Introserve Ltd., not a codebase. There are no build, lint, or test commands because there is nothing to build.

Tasks here are almost always content or document tasks (editing/generating copy, restructuring a deck, extracting text from a PDF), not software engineering tasks — read the actual request carefully before assuming it wants code.

## What's in the repo

- `novaji-logo.png`, `nipep-logo.png` — brand logos (Novaji Introserve; NiPEP sub-brand)
- `MATRICS_Automated_AML_Solution.pdf` — one-pager for MATRICS, a risk-based AML & transaction-monitoring / anti-fraud platform for financial institutions
- `NiPEP_v2.pdf` — one-pager/deck for NiPEP, a cloud-based RESTful API web service for screening Nigerian Politically Exposed Persons (PEPs)
- `Novaji_Profile_2026.pptx` — general company profile deck (services: VAS/USSD, mobile financial services, digital content monetization, enterprise/ERP solutions, systems integration)
- `Novaji_Investor_Pitch_Deck_2026.pptx` — investor-facing pitch deck, framed around "Building the Compliance & RegTech Infrastructure for African Financial Institutions" (novajii.com)
- `README.md` — currently just the repo title; carries no project description

Every binary file above has a matching `<filename>:Zone.Identifier` file tracked in git. These are Windows/WSL alternate-data-stream artifacts left over from downloading the files, not real content — don't treat them as documents to read or edit, and don't "clean them up" without checking with the user first since they're already committed history.

## Working with the PDFs/PPTX files

These are binary office documents, not text you can `Read` directly:
- Extract text with `pdftotext` (e.g. `pdftotext file.pdf -`) for the PDFs.
- PPTX files are zip archives; slide text lives in `ppt/slides/slideN.xml` and can be pulled out with `unzip -p file.pptx ppt/slides/slide1.xml | grep -o '<a:t>[^<]*</a:t>'`.

There is no source-of-truth text version of these decks/one-pagers in the repo — the PDF/PPTX *is* the document.
