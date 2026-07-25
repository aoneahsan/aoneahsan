# GitHub Profile (aoneahsan/aoneahsan) — CLAUDE.md

Mirror of **`AGENTS.md`** — the two files are byte-identical except this header. Change one, change both.

**Last Updated**: 2026-07-25

## What this repo is

The GitHub **special repo** `aoneahsan/aoneahsan`. Its `README.md` renders as the profile landing page at
**<https://github.com/aoneahsan>** — for most visitors it is the first and only page they see.

- **The repo is PUBLIC.** Everything here is world-readable, permanently. No secrets, no `.env`, no private
  paths that reveal anything sensitive.
- Contents: `README.md`, `assets/logos/*.svg` (23 project marks), and the two contribution banners.
- There is no build step and no dependencies — it is markdown plus SVG.

## 🔴 Link verification — no URL ships unverified (IRON-SOLID)

**Every URL in `README.md` must return 200/301 on a fresh probe before it is committed.** A dead link on the
profile landing page is visible to every recruiter, client and package consumer who looks you up.

```bash
grep -oE 'https?://[^)"| ]+' README.md | sed 's/[.,)]*$//' | sort -u |
  while read -r u; do sleep 0.45
    printf '%-6s %s\n' "$(curl -s -o /dev/null -w '%{http_code}' -m 25 -L \
      -A 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7)' "$u")" "$u"; done
```

Rules learned from the 2026-07-25 sweep — do not re-learn them the hard way:

| Rule | Why |
|---|---|
| **Probe sequentially with a delay.** | A parallel burst returns spurious `000`s. Five hosts "failed" on the first pass and all returned 200 when probed one at a time. |
| **A `404`/`000` means OMIT the link** — never "coming soon", never ship it anyway. | Owner decision 2026-07-25. |
| **The probe beats the data file.** | `PROJECT-LINKS-IDENTIFIERS-CONTACT.json` carried two docs URLs that do not resolve, and 8 Play URLs that 404. |
| **`npmjs.com` 403s every non-browser client** (Cloudflare, even with a browser UA). | Verify packages through `https://registry.npmjs.org/<pkg>` instead — a 403 here is not a broken link. |
| **Play Store 404 = not publicly listed.** | A closed/internal testing track returns 404. Several projects' own docs call these "live on Play Store"; they are not. |
| **Only 4 repos are public** — `strata-storage`, `macleanup`, `linux-cleanup`, `sysscope`. | Every other repo link would 404. Confirm with `gh repo view aoneahsan/<repo> --json visibility`. |

## README structure contract

- **Public file** → it carries the anchor + TOC contract from `aoneahsan-cccs-markdown`: every heading below
  the H1 gets an explicit `<a id="…">` and a visible `[#](#…)` permalink; the TOC is built from the H2 set.
- **One `<details>` block per project**, grouped under six H3 headings. `<summary>` = logo `<img>` + name +
  a one-line description (≤ ~90 chars). Body = **exactly 5 factual bullets**, a link row of *verified* channels,
  and **one** CTA to that project's main link.
- **Bullets describe what the product does, never where it is distributed.** Distribution is conveyed solely
  by the link row, so an unlisted store can never contradict the copy.
- Copy follows `aoneahsan-cccs-copywriting`: no hype, no banned words, no fabricated numbers. Figures come
  from the project's own portfolio-info file.
- **Counts in the header must be recomputed** whenever a link is added or removed (currently: 23 products ·
  20 web · 8 Play · 4 extension listings · 5 npm · 16 docs sites).

## Logo assets

`assets/logos/<slug>.svg` — 23 project marks, one per `<details>` block. Every file must be referenced by the
README; an unreferenced asset is deleted, not kept "just in case" (it re-extracts in seconds).

- **GitHub strips inline `<svg>` from markdown.** Logos must be committed files referenced with
  `<img src="./assets/logos/<slug>.svg" width="18" align="top" alt="">`. Never paste raw SVG into the README.
- Source of truth is each project's portfolio-info file (`### Logo (SVG — inline)` block) in the notebook at
  `~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/projects-info-as-portfolio-item/`.
- All share `viewBox="0 0 96 96"`, so they render as a uniform row. Re-extract from the portfolio-info file
  rather than hand-editing, and re-validate that each parses as XML.

## No docs site — ever

This repo is a profile README, not a product. **`~/.claude/rules/docs-sites.md` does not apply.** Never create
a `<project>-docs` sibling, a `static/CNAME`, a Pages workflow, or a Docusaurus site for it.

## ORCID / BibTeX record

<!-- RULE:orcid-bibtex v2026-07-25 -->
The 23 projects showcased in this README are also published as works on ORCID
**[0009-0006-2311-8687](https://orcid.org/0009-0006-2311-8687)**. Their BibTeX entries live at
`~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/orcid-project-projects-files/` — one
`<slug>.bib` per project plus a combined `aoneahsan-all-works.bib` for a single import.

On *"update ORCID profile info"*: regenerate the affected `.bib` files from each project's portfolio-info file
and its **probe-verified** live URLs, refresh the combined file, and invoke `aoneahsan-cccs-orcid-profile` +
`aoneahsan-cccs-bibtex`. Never invent a URL or a DOI. The URLs in the `.bib` corpus and the URLs in this
README are the same set — if one omits a channel as dead, so does the other.

## Portfolio info file — weekly update rule (IRON-SOLID)

- Maintain ONE dated portfolio info file: `GITHUB-PROFILE_portfolio-info_YYYY-MM-DD.md`.
- Refresh weekly (mandatory); 3-day skip floor; keep at most 10 history records.
- Required blocks: Identity & Distribution, inline SVG logo, palette, Update History, Vision/Mission, Best
  Features, Hidden Facts, Resume bullets, Social angles, SEO keywords, Hashtags.
- After refreshing, copy it to
  `~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/projects-info-as-portfolio-item/apps/`
  and delete the previous-dated version in both places.
- Tracker: `/Users/pc/Documents/ahsan-work/code/docs/tracking/portfolio-info-files-update-tracker.json`.

## Maintenance

- Banners are SVG — keep the light and dark variants in sync. Theme switching uses `<picture>` +
  `<source media="(prefers-color-scheme: dark)">`, no JavaScript.
- Update contact links in `README.md` if any contact channel changes.
- Re-run the link sweep before every commit that touches a URL, and at least at each weekly refresh.
