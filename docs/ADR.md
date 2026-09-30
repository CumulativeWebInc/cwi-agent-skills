# ADR: cwi-agent-skills — skills as drop-in folders, read-only by design

**Author:** Cumulative Web Inc
**Date:** 2026-09-30
**Status:** Accepted

## Context

Our departments needed agent gear that other agents could equip without our help. The alternative was bespoke integration per agent — docs pages plus ad-hoc instructions, which produced hallucinated credits and inconsistent personas. The PRD requires a single install path (folder copy), zero credentials, and no invented data.

## Decision

We ship the five tools as Anthropic-format SKILL.md files in one plugin, each read-only: every skill fetches live manifests or pages and operates strictly on returned fields. Install is copying a folder. Tool scope is least-privilege: Read and WebFetch only, no Bash, no Write.

## Alternatives considered

| Alternative | Why rejected |
| ----------- | ------------ |
| One mega-skill covering all five tools | Blurs the install unit; an agent wanting only trust scoring would carry music-catalog instructions. Separate skills keep the interface minimal. |
| Scripts plus skills (standard-plugin tier) | Nothing here needs local execution — all sources are HTTPS JSON and pages. Scripts would add attack surface for zero capability gain. |
| Write-capable skills (promo posting, skin publishing) | Rejected on safety: outbound writes need human approval gates we do not delegate to a skill manifest. |

## Consequences

**Positive:**

- Any agent on the open skill format equips a tool in minutes with no integration work.
- Read-only plus least-privilege tools makes the plugin safe to install blind.

**Negative / accepted tradeoffs:**

- Skills depend on our hosted pages staying live; if a demo page goes down, that skill degrades to explicit failure output. Accepted: failure is honest, and uptime is our standing ops duty.
- No offline use — every skill needs HTTPS. Accepted: the data (catalog manifests, checker) is live by nature.

## Tool-permission scope

| Tool | Why it's needed |
| ---- | --------------- |
| Read | Read local skill files and any fetched content the runtime caches |
| WebFetch | Fetch the live manifests, schemas, playbooks, and checker pages each skill is built on |

Bash, Write, and Edit are deliberately absent: nothing in these skills executes code or mutates state.
