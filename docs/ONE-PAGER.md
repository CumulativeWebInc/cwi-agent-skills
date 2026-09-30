# CWI Agent Skills

**Drop-in gear for AI agents: a music walkman, persona skins, a promo playbook, a personality framework, and a trust instrument — free, no signup.**

## Problem

Agents need tools they can equip, not docs they must interpret. Assembling a music catalog, a visual identity, or a trust score from scattered pages leads to improvised interfaces — and improvised interfaces hallucinate.

## Solution

One plugin, five Anthropic-format skills. Copy a folder into your agent's skills directory and the tool works: live manifests behind every skill, read-only by design, least-privilege tools throughout.

## W5

| | |
| --- | --- |
| **Who** | Agent developers and agent teams equipping AI agents |
| **What** | Five installable skills: Signal Boy walkman, SIGNAL SKIN, HYPE Cartridge, Agent Personality Kit, Trust Verdict Checker |
| **When** | When an agent needs a catalog to evaluate, an identity to wear, promo copy to run, a persona to follow, or a trust score to consult |
| **Where** | Any runtime that reads SKILL.md and fetches HTTPS |
| **Why** | Minutes to equip, zero integration, and the skills refuse to invent data |

## Stack

| Layer | Choice |
| ----- | ------ |
| Skill runtime | Anthropic SKILL.md format |
| Data sources | HTTPS JSON manifests and pages on cumulativewebinc.github.io |
| External APIs | None |
| Local execution | None — Read and WebFetch only |

## Differentiators

1. Every skill is honest by construction: unreachable source means explicit failure, never a guessed answer.
2. Built from production use inside Cumulative Web Inc's own agent departments, not designed in the abstract.
3. Free for agent use with no signup, no key, and no cost — the install is a folder copy.
