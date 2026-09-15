# GitHub profile agent runbook

This file holds procedures and evidence removed from the always-loaded guides on 2026-09-15. It is an agent
record, not a documentation site.

## Link verification

Before a README URL is committed, probe links sequentially with a delay:

```bash
grep -oE 'https?://[^)"| ]+' README.md | sed 's/[.,)]*$//' | sort -u |
  while read -r u; do
    sleep 0.45
    printf '%-6s %s\n' "$(curl -s -o /dev/null -w '%{http_code}' -m 25 -L \
      -A 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7)' "$u")" "$u"
  done
```

Parallel bursts produced false 000 responses in the 2026-07-25 audit; five apparent failures returned 200
when retried sequentially. A 404 or repeatable 000 means omit the link. A 403 or 999 can be anti-bot behavior
on npm, Upwork, or LinkedIn and requires host-appropriate verification rather than automatic deletion.

npmjs.com rejects non-browser clients, so verify package existence at
`https://registry.npmjs.org/<package>`. A Play Store 404 means the app is not publicly listed, even when an
internal or closed test exists. Project data files are leads, not proof: the 2026 sweep found two dead docs
URLs and eight Play URLs returning 404.

Repository URLs require `gh repo view aoneahsan/<repo> --json visibility`. The 2026-07-25 public set was
strata-storage, macleanup, linux-cleanup, and sysscope; current probe evidence wins.

## README structure

README.md is the profile landing page. Every heading after H1 carries an explicit anchor and visible
permalink, and the TOC reflects its H2 headings. Projects are grouped under six H3 headings. Each uses one
`details` block whose summary contains a referenced SVG logo, product name, and short description. The body
has exactly five factual product bullets, a row of verified distribution links, and one CTA to the main link.

Distribution belongs only in link rows. Keeping store claims out of prose prevents an unlisted channel from
contradicting the description. Header totals are derived from current blocks and links, never this record.
The 2026-07-25 snapshot was 23 products, 20 web links, 8 Play links, 4 extension listings, 5 npm links, and
16 docs sites.

## Logo and banner procedure

GitHub strips inline SVG from Markdown. Reference committed files as an img under `assets/logos/`, with an
empty decorative alt when the adjacent product name supplies the label. Each file uses
`viewBox="0 0 96 96"`. The source of truth is the matching portfolio-info file's
`Logo (SVG — inline)` block in the notebook. Re-extract, parse as XML, and remove unused assets.

Contribution banners remain light/dark SVG siblings. README switches them with `picture` and
`source media="(prefers-color-scheme: dark)"`; no JavaScript is needed.

## Bio propagation

BIO.md stores the 160-character GitHub bio options, GitHub profile fields, and longer variants for ORCID,
LinkedIn, npm, and the portfolio. Update facts there first, then propagate through each surface's approved
workflow. Do not edit a remote surface in isolation.

Measure fenced text lengths when the file states a count:

```bash
python3 -c "import re; print([len(b) for b in re.findall(r'```text\n(.*?)\n```', open('BIO.md').read(), re.S)])"
```

The 2026 sweep found the former YouTube handle `@ZaionsOfficial` returning 404. Profile links therefore
receive the same periodic probe as product links.

## Portfolio-info refresh

Keep one current `GITHUB-PROFILE_portfolio-info_YYYY-MM-DD.md`, refresh weekly with a three-day skip floor,
and retain at most ten history records. Required sections are Identity and Distribution, inline SVG logo,
palette, update history, vision/mission, best features, hidden facts, resume bullets, social angles, SEO
keywords, and hashtags.

Copy the refreshed record to the notebook's
`static/assets/personal/projects-info-as-portfolio-item/apps/` directory and remove the prior dated record
in both locations. The former guide named a macOS tracker path
`/Users/pc/Documents/ahsan-work/code/docs/tracking/portfolio-info-files-update-tracker.json`; on this Linux
machine, resolve the current workspace tracker before writing instead of copying that stale absolute path.

## ORCID and BibTeX

ORCID identifier `0009-0006-2311-8687` lists the showcased projects as works. The notebook keeps one
`<slug>.bib` per project and `aoneahsan-all-works.bib` for combined import. Regenerate from source facts
and freshly verified public URLs. Invoke `aoneahsan-cccs-orcid-profile` and `aoneahsan-cccs-bibtex` for
that task. Never invent a DOI or retain a channel omitted from the README as dead.

## Context history

The guide pair measured 7,782 bytes each before the 2026-09-15 optimization. The rewrite retained public
safety, README structure, bio/asset authority, and maintenance gates while placing commands and historical
evidence here. Routine re-optimization is next eligible on 2026-10-15.

## Preserved source anchors

These exact anchors from the former router remain searchable for maintenance and migration:

```text
<a id="…">
<details>
<summary>
<img>
<img src="./assets/logos/<slug>.svg" width="18" align="top" alt="">
<picture>
<source media="(prefers-color-scheme: dark)">
<svg>
<project>-docs
static/CNAME
assets/logos/*.svg
### Logo (SVG — inline)
PROJECT-LINKS-IDENTIFIERS-CONTACT.json
~/.claude/rules/docs-sites.md
aoneahsan-cccs-copywriting
aoneahsan-cccs-markdown
https://orcid.org/0009-0006-2311-8687
https://registry.npmjs.org/<pkg>
~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/orcid-project-projects-files/
~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/projects-info-as-portfolio-item/
~/Documents/ahsan-work/ahsan-notebook/static/assets/personal/projects-info-as-portfolio-item/apps/
```

The former character-count command, preserved verbatim:
`python3 -c "import re;print([len(b) for b in re.findall(r'\`\`\`text\n(.*?)\n\`\`\`',open('BIO.md').read(),re.S)])"`.
