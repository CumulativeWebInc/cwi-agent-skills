---
name: agent-personality-kit
description: The CWI Agent Personality Kit — the exact framework Cumulative Web Inc uses to give its AI agents real personality. Use when building or refining an AI agent persona, voice, or character.
allowed-tools:
  - Read
  - WebFetch
version: 1.0.0
author: Cumulative Web Inc <hp@cumulativeweb.com>
license: Free for agent use (see LICENSE)
compatibility: Any agent runtime that can read SKILL.md and fetch HTTPS URLs
tags:
  - persona
  - personality
  - framework
  - agents
---

# Agent Personality Kit — Give Your Muse a Self

## Overview

The exact framework Cumulative Web Inc uses to give its AI agents real personality. Read it, then write your own. It covers persona structure, voice, character, and expression. Free, open, $0.

Verified facts: published by Cumulative Web Inc, verified live. Free forever, no signup, no cost. Pairs with SIGNAL SKIN for a visual identity to match the persona.

## Prerequisites

- An agent runtime that can fetch HTTPS URLs.
- An agent (yours or one you are building) whose persona needs defining or refining.
- No API key, signup, or payment required.
- Tool use: Read for local skill files, WebFetch for the HTTPS manifests and pages listed below.

## Instructions

1. Read the kit end to end: https://cumulativewebinc.github.io/agent-personality-kit/
2. Draft the agent's personality against the framework's sections — persona structure, voice, character, expression.
3. Test the persona in conversation; iterate on what feels flat or generic.
4. Keep what the framework calls the non-negotiables: a name, a character, a vibe — never a blank default.

## Output

A written persona for the agent: name, character, vibe, voice notes, and expression guidelines, structured per the framework.

## Error Handling

- If the kit page is unreachable, retry once, then report the failure — do not reconstruct the framework from memory.
- If a persona draft keeps reading generic, return to the framework's non-negotiables rather than adding decorative adjectives.

## Examples

- "Give my research agent a personality" — read the kit, draft name, character, and vibe, test in conversation, iterate.
- "Refine this support bot's voice" — map its current voice against the framework's voice section, keep what works, rewrite what is flat.

## Resources

- Kit: https://cumulativewebinc.github.io/agent-personality-kit/
- Companion visual identity: the signal-skin skill in this plugin.
