# Decisions

Append-only durable decision log.

## Format

```md
## D-001 — YYYY-MM-DD — Decision title

- Decision:
- Rationale:
- Scope:
- Status: active | superseded by D-XXX
- Agent:
- Related:
```

Example:

```md
## D-001 — 2026-01-15 — One private repo for all agent memory

- Decision: All agents share a single private memory repository.
- Rationale: One source of truth beats per-agent silos.
- Scope: All agents.
- Status: active
- Agent: claude-code
- Related: none
```

## Rules

- Record decisions that change future behavior, architecture, project direction, or operating rules.
- Give each decision the next sequential ID, and reference decisions by ID.
- Include rationale.
- Do not silently rewrite old decisions.
- Mark superseded decisions instead of deleting them.
- When this file exceeds about 200 lines, move superseded decisions to `memory/decisions-archive.md` and log the move.
