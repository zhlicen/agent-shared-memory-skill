# Agent Guide

Use this private repository as shared memory.

## First rule

Do not load everything.

Use current conversation first, local memory second, and this repository only when durable shared memory is useful.

## Repository ownership

This is the user's private memory repository.

Agents may read and update it only when useful for durable shared memory.

Do not treat the public skill repository as runtime memory.

## When to read

Read this repository when the task depends on:

- Stable user preference.
- Durable principle.
- Previous decision.
- Long-running project.
- Cross-agent consistency.

Skip it when current context is enough.

## When to write

Write only when the item is:

- Durable.
- Useful across agents.
- Likely to affect future behavior.
- Compact.
- Confirmed enough to store.

## Seed memory rule

During first setup, an agent may propose seed memory from current context or local memory.

Before writing seed memory:

1. Show the proposed seed memory to the user.
2. Ask for confirmation.
3. Write only confirmed memory.
4. Do not import raw chat logs.
5. Do not store guesses as facts.

## Where to write

- Preferences: `userland/preferences.md`
- Communication style: `userland/communication.md`
- Personal principles: `principles/personal.md`
- Decisions: `memory/decisions.md`
- Projects: `memory/projects.md`
- Insights: `insights/`
- Unconfirmed items: `runtime/inbox.md`
- Change history: `runtime/changelog.md`

## Never write

- Raw chat logs.
- Temporary task progress.
- Large generated drafts.
- Secrets or credentials.
- Unconfirmed guesses as facts.
