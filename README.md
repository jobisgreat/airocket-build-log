# AI Rocket — Build Log

Public build record for [airocket.pro](https://www.airocket.pro).

One founder in Waltham, Massachusetts, directing AI agents to build and run a business.
Each entry is a single self-contained HTML report for one working session: what shipped,
what broke, what it would have cost the traditional way.

## What is in an entry

- **Verified numbers** — line counts from `git log --numstat`, live HTTP checks, file counts.
  Anything labelled verified was measured, not estimated.
- **Estimated numbers** — developer hours and dollar comparisons, calculated at $150/hr.
  These are labelled as estimates everywhere they appear.
- **The failures.** Blocked steps, wrong turns and shipped mistakes are in the timeline
  alongside the wins. A log that only contains wins is marketing, not a record.

## Entries

| Date | Entry |
|---|---|
| 2026-09-14 | [The build log went public](reports/2026-09-14-build-log-went-public.html) — this repository, the redaction pipeline that nearly published its own blocklist, and a custom domain |
| 2026-09-14 | [The SEO pack shipped](reports/2026-09-14-seo-pack-shipped.html) — /pilot from 404 to live, eleven articles published, 26 URLs in the sitemap |

## Code released

| Project | What it is | URL |
|---|---|---|
| [zero-dep-markdown](https://github.com/jobisgreat/zero-dep-markdown) | The markdown renderer behind the articles on airocket.pro. One file, no dependencies, MIT. | https://github.com/jobisgreat/zero-dep-markdown |

## How these are produced

Reports are generated from a structured data file, then put through three gates before
anything is published here:

1. **Derive.** A public variant is built from the internal session record — client work,
   contract terms and contact routing are dropped rather than reworded.
2. **Seal.** Every external resource is inlined, so a report renders offline in any viewer
   with no CDN, font or tracking requests.
3. **Scrub.** A checker reads the rendered text of the sealed file and refuses the push if
   any blocked term survives. Exit 0 means safe to publish; exit 1 means do not.

The internal data file and the tooling both stay out of this repository — the checker's own
rule list names the terms it exists to catch. See `.gitignore`.

## Reading the reports

Each file is a single HTML document with no external dependencies. Open it directly,
or browse the published version if GitHub Pages is enabled on this repository.

---

AI Rocket · 681 Main Street, Waltham, MA 02451 · hello@airocket.pro
Serving Waltham, Newton, Boston & Greater Boston.
