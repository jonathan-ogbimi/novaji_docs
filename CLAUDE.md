# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project status

This repository is still a placeholder for the actual website — no application code, `composer.json`, or `package.json` has been committed yet.

It does, however, contain non-code business collateral used for content tasks (not part of the eventual website codebase):
- `novaji-logo.png`, `nipep-logo.png` — brand logos
- `MATRICS_Automated_AML_Solution.pdf`, `NiPEP_v2.pdf` — product one-pagers for the company's two products (MATRICS, an AML solution; NiPEP, a product in development)
- `Novaji_Profile_2026.pptx` — company profile/pitch deck
- `.tasks.md` — ad-hoc task briefs for content work (e.g. building the pitch deck); check it for current content-generation asks before assuming a task is code-related

## Purpose

Per `README.md`: this repo is intended to hold the website for novajii.com, to be built on **Winter CMS** (a Laravel-based CMS).

## What the .gitignore implies about the planned stack

The `.gitignore` is pre-configured for a Laravel/Winter CMS project (vendor/, node_modules/, storage paths, `.env`, `public/build`, `auth.json`, etc.), so when code is added it will likely follow standard Laravel conventions:
- PHP dependencies via Composer (`vendor/`, `composer.json`/`composer.lock`)
- Front-end assets via npm/yarn (`node_modules/`, `public/build`)
- Environment config in `.env` (not committed)
- Winter CMS plugin/theme structure once scaffolded

## Notes for future work

There are no build, lint, or test commands yet since no framework files exist. Once Winter CMS is installed, check `composer.json` and `package.json` for the actual scripts before assuming standard Laravel/Winter commands apply.
