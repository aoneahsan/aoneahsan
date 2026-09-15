# GitHub profile repository

**Last updated:** 2026-09-15. This public special repository is aoneahsan/aoneahsan; README.md renders at
https://github.com/aoneahsan. Claude Code reads CLAUDE.md; other agents read AGENTS.md. Read one native guide
only and keep their rules equivalent.

## Safety and scope

Everything committed here is permanently public. Never add secrets, .env files, private paths, private
repository links, or sensitive owner data. The repository has no dependencies or build: it is Markdown and
SVG. Preserve unrelated changes and stage only task-owned paths.

## README contract

- Every URL in README.md must receive a fresh sequential probe before commit. Omit genuine 404/000 results.
  Distinguish anti-bot 403/999 responses; verify npm packages through registry.npmjs.org. The probe procedure
  and known host behavior are in [docs/AGENT-RUNBOOK.md](docs/AGENT-RUNBOOK.md#link-verification).
- Public Markdown follows the heading-anchor contract: each heading below H1 gets an explicit HTML anchor and
  visible permalink; the table of contents matches the H2 set.
- Use one details block per project under six H3 groups. Its summary is logo, name, and a description of about
  90 characters or fewer. Its body has exactly five factual bullets, a verified-channel link row, and one CTA.
- Bullets explain what the product does; distribution appears only in the link row.
- Copy is factual, unhyped, and sourced from the product's portfolio-info record. Never fabricate numbers.
- Recompute header counts whenever a channel changes. A repository link ships only after gh confirms public
  visibility; recheck current state instead of preserving the historical set.

## Assets and bio

Each project details block references assets/logos/<slug>.svg as an img. GitHub strips inline SVG. Keep a
96-by-96 viewBox, parse every asset as XML, and delete unreferenced logos. Re-extract from the project's
portfolio-info Logo block instead of hand-editing.

BIO.md is the canonical home for GitHub fields and the approximately 50-, 120-, and 250-word bio variants.
Edit it first, then propagate only through the applicable approved workflow. Every claim must resolve to its
facts table. Measure stated character counts; do not estimate. Counts shared with README.md change together.
Probe social URLs on refresh.

## External records

This profile has no docs product and never gets a project-docs sibling, CNAME, Pages workflow, or Docusaurus
site. The local docs/ directory contains agent records only.

ORCID/BibTeX works and the dated portfolio-info record are maintained through the sourced procedures in
[docs/AGENT-RUNBOOK.md](docs/AGENT-RUNBOOK.md#portfolio-info-refresh). Never invent a URL or DOI; README and
BibTeX omit the same dead channel.

## Context optimization record

| Field | Value |
|---|---|
| Last optimized | 2026-09-15 |
| Next routine optimization eligible | 2026-10-15 |
| Guide bytes | 3,658 B |
| Covered subtree | Entire aoneahsan-github-profile repository |
| Method | Public-safety and content contracts retained; probe evidence and maintenance detail moved on demand |
| Fleet record | /home/ahsan/Documents/01-code/docs/tracking/project-context-budget-tracker.json |

During the 30-day cooldown, do not begin another general context pass. Active feature work may make its
smallest required guide change; proven pointer, mirror, record, or cap regressions may be repaired and
recorded centrally.

## Before handoff

Validate SVG as XML, verify URLs sequentially, recalculate counts, check anchors, and run git diff --check.
Keep light/dark SVG banners synchronized without JavaScript. Follow inherited rules.
