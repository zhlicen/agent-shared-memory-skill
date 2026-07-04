# Agent Shared Memory Skill

**A public, read-only skill for building private cross-agent memory.**

---

## TL;DR

This repository teaches AI agents **how to use shared memory**.

It does **not** store user memory.

User memory belongs in a **private repository**.

---

## Quick Install

Copy this to any AI agent:

```text
Use this skill:
https://github.com/zhlicen/agent-shared-memory-skill
Read README.md and SKILL.md.
Treat this repository as read-only.
If I don't have a private shared memory repository, help me create one.
If I already have one, use it for all future shared memory and runtime.
```

Review the files yourself before adopting them. Pin a commit or tag if you want the protocol immutable.

To install as a Claude Code skill, clone into a directory named `agent-shared-memory` (matching the skill name in `SKILL.md`).

---

## Architecture

```text
Public Skill (this repo)
    ↓
Teaches agents how memory works

Private Repository
    ↓
Stores user preferences
Stores decisions
Stores projects
Stores insights
Stores runtime (inbox + changelog)
```

---

## Context Order

```text
Current Conversation
        ↓
Local Memory + Project Files
        ↓
Private Shared Memory
        ↓
Public Skill (framework rules only)
```

Check the top first. Go lower only when needed.

---

## Write Only

* Preferences
* Principles
* Decisions
* Projects
* Insights
* Pending questions

Never:

* Chat history
* Temporary tasks
* Generated drafts
* Unconfirmed guesses
* Secrets

---

## Principle

> Framework is public.
>
> Memory is private.
>
> Shared memory is indexed, not loaded.

Indexed: agents pick the smallest relevant file through the private repo's `MANIFEST.md`, never bulk-load.

---

## Files

```text
README.md
QUICKSTART.md
SKILL.md
LICENSE
templates/
```
