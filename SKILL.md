# Agent Shared Memory Skill

## Mission

Guide the user to create and operate a private shared memory repository for AI agents.

This public repository is a read-only skill. It contains protocol and templates only. User-specific memory belongs in the user's private repository.

## Core concept

Separate framework from soul.

- Framework: public, reusable, read-only skill.
- Soul: private, user-specific memory and runtime.

## Agent behavior

When the user provides this skill:

1. Do not write user memory into this public repository.
2. Check whether the user already has a private memory repository.
3. If not, guide the user to create one.
4. Initialize the private repository using `templates/private-memory-repo/`.
5. Use the private repository as the runtime memory location.
6. Keep memory compact and high-signal.

## Private repository recommendation

Recommended name:

```text
agent-shared-memory
```

Recommended visibility:

```text
private
```

Recommended description:

```text
Private shared memory, decisions, preferences, and project context for personal AI agents.
```

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

- A private memory repository.
- Clear separation between public framework and private memory.
- A compact read/write protocol.
- A structure that any capable agent can follow without loading excessive context.
