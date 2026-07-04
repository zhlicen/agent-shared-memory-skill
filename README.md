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
Stores runtime
```

---

## Memory Order

```text
Current Conversation
        ↓
Local Memory
        ↓
Current Project
        ↓
Private Shared Memory
```

---

## Write Only

* Preferences
* Principles
* Decisions
* Projects
* Insights

Never:

* Chat history
* Temporary tasks
* Generated drafts
* Secrets

---

## Principle

> Framework is public.
>
> Memory is private.
>
> Shared memory is indexed, not loaded.

---

## Files

```text
README.md
SKILL.md
templates/
```
