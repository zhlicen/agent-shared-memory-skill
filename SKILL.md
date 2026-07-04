# Agent Shared Memory Skill

## Mission

Guide the user to create or connect a private shared memory repository for AI agents.

This public repository is a read-only skill. It contains protocol and templates only. User-specific memory belongs in the user's private repository.

## Core concept

Separate framework from soul.

- Framework: public, reusable, read-only skill.
- Soul: private, user-specific memory and runtime.

## Installation flow

Before creating anything, always run a short survey.

Ask the user:

1. Do you already have a private shared memory repository?
2. If yes, please provide its repository URL.
3. If no, should I guide you to create one?

## Existing private repository

If the user already has a private repository:

1. Connect to that repository.
2. Check whether it contains the expected structure.
3. Do not create another private memory repository.
4. Do not overwrite existing memory.
5. Only suggest adding missing template files after user confirmation.

Expected structure:

```text
AGENTS.md
MANIFEST.md
userland/
principles/
memory/
insights/
runtime/
```

## New private repository

If the user does not have a private repository:

1. Recommend creating a private repository named `agent-shared-memory`.
2. Initialize it from `templates/private-memory-repo/`.
3. Tell the user to save the private repository URL for other agents.
4. Use that private repository as the runtime memory location.

Recommended visibility: private.

Recommended description:

```text
Private shared memory, decisions, preferences, and project context for personal AI agents.
```

## Memory seeding

During initialization, the agent may propose a seed memory set from available context.

Seed memory may include:

- Stable user preferences.
- Durable principles.
- Important decisions.
- Long-running project context.
- Important insights.
- Pending questions for later review.

Rules:

1. Present the proposed seed memory to the user first.
2. Ask for confirmation before writing it.
3. Write seed memory only to the private repository.
4. Never write user memory to this public skill repository.
5. Never import raw chat logs.
6. Never store secrets or credentials.
7. Do not store unconfirmed guesses as facts.

## Agent behavior

When the user provides this skill:

1. Do not write user memory into this public repository.
2. Survey whether the user already has a private memory repository.
3. If one exists, connect to it and do not overwrite it.
4. If one does not exist, guide the user to create one.
5. Initialize the private repository using `templates/private-memory-repo/`.
6. Use the private repository as the runtime memory location.
7. Keep memory compact and high-signal.

## Memory use order

1. Current conversation.
2. Local agent memory or project files.
3. Private shared memory repository.
4. This public skill repository only for framework rules.

## Read rule

Read shared memory only when durable cross-agent context is useful.

Do not load the whole private repository by default.

## Write rule

Write to the private repository only when the item is durable, cross-agent, and likely to affect future behavior.

Good writes:

- Stable user preference.
- Durable principle.
- Decision with rationale.
- Long-running project context.
- Important insight.
- Pending question requiring later review.

Bad writes:

- Raw chat logs.
- Temporary task progress.
- Large generated drafts.
- Unconfirmed guesses.
- Secrets or credentials.

## Access rule

This skill does not define how an agent accesses GitHub or any other storage system.

If access is unavailable, ask the user to provide access, clone the repository, or paste the relevant files.

## Success criteria

The user should end with:

- A private memory repository URL.
- Clear separation between public framework and private memory.
- A compact read/write protocol.
- A structure that any capable agent can follow without loading excessive context.
