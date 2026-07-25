# Bio

Canonical bio copy for Ahsan Mahmood, in every length a surface asks for. **One home:** change it here, then
propagate. Every fact below is verified — see [Facts this bio is built on](#facts).

**Last Updated:** 2026-07-25

- [📌 GitHub bio field](#github-bio-field)
- [🧭 The rest of the GitHub profile](#github-profile-fields)
- [📝 Longer bios for other surfaces](#longer-bios)
- [✅ Facts this bio is built on](#facts)
- [🔧 Maintenance](#maintenance)

<a id="github-bio-field"></a>
## 📌 GitHub bio field&nbsp;[#](#github-bio-field)

The short line under your avatar on <https://github.com/aoneahsan>. **Hard limit: 160 characters.**
Set it at **Settings → Public profile → Bio**.

### ✅ Recommended (152 chars)

```text
Full-stack developer. One React + TypeScript codebase becomes a web app, an Android app and a browser extension. 23 products shipped on zero-cost infra.
```

It leads with what you are, states the thing that is actually distinctive about how you build, and ends on a
concrete number — the emphatic position. No links: the website and social fields already carry those, so
spending bio characters on a URL wastes them.

### Alternatives

**Stack-forward (136)** — for recruiters scanning for keywords:

```text
Full-stack SaaS developer — React, TypeScript, Capacitor, Firebase, Laravel. Web, Android and browser extensions from a single codebase.
```

**Plain and human (140)** — least jargon, widest audience:

```text
Full-stack developer building SaaS products end to end: web apps, Android apps, browser extensions and open-source npm packages. Lahore, PK.
```

**Open-source-forward (141)** — if you want contributors, not clients:

```text
Full-stack developer. I build SaaS products and publish the pieces: strata-storage, native-update, macleanup, linux-cleanup, sysscope on npm.
```

> [!NOTE]
> Your current bio still lists **MongoDB and GraphQL**, which no longer appear in your stack, and spends 40
> characters repeating a link the profile already shows. Replacing it is the single highest-value edit here.

<a id="github-profile-fields"></a>
## 🧭 The rest of the GitHub profile&nbsp;[#](#github-profile-fields)

| Field | Set it to | Why |
|---|---|---|
| **Name** | `Ahsan Mahmood` | Already correct. |
| **Bio** | the recommended line above | Replaces the stale MongoDB/GraphQL text. |
| **Company** | `@Zaions` | The `@` makes it a link when the org exists; plain `Zaions` otherwise. |
| **Location** | `Lahore, Pakistan` | More useful to an international reader than `Lahore` alone. |
| **Website** | `https://aoneahsan.com` | Currently points at `/cv`. The homepage is the better landing — the CV is one click from it, and the README links `/cv` and `/resume` directly. |
| **Pronouns** | your choice | Optional; the field exists. |
| **Available for hire** | on | Already on. |

### Social accounts

| Provider | URL | Status |
|---|---|---|
| LinkedIn | `https://www.linkedin.com/in/aoneahsan/` | ✅ keep |
| npm | `https://www.npmjs.com/~aoneahsan` | ✅ keep |
| Upwork | `https://www.upwork.com/freelancers/aoneahsan` | ✅ keep |
| YouTube | `https://www.youtube.com/@aoneahsan` | ⚠️ **change this one** |
| ORCID | `https://orcid.org/0009-0006-2311-8687` | ➕ add if you want a fifth |

> [!WARNING]
> The YouTube link on your profile right now is **`@ZaionsOfficial`, which returns 404** — probed on
> 2026-07-25 across `@ZaionsOfficial`, `@zaionsofficial` and `/c/Zaions`, all dead. **`@aoneahsan` returns 200
> and is your channel.** Swap it; a dead link on the profile is the same defect the README was just cleaned of.

<a id="longer-bios"></a>
## 📝 Longer bios for other surfaces&nbsp;[#](#longer-bios)

### Short — ~50 words (ORCID biography, npm, speaker blurb, guest post)

> Ahsan Mahmood is a full-stack software developer based in Lahore, Pakistan, with six years of professional
> experience building SaaS products end to end. He ships web applications, Android apps, browser extensions
> and open-source npm packages — usually from a single React and TypeScript codebase, running on
> infrastructure that costs nothing to operate.

### Medium — ~120 words (LinkedIn About opener, portfolio intro, proposal header)

> I'm a full-stack software developer with six years of professional experience, building SaaS products end
> to end — from the data model and security rules through to the store listing.
>
> Most of what I ship follows one pattern: a single React and TypeScript codebase that becomes a web app, an
> Android app and a browser extension, running on infrastructure that costs nothing to operate. Where a
> product needs a backend it is Laravel or Cloudflare Workers; where it needs storage or transactional email
> it is FilesHub, which I built and run myself.
>
> Twenty-three products are live across the web, Google Play and the Chrome, Firefox and Edge extension
> stores, alongside five published npm packages. Based in Lahore, Pakistan, working remotely.

### Long — ~250 words (About page, detailed profile, agency bio)

> I'm Ahsan Mahmood, a full-stack software developer based in Lahore, Pakistan. Over six years I've built
> SaaS products end to end — data modelling and security rules, the interface, the mobile packaging, the
> store submission, and the documentation that has to exist afterwards.
>
> Most of what I ship follows one pattern: a single React and TypeScript codebase that becomes a web app, an
> Android app and a browser extension. Where a product needs a backend, it is Laravel or Cloudflare Workers;
> where it needs file storage or transactional email, it is FilesHub, a platform I built and operate. The
> constraint I work under deliberately is that a product should cost nothing to run — free-tier Firebase or
> Supabase, client-side processing wherever the work can happen in the browser, and no paid service in the
> critical path.
>
> That range covers twenty-three live products: hiring and health platforms, a laboratory information
> system, a link-management SaaS, exam preparation, tax compliance, a Slack archiver, developer toolboxes,
> and command-line utilities. Five are published npm packages, four of them open source — including
> `strata-storage`, one storage API spanning localStorage, IndexedDB, SQLite, Keychain and the filesystem,
> and `native-update`, over-the-air updates for Capacitor apps.
>
> I also work in Flutter and Tauri, and I care about the parts that usually get skipped: honest store
> listings, documentation someone can actually follow, and links that resolve. My portfolio is at
> aoneahsan.com and my published works are on ORCID under 0009-0006-2311-8687.

<a id="facts"></a>
## ✅ Facts this bio is built on&nbsp;[#](#facts)

Verified 2026-07-25. Nothing above is estimated or rounded up.

| Claim | Source |
|---|---|
| 23 live products | `README.md` — each with a probe-verified link |
| 20 web apps · 8 Google Play · 4 extension listings · 5 npm packages · 16 docs sites | sequential HTTP probe, 68/74 URLs returned 200; the 6 npm URLs 403 to bots and were confirmed via `registry.npmjs.org` |
| 4 open-source packages | `strata-storage`, `macleanup`, `linux-cleanup`, `sysscope` — the only public repos of the 23 |
| Six years professional experience | owner-stated, carried from the previous README |
| Lahore, Pakistan; remote worldwide | GitHub `location` field + aoneahsan.com/address |
| Company: Zaions | GitHub `company` field |
| GitHub member since March 2018 | `users/aoneahsan.created_at` |
| ORCID 0009-0006-2311-8687 | the works corpus in the notebook |

**Deliberately not claimed:** follower or star counts, download numbers, client names, "best/leading/#1"
framing, or any certification. A bio that can be checked is worth more than one that impresses.

<a id="maintenance"></a>
## 🔧 Maintenance&nbsp;[#](#maintenance)

- **This file is the single home.** GitHub, LinkedIn, ORCID, npm and the portfolio all draw from it; edit here
  first, then propagate, so the surfaces cannot drift apart.
- **Re-verify the counts whenever a product ships or a link changes** — they appear in both the bio and the
  README header line, and a stale number is the easiest thing on the page to disprove.
- **Probe the social URLs at each weekly portfolio refresh.** The YouTube link went dead without anyone
  noticing; profile links rot silently because nobody clicks their own.
- Keep every length in sync: a change of substance belongs in all four, not just the one you happened to open.
