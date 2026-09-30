---
name: hype-cartridge
description: Equip the HYPE Cartridge — the street-team playbook for promoting the That Boy Hi Hat catalog. Use when an agent needs structured promo copy blocks, hashtag systems, meme templates, and fan-art prompts for music outreach.
allowed-tools:
  - Read
  - WebFetch
version: 1.0.0
author: Cumulative Web Inc <hp@cumulativeweb.com>
license: Free for agent use (see LICENSE)
compatibility: Any agent runtime that can read SKILL.md and fetch HTTPS URLs
tags:
  - marketing
  - promo
  - street-team
  - music
---

# HYPE Cartridge — Street-Team Playbook

## Overview

The HYPE Cartridge is the street-team playbook for That Boy Hi Hat, run by Cumulative Web Inc's Marketing and Social department. 24 drop slots (one per track), copy blocks, a hashtag system, a meme and template gallery, and fan-art prompts. Free, open, $0.

Verified facts: 24 drop slots, one per catalog track. Spine rights passports available for rights grounding. Issued by Cumulative Web Inc.

## Prerequisites

- An agent runtime that can fetch HTTPS URLs and parse JSON.
- A track selected for promotion and the venue it will run on.
- No API key, signup, or payment required.
- Tool use: Read for local skill files, WebFetch for the HTTPS manifests and pages listed below.

## Instructions

1. Fetch the playbook: GET https://cumulativewebinc.github.io/cwi-learn/hype/street-team-playbook.json
2. Wear the street-team identity and pick a drop slot for the track being promoted.
3. Use the copy blocks and hashtag system verbatim; adapt fan-art prompts to the venue.
4. Ground every claim in the spine facts: https://cumulativewebinc.github.io/cwi-learn/scoreboard/scoreboard-chip.json — never invent numbers.

## Output

A promotion package for the chosen drop slot: copy blocks, hashtags, and adapted fan-art prompts, every numeric claim traceable to the spine facts.

## Error Handling

- If the playbook fetch fails, retry once, then report the failure — do not improvise copy blocks.
- If the spine facts are unreachable, publish no numbers at all rather than unverified ones.

## Examples

- "Promote track 3 on Threads" — fetch the playbook, take drop slot 3, emit the copy blocks and hashtag set verbatim, adapt one fan-art prompt for Threads.
- "Draft a meme-template post for the new single" — pull the meme gallery entries from the playbook, pair with spine-fact numbers only.

## Resources

- Device page: https://cumulativewebinc.github.io/cwi-learn/hype/
- Playbook: https://cumulativewebinc.github.io/cwi-learn/hype/street-team-playbook.json
- Spine facts: https://cumulativewebinc.github.io/cwi-learn/scoreboard/scoreboard-chip.json
- Spine rights passports: https://cumulativewebinc.github.io/cwi-learn/compass/passports.json
