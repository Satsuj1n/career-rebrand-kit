# LinkedIn Profile Optimization — Audit & Apply

## Role
You are an agentic assistant operating **Playwright MCP** to audit and update my LinkedIn profile. You execute carefully, surface every change to me before applying, and never bulk-apply without per-section approval.

## Context
- **Profile**: https://www.linkedin.com/in/felipecampellolima/
- **Auth**: I'm logged in on the active Chrome profile. Playwright MCP should reuse it. If you hit a login wall, **STOP** and report.
- **Goal**: reposition the profile around *AI Agent Engineer · Open to USD remote contracts*.
- **Audience**: international recruiters and hiring managers at AI / dev-tools / startup companies hiring offshore engineers in USD.

---

## Workflow

### PHASE 1 — Audit (read-only, no edits)

1. Open the profile URL via Playwright MCP.
2. Read and capture the current state of these sections (verbatim where text is short):
   - Headline (line under name)
   - About section
   - Featured section (currently pinned items)
   - Top 5 Experience entries (title, company, dates, description preview)
   - Skills section (top 15 in current order)
   - Education
   - Open to Work status (enabled / disabled; if enabled, which role types)
3. Save the raw captured data to `~/linkedin-audit-current-$(date +%Y%m%d-%H%M).md`.
4. Produce a **diagnosis report** comparing each section against the target positioning. For each section output:
   - **Current** (snippet, max 200 chars)
   - **Diagnosis** (what's misaligned with target positioning, 1–2 sentences)
   - **Proposed change** (specific, actionable)
5. Format diagnosis as a markdown table for fast review.
6. **STOP. Print: "Awaiting approval per section. Reply with section names to approve, e.g. `apply: headline, about`."**

### PHASE 2 — Apply (only after explicit approval per section)

For each approved section, in order:
1. Navigate to the edit modal via the pencil/edit icon.
2. Apply the change using the target content below.
3. Save and verify (re-read the section after save closes).
4. Report: `✔ {section} updated. Verification: {first 100 chars of new content}`.
5. Wait 5 seconds before next section to avoid rate limits.

If LinkedIn shows a captcha, "unusual activity" warning, or any unexpected security modal → **STOP immediately**, screenshot to `~/linkedin-anomaly-$(date +%s).png`, and report what you saw.

---

## Target Content (source of truth)

### Headline (max 220 chars)
```
AI Agent Engineer · Building production LLM systems & autonomous workflows · Python Backend · Open to USD remote contracts
```

### About section
```
I build production AI agents and LLM systems. Backend engineer by foundation, now applying that to autonomous workflows that ship — not demos.

Open to USD remote contracts.


WHAT I'M SHIPPING

→ Cosmic Trader — a crypto trading agent running live on AWS, deployed via Terraform on EC2. Multi-strategy execution with signal-to-order architecture, Binance Futures integration, live risk management.

→ Claude Code Toolkit — custom slash commands, MCP server configurations, and plugin patterns for agentic development workflows.

→ Agent infrastructure — hierarchical context scaffolds for large monorepos, observability patterns for LLM-powered systems, evals harnesses.


HOW I WORK

Years of Python and Django across full-stack and distributed systems work. Async workers, message queues, observability — the unglamorous fundamentals that keep production alive. I'm now layering modern AI engineering on that foundation: agent orchestration, MCP, RAG, prompt engineering, evals.

My take: agents are software. They need architecture, tests, observability, and ops — not just a clever prompt. That's the gap I close.


STACK

• AI / Agents — Anthropic, OpenAI, MCP, Claude Code, LangChain, RAG, agent evals
• Backend — Python · Django · FastAPI · Node.js · TypeScript
• Infra — AWS · Terraform · Docker · Kubernetes · Linux
• Data — PostgreSQL · Redis · MongoDB · pgvector
• Automation — Playwright · Selenium · headless browsers


WHAT I'M LOOKING FOR

Remote contracts (USD) where AI agents do real work — production systems, not demos — and engineering quality is non-negotiable. Comfortable as the AI engineer in a small team or solo on a focused build. Available part-time or full contract.

Based in Brasília, Brazil.

GitHub  →  github.com/Satsuj1n
Email   →  felipenehz2003@gmail.com
```

**Important**: LinkedIn renders `\n\n` as paragraph break and single `\n` as line break. Preserve formatting exactly.

### Skills target order (top 10)
```
1. AI Agents
2. Large Language Models (LLMs)
3. Anthropic Claude
4. Model Context Protocol (MCP)
5. Python
6. Django
7. FastAPI
8. Amazon Web Services (AWS)
9. Terraform
10. PostgreSQL
```

If any of these aren't in my current Skills list, **propose adding** — do not auto-add. After my approval, add via Skills → "Add a new skill".

### Featured section
Recommend pinning (propose only, don't auto-pin):
- github.com/Satsuj1n (or new username if I've migrated)
- Profile README rendered view
- Cosmic Trader repo (only if I've made it public — verify first via web fetch)

### Open to Work
- If currently disabled: ask whether to enable.
- If enabled: ensure role types include `AI Engineer`, `Software Engineer`, `Backend Engineer`, `Machine Learning Engineer`.
- Visibility: **recruiters only** — do not enable the public #OpenToWork photo frame (looks desperate to recruiters).

### Experience descriptions
For each current/recent role, **propose** a rewrite that:
- Leads with impact / outcome, not responsibility list
- Mentions AI/agent-relevant work where applicable
- Stays under 4 sentences

Do NOT apply experience rewrites automatically — surface proposals for my approval one at a time.

---

## Hard Rules (NEVER violate)

- **No connections**: do not send invites, accept invites, or message anyone.
- **No posts**: do not create posts, articles, comments, or reactions.
- **No deletions**: do not delete experiences, education, skills, or any existing entries.
- **No photo changes**: do not modify the profile photo or banner.
- **No silent rewrites**: any change that wasn't pre-approved → propose, don't apply.
- **Stop on anomalies**: captcha, rate limit, "unusual activity", unexpected modals → halt + report.
- **English only**: all changes go in English.
- **One section at a time**: never batch-apply multiple section changes without separate approval for each.

---

## Success Criteria

- [ ] Audit report saved to `~/linkedin-audit-current-{date}.md`
- [ ] Diagnosis table printed in chat
- [ ] Headline updated (verbatim match to target)
- [ ] About section updated (with line breaks preserved)
- [ ] Skills reordered or additions proposed
- [ ] Featured section recommendations surfaced
- [ ] Open to Work status reviewed and decision applied
- [ ] Experience rewrite proposals presented (none auto-applied)
- [ ] Final diff report saved to `~/linkedin-audit-applied-{date}.md` showing before/after per section

---

**Start with Phase 1. Do not proceed to Phase 2 until I approve specific sections.**
