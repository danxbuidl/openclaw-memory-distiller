# openclaw-memory-distiller

`memory-distiller` is an OpenClaw skill for turning repeated user preferences,
successful patterns, and durable operating rules into reusable memory notes.

It is designed for workflows like:

- extracting stable preferences from conversations
- turning task outcomes into reusable rules
- producing prompt-ready context blocks from prior work
- separating durable memory from one-off chatter

## Skill

The published skill lives at:

- `memory-distiller/SKILL.md`

## What it produces

Depending on the request, the skill can help generate:

- a compact memory profile
- a prompt-ready context block
- a rules checklist for future tasks
- a cleanup pass that removes weak or temporary memories

## Example prompts

- `Use $memory-distiller to extract durable preferences from this conversation.`
- `Use $memory-distiller to turn these task outcomes into reusable working rules.`
- `Use $memory-distiller to create a concise context block I can reuse next time.`

## Repository goal

This repository is intended to host a standalone OpenClaw skill that can be
published to ClawHub and improved independently from core runtime changes.
