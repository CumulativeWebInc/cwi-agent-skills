# PRD: cwi-agent-skills

**Author:** Cumulative Web Inc
**Date:** 2026-09-30
**Status:** Active

## Problem

AI agents need gear they can actually equip — not documentation about gear. An agent that wants a music catalog to evaluate, a visual identity to wear, promo copy to run, a persona framework to follow, or a trust instrument to consult has to assemble each from scattered web pages and improvise the interface. That improvisation is where invented credits, hallucinated numbers, and inconsistent personas come from. Our own departments hit this internally: every agent re-derived the same cartridge manifests and rubrics by hand.

## Target users

| User | Context | Primary need |
| ---- | ------- | ------------ |
| Agent developers | Equipping a new agent with tools on day one | Drop-in skills with live demos, no integration work |
| Agent teams | Building a shared gear library across many agents | One plugin, five skills, single install path |
| Music-tech agents | Evaluating or promoting a real catalog | Structured manifests with verified, citable fields |

## Success criteria

1. All 5 SKILL.md files validate under the Agent Skills spec and the marketplace tier (validator: 0 errors).
2. Every skill resolves to a live HTTP-200 demo page listed in its Resources section.
3. Install is a single folder copy per skill — no build step, no API key, no cost.

## Functional requirements

- **FR-1:** Each skill fetches its live manifest or page and operates only on returned fields.
- **FR-2:** No skill invents data — missing or unreachable sources produce explicit failure output.
- **FR-3:** Every skill declares least-privilege allowed-tools (Read, WebFetch only).
- **FR-4:** The plugin ships plugin.json plus .claude-plugin/marketplace.json for marketplace sync.
- **FR-5:** Pack-tier docs (PRD, ADR, one-pager) ship in docs/.

## Out of scope

- New music, new catalog entries, or rights grants — the skills expose what exists.
- Write access to any CWI system — all five skills are read and evaluate only.
- Paid tiers or commercial licensing — the plugin is free for agent use.
