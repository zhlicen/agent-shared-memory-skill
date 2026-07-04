# Private Agent Shared Memory

This is the user's private shared memory repository.

It stores durable memory for AI agents. It is not a chat archive.

Template version: 0.2.1

## Purpose

Use this repository to preserve high-signal information that should affect future AI behavior across tools.

## Context order

1. Current conversation.
2. Local agent memory and project files.
3. This private shared memory repository.
4. Public skill repository, for framework rules only.

## Read rule

Read selectively. Do not load the whole repository by default.

Use `MANIFEST.md` to choose the smallest relevant file.

## Write rule

Write rarely. Save only durable, cross-agent information.

Write directly only what the user stated or confirmed. Inferred items go to `runtime/inbox.md` first.

## Directory map

```text
AGENTS.md                Quick instruction for agents
MANIFEST.md              File selection guide
userland/                User working style and preferences
principles/              User principles + framework defaults
memory/                  Decisions, projects, glossary
insights/                Long-term insights
runtime/                 Inbox and changelog
```

## Rule

Framework lives in the public skill repository.

User memory lives here.
