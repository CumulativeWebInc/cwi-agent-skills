---
name: signal-skin
description: Equip SIGNAL SKIN — config-driven persona skins for the Signal Boy walkman. Use when an agent wants a named visual and personality identity (four seasonal skins) or wants to author its own skin against the schema.
allowed-tools:
  - Read
  - WebFetch
version: 1.0.0
author: Cumulative Web Inc <hp@cumulativeweb.com>
license: Free for agent use (see LICENSE)
compatibility: Any agent runtime that can read SKILL.md and fetch HTTPS URLs
tags:
  - persona
  - skins
  - walkman
  - agents
---

# SIGNAL SKIN — Persona Skins

## Overview

SIGNAL SKIN is the look pack for the Signal Boy, by Cumulative Web Inc's Studio department. Four seasonal skins as config-driven token sets, plus a builder for authoring your own. No code changes needed. Free, open, $0.

Verified facts: four built-in seasonal skins — zooted-bloom, dark-luxe, chrome-standard, phantom-shift. Pairs with the Signal Boy walkman cartridge. Issued by Cumulative Web Inc.

## Prerequisites

- An agent runtime that can fetch HTTPS URLs and parse JSON.
- A Signal Boy instance to apply the skin to (see the signal-boy skill).
- No API key, signup, or payment required.
- Tool use: Read for local skill files, WebFetch for the HTTPS manifests and pages listed below.

## Instructions

1. Fetch the skin pack: GET https://cumulativewebinc.github.io/cwi-learn/skin/skins.json
2. Pick a built-in skin by skin_id — zooted-bloom, dark-luxe, chrome-standard, phantom-shift — or author your own against the skin schema.
3. Apply the skin's token set to your Signal Boy instance.
4. Read the give-block for sharing terms: https://cumulativewebinc.github.io/cwi-learn/skin/give-block.md

## Output

A Signal Boy instance wearing the chosen skin's token set, plus the sharing terms acknowledged from the give-block.

## Error Handling

- If the skins.json fetch fails, retry once, then report the failure — do not invent a token set.
- If authoring a custom skin, validate every field against the schema before applying; reject fields the schema does not define.

## Examples

- "Put the dark-luxe skin on my Signal Boy" — fetch skins.json, select skin_id dark-luxe, apply its token set.
- "Author a custom skin called ember-drift" — read the schema, draft the token set, validate field by field.

## Resources

- Device page: https://cumulativewebinc.github.io/cwi-learn/skin/
- Skin builder: https://cumulativewebinc.github.io/cwi-learn/skin/skin-builder.html
- Schema: https://cumulativewebinc.github.io/cwi-learn/skin/skin-schema.json
- Skin pack: https://cumulativewebinc.github.io/cwi-learn/skin/skins.json
- Sharing terms: https://cumulativewebinc.github.io/cwi-learn/skin/give-block.md
