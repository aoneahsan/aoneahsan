# GitHub Profile (aoneahsan) — Portfolio Info

Reference Date: 2026-07-25
Project Type: GitHub profile README repo — banner, project showcase, and contact directory at github.com/aoneahsan
Project Slug: github-profile
Primary Email Reference: aoneahsan@gmail.com
Last Portfolio Update: 2026-07-25
Next Eligible Update After: 2026-08-01

---

## Identity & Distribution (Authoritative)

| Field | Value |
| --- | --- |
| Project Slug | `github-profile` |
| Public Brand Name | aoneahsan (GitHub Profile) |
| Public URL (Live) | https://github.com/aoneahsan |
| Repository | https://github.com/aoneahsan/aoneahsan (special profile repo, **public**) |
| Type | GitHub `username/username` profile repo (renders on the profile landing) |
| License | MIT |
| Author | Ahsan Mahmood — aoneahsan@gmail.com — https://aoneahsan.com |
| Contact (WhatsApp) | +923046619706 |
| LinkedIn | https://linkedin.com/in/aoneahsan |
| NPM | https://www.npmjs.com/~aoneahsan |
| ORCID | https://orcid.org/0009-0006-2311-8687 |
| Resume | https://aoneahsan.com/resume |
| CV | https://aoneahsan.com/cv |
| Skype | `live:aoneahsan` |
| Docs site | **None, by rule.** This is a profile README, not a product — `rules/docs-sites.md` does not apply. |

---

## Brand Assets

### Logo (SVG — inline)

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 96 96" role="img" aria-label="aoneahsan GitHub Profile">
  <defs>
    <linearGradient id="ghp-grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0F172A"/>
      <stop offset="100%" stop-color="#22D3EE"/>
    </linearGradient>
  </defs>
  <rect x="2" y="2" width="92" height="92" rx="22" fill="url(#ghp-grad)"/>
  <path d="M48 16 a32 32 0 0 0 -10 62 v-8 c-12 2 -14 -8 -14 -8 c-2 -4 -4 -6 -4 -6 c-4 -2 0 -2 0 -2 c4 0 6 4 6 4 c4 6 10 4 12 4 c0 -4 2 -6 4 -8 c-10 -2 -20 -6 -20 -22 c0 -4 2 -8 4 -10 c0 -2 -2 -6 0 -12 c0 0 4 -2 12 4 c4 0 8 -2 12 -2 c4 0 8 0 12 2 c8 -6 12 -4 12 -4 c2 6 0 10 0 12 c2 2 4 6 4 10 c0 16 -10 20 -20 22 c2 2 4 4 4 8 v12 a32 32 0 0 0 -10 -62z" fill="#FFFFFF"/>
</svg>
```

### Color Palette

| Role | Token | Hex |
| --- | --- | --- |
| Primary | Slate 900 | `#0F172A` |
| Secondary | Cyan 400 | `#22D3EE` |
| Banner | Custom SVG (light + dark variants) | `contribution-banner-light.svg` / `contribution-banner-dark.svg` |
| Project marks | 23 per-project SVG logos | `assets/logos/<slug>.svg`, all `viewBox="0 0 96 96"` |

---

## Update History (max 10)

| Date | Type | Notes |
| --- | --- | --- |
| 2026-07-25 | **Major rebuild** | Turned the profile from generic positioning into a verified product showcase. Added **23 projects** as collapsible `<details>` blocks in six groups, each with a logo, a one-line description, exactly 5 factual bullets, a link row of verified channels, and one CTA. Added `assets/logos/` (24 SVG marks extracted from the portfolio-info corpus — GitHub strips inline `<svg>`, so they must be files). Added the anchor + TOC contract, a header badge row, and an ORCID link. **Every URL probe-verified: 68/74 returned 200; the 6 npm URLs 403 to bots but were confirmed live via `registry.npmjs.org`.** Honest omissions: 8 Play listings 404 and 19 of 23 repos are private, so those links are absent rather than dead. CLAUDE.md/AGENTS.md rewritten — fixed two stale Linux-machine paths, added the link-verification rule, README structure contract, logo-asset rule, the no-docs-site rule, and the ORCID pointer. |
| 2026-06-08 | Material refresh | Portfolio-refresh pass on the profile README. Tightened the intro copy, added a non-numeric "What I build" section, added the npm contact link to both the README contact list and this dossier's Identity table. Removed the dangling empty "Let's connect!" trailing header. |
| 2026-05-07 | Date refresh | No commits since 2026-04-30. State stable: profile README repo with light + dark SVG banners, tagline, contact directory. |
| 2026-04-30 | Created | First portfolio info file. Captured the GitHub profile README repo — landing banner (light + dark SVG), tagline, links to aoneahsan.com, LinkedIn, resume, CV. |

---

## One-Line Summary

The GitHub Profile repo is the public landing for `github.com/aoneahsan` — a theme-aware SVG banner, a header
badge row, and a showcase of **23 shipped products** as collapsible blocks (logo, one-liner, five bullets,
verified links, one call to action), followed by a full contact and profile directory.

## Elevator Pitch

This is the special `username/username` GitHub repo whose README renders directly on Ahsan's GitHub profile
landing page — the first and often only page a recruiter, client or package consumer sees. As of 2026-07-25 it
is no longer a business card: it is a catalogue of 23 products spanning web apps, Android apps, browser
extensions and npm packages, each with its own mark and its own verified distribution links. The discipline
that makes it trustworthy is that **no URL ships unverified** — every link is probe-checked before commit, and
a channel that does not resolve is omitted rather than shown as "coming soon".

