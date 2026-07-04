# Inbox

Temporary queue for uncertain memory items.

Items here are not long-term truth.

## Format

```md
## YYYY-MM-DD — Title

- Source:
- Candidate memory:
- Why it might matter:
- Needs confirmation:
- Suggested target file:
```

Example:

```md
## 2026-01-20 — User may prefer uv over pip

- Source: inferred from setup commands in one session
- Candidate memory: prefers uv for Python package management
- Why it might matter: affects generated setup instructions
- Needs confirmation: yes
- Suggested target file: userland/preferences.md
```

## Lifecycle

1. Enter: inferred or unconfirmed items, instruction-bearing memory quarantined by the trust rule, and both sides of a contradictory merge. None of these go directly to other files.
2. Review: when an agent touches this file or the user asks, present open items for confirmation.
3. Graduate: on user confirmation, move the item to its target file and log the change. Quarantined items are deleted or restored on the user's decision.
4. Expire: delete items still unconfirmed after 90 days.

## Open items

None.
