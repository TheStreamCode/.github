# Repository standard

The rules every public repository owned by [TheStreamCode](https://github.com/TheStreamCode)
follows. Repositories evolve independently but share this contract so they look and behave the same.

## Identity

- Legal holder: **Michael Gasperini**. Trade name: **Mikesoft**.
- Canonical copyright line: `Copyright (c) 2026 Michael Gasperini (Mikesoft)`.
- README footer: `Maintained by Michael Gasperini (Mikesoft).`
- Contact: <michael@mikesoft.it>. Studio: [mikesoft.it](https://mikesoft.it).

## Documentation language

English (US) for every repository file: README, docs, CONTRIBUTING, SECURITY, SUPPORT, CHANGELOG,
code comments and release notes. Sentence case for headings, second person for instructions, active
voice. No emoji, no exclamation marks, no promotional superlatives, no internal process narration in
public files.

## Required files

| File | Purpose |
| --- | --- |
| `README.md` | Product overview, install, quick start, configuration, development, support |
| `LICENSE` | SPDX license with canonical text |
| `CHANGELOG.md` | Keep a Changelog format, newest first, user-facing wording |
| `CONTRIBUTING.md` | How to report, propose and validate a change |
| `CODE_OF_CONDUCT.md` | Contributor Covenant 2.1 |
| `SECURITY.md` | Supported versions and private vulnerability reporting |
| `SUPPORT.md` | Where to ask for help and what support covers |
| `AGENTS.md` | Instructions for coding agents working in the repository |
| `.editorconfig`, `.gitattributes`, `.gitignore` | Baseline repository hygiene |
| `.github/CODEOWNERS` | `* @TheStreamCode` |
| `.github/FUNDING.yml` | Sponsor button |
| `.github/dependabot.yml` | Grouped dependency updates |
| `.github/PULL_REQUEST_TEMPLATE.md` | Change, verification, checklist |
| `.github/ISSUE_TEMPLATE/` | Bug report and feature request forms |
| `.github/workflows/ci.yml` | Lint, typecheck and tests |

Add `CITATION.cff` for citable tools, `NOTICE`/`THIRD-PARTY-NOTICES` where licensing requires it,
and `TRADEMARKS.md` for integrations with third-party products.

WordPress.org plugins keep `readme.txt` and `changelog.txt` as the changelog of record, because the
plugin directory reads them; `CHANGELOG.md` is optional there.

## README structure

1. Product name and one-sentence tagline.
2. Badges: CI, license, distribution.
3. Optional hero image with alt text.
4. Summary paragraph and, where relevant, an independent/unofficial note.
5. `Install`, `Quick start`.
6. `Features` (at most 8 factual bullets).
7. `Requirements` / `Compatibility`.
8. `Configuration` table.
9. `Privacy and security`.
10. `Troubleshooting` (3–5 real failure modes).
11. `Development` (clone, install from the lockfile, checks).
12. `Support`, `Contributing`, `License`.
13. Footer with the maintainer identity.

Length: up to 1,200 words for applications, extensions and plugins; up to 2,500 for platform or
research projects. Longer material goes to `docs/`.

## Repository metadata

- Description: at most 160 characters, sentence case, no trailing period, states the product and its
  audience.
- Topics: 8 to 20 lowercase kebab-case topics, always including `mikesoft`.
- Homepage: the primary distribution surface (marketplace, package registry, product site).
- Social preview: keep the GitHub default (account avatar plus repository name). Do not upload a
  custom image.

## GitHub settings

- Default branch `main`; Issues enabled; Discussions enabled for product repositories; Wiki and
  Projects disabled.
- Squash-only merges, auto-merge enabled, branches deleted after merge.
- Branch protection on `main`: pull request required, required CI checks, conversation resolution,
  linear history, no force pushes, no branch deletion.
- Secret scanning with push protection, Dependabot alerts and security updates, CodeQL where the
  language is supported.
- Release workflow permissions are declared explicitly and default to read-only.

## Releases

Semantic versioning with `vX.Y.Z` tags. Every tag has a GitHub release with highlights and change
sections. Version bumps update the manifest, `CHANGELOG.md` and `CITATION.cff` together. Release
artifacts are built from the tagged commit by CI.

## Commits and pull requests

Conventional Commits (`type(scope): summary`, imperative mood, English). One logical change per
commit. Pull requests state the problem, the change and the verification performed.