## What This Project Is About

A profile landing repo with no build step: `README.md`, `assets/logos/*.svg`, and two contribution banners.
The README is generated from, and kept honest against, the portfolio-info corpus in the notebook plus live
HTTP probes.

## Vision

Make the first impression on GitHub do real work — show what has actually shipped, prove every link, and give
one obvious next click per product.

## Mission

- Render a clean, theme-aware banner and an accurate at-a-glance count line.
- Showcase every flagship product with a mark, an honest description, and its live channels.
- Never ship a dead link, and never claim a distribution channel that is not publicly reachable.
- Keep the contact directory and the ORCID record consistent with the portfolio at aoneahsan.com.

## Best Features

- **23 products as collapsible `<details>` blocks** — scannable as a list, full depth on demand, so a long
  catalogue does not become an endless scroll.
- **Every link probe-verified** before commit; the verification command lives in `CLAUDE.md`.
- **Per-project SVG marks** in `assets/logos/`, extracted from the same portfolio-info corpus that feeds the
  ORCID BibTeX entries, so branding stays consistent across surfaces.
- Light + dark SVG banner variants via `<picture>` + `prefers-color-scheme` — no JavaScript.
- Explicit heading anchors and a TOC, so any section is individually linkable.
- Honest count line (23 products · 20 web · 8 Play · 4 extension listings · 5 npm · 16 docs sites), recomputed
  whenever a link changes.

## Hidden Facts and High-Value Talking Points

- This is a **GitHub special repo** — `aoneahsan/aoneahsan` — recognized by GitHub to render its README on the
  profile landing page.
- **GitHub strips inline `<svg>` from markdown.** Logos must be committed files referenced by `<img>` — a
  detail that silently breaks profile READMEs that paste SVG directly.
- **A parallel link probe lies.** Probing 21 hosts at once returned five spurious `000`s; all five returned
  200 when probed sequentially. The rule is now "sequential, with a delay".
- **`npmjs.com` returns 403 to every non-browser client**, even with a browser user-agent — package existence
  must be confirmed through `registry.npmjs.org`, not the website.
- **A Play Store 404 means "not publicly listed"**, typically a closed testing track. The 2026-07-25 sweep
  found 8 such listings that project docs described as live.
- The same verified URL set feeds both this README and the ORCID BibTeX corpus, so the two can never disagree.

## Strong Resume Bullet Ideas

- Rebuilt a public GitHub profile landing (`aoneahsan/aoneahsan`) into a 23-product showcase with per-project
  SVG marks, collapsible detail blocks, and a link-verification gate that probe-checks every URL before commit.
- Established a documented honesty rule for public-facing links: a channel that does not return 200 is omitted
  rather than published, after an audit found 8 store listings and 19 repository links that would have 404'd.

## Social Post Angles

- The GitHub special-repo pattern — what `username/username` does that nothing else does.
- Why your profile README's inline `<svg>` never renders, and what to do instead.
- Auditing your own links before a recruiter does: what a probe sweep of 74 URLs actually found.
- Collapsible `<details>` blocks: how to show 23 projects without an endless scroll.
- Theme-aware banners with `<picture>` + `prefers-color-scheme`, no JavaScript.

## Suggested SEO Keywords

- aoneahsan GitHub profile
- Ahsan Mahmood GitHub
- Full-Stack Software Developer GitHub
- SaaS Specialist developer profile
- GitHub profile README project showcase

## Social Hashtags

### Generic
#Aoneahsan #AhsanMahmood #Zaions #BestOpenSourceCommunityProject #TopFree #SaaSApp

### Top 20
#GitHubProfile #DeveloperProfile #FullStackDeveloper #SaaSSpecialist #BuildInPublic #GitHub
#DeveloperBranding #PersonalBrand #ProfileReadme #AhsanMahmood #aoneahsan #Zaions #SoftwareDeveloper
#ProductEngineering #IndieDev #TechPortfolio #Recruiting #DeveloperJourney #OpenSource #ORCID

## Known Constraints

- Repo is decoration-only — no `package.json`, no build, no tests.
- Must stay **public** so GitHub renders the README on the profile landing — therefore no secrets, ever.
- Keep the two contribution-banner SVGs in place; they are part of the rendered profile.
- Only 4 of the 23 projects have a public repository, so most blocks carry no GitHub link. That is correct,
  not an omission to fix.

## Asks for next refresh

- **8 Play Store listings return 404** (habitforge, imtehanhub, taxease, slackvault, labflow,
  video-controls-plus, native-update, files-hub) while several project docs call them "live on Play Store".
  Confirm whether each is in a closed track or genuinely unpublished, then correct those project records.
- **Two docs URLs in `PROJECT-LINKS-IDENTIFIERS-CONTACT.json` do not resolve** — `native-update-docs`
  (live host is `nativeupdate-docs`) and `docs.labflow`. Left unedited this pass by owner choice.
- `labflow-docs.aoneahsan.com` resolves but returns 404 — the DNS record exists with nothing deployed.
- ShieldPro Ultimate has no docs site and no public store listing; only its marketing site is linked.

## File Usage Rule

Refresh weekly (MANDATORY); 3-day skip floor; max 10 history records. Filename always carries the last-updated
date. Final destination:
`~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/projects-info-as-portfolio-item/apps/GITHUB-PROFILE_portfolio-info_<YYYY-MM-DD>.md`
