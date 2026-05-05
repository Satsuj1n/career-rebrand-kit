# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Career Rebrand Kit — a **content kit**, not a code project. The artifacts are markdown files (`linkedin/`, `github/`, `strategy/`) plus banner assets (`banner/banner.svg`, `banner/banner.png`). There is no build, no test suite, no linter, no package manager. The "deliverable" is text the user copy-pastes into LinkedIn / GitHub.

The kit is also a **case study**: the published versions on `main` are the actual content the original author applied to his own LinkedIn. Don't treat the prose as a draft to "improve" — the wording is intentional (anti-corporate, opinionated, calibrated for international AI/agent recruiters). Edit only when the user explicitly asks.

## Two-branch model — important

- `main` — case study with the original author's real personal data (name, email, GitHub handle, LinkedIn slug, project names like Cosmic Trader and Claude Code Toolkit). This is the public reference version.
- `template` — same files with personal data replaced by `[YOUR_NAME]`, `[YOUR_EMAIL]`, `[YOUR_GITHUB]`, `[YOUR_LINKEDIN_SLUG]`, `[YOUR_PROJECT_1]`, `[YOUR_PROJECT_2]`. Forks should branch from here.

Never push placeholder strings into `main` and never push real personal data into `template`. If the user asks to update content, ask which branch the change belongs to. Default branch is `main`.

## The operational asset: `linkedin/audit-prompt-claude-code.md`

This file is **not documentation** — it's a runnable prompt. It instructs an agent (Claude Code with a browser MCP — Playwright MCP or chrome-devtools-mcp) to audit and update the user's LinkedIn profile in two phases (read-only audit, then per-section apply with explicit approval gates). The hard rules in that file (no connections, no posts, no deletions, stop on captcha, English-only changes, one section per approval) are non-negotiable.

When the user asks to "run the audit" or "update my LinkedIn", the workflow lives in this prompt. Read it before acting. The prompt expects audit artifacts saved to `~/linkedin-audit/` (timestamped `audit-current-*.md` and `applied-*.md`), outside the repo working tree.

## The only "build" command

Regenerating `banner/banner.png` from `banner/banner.svg` after editing colors:

```bash
pip install cairosvg
python3 -c "import cairosvg; cairosvg.svg2png(url='banner/banner.svg', write_to='banner/banner.png', output_width=1584, output_height=396)"
```

1584×396 is the LinkedIn banner spec — don't change.

## Conventions

- Files are bilingual on purpose: README/SETUP narrative is in PT-BR (audience is Brazilian devs), but the LinkedIn/GitHub content (`linkedin/about.md`, `github/profile-readme.md`, etc.) is in EN because the audience for *those* outputs is international recruiters. Don't translate either direction without asking.
- The kit's anti-checklist (`SETUP.md` §3) bans words like "passionate", "results-driven", "team player" in About content — and bans "30-skills laundry lists". Honor this when proposing edits.
- License is MIT but the README explicitly forbids reselling as a paid kit.

## When working with this repo

- Don't add tooling (CI, linters, formatters, package.json) — the kit is intentionally minimal markdown. Adding scaffolding turns a content kit into a project.
- Don't "improve" prose unprompted. If you spot something off, surface it; don't rewrite.
- For LinkedIn automation: see memory `feedback_linkedin_automation_pacing.md` and `feedback_chrome_devtools_mcp_quirks.md` — there are session-specific gotchas (React `_valueTracker` bypassing `fill`, services-add API hangs after ~10 saves) that bit hard during the first audit run.
