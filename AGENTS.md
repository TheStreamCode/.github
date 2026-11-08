# Repository Instructions

These instructions apply to the entire repository.

## Purpose

This repository provides the default community health files for repositories owned by
[TheStreamCode](https://github.com/TheStreamCode) and documents the [repository standard](STANDARDS.md).

- `STANDARDS.md` is the contract. Every rule change belongs there first.
- `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md` and `SUPPORT.md` are the inherited defaults
  for repositories that do not ship their own copy.
- `FUNDING.yml` provides the default sponsor button.

## Invariants

- Keep the public wording English, sentence case, second person, active voice. No emoji, no
  exclamation marks, no promotional superlatives.
- Keep `STANDARDS.md` internally consistent: a rule must not contradict another rule or a file in
  this repository.
- Do not add repository-specific rules here. Product-specific behavior belongs in that product's
  `AGENTS.md`.
- Changes to `STANDARDS.md` that require work in other repositories must say so in the pull request.

## Validation

```powershell
npx --yes markdownlint-cli2 "**/*.md"
```

CI runs the same command. Do not weaken the Markdown rules to make a change pass.

## Change boundaries

- Do not commit, push, tag or change GitHub settings unless the user explicitly authorizes it.
- Do not add AI-attribution or generated-by footers to commits, pull requests or documentation.
