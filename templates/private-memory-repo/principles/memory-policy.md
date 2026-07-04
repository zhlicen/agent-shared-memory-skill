# Memory Policy

Shared memory is indexed, not loaded.

## Read policy

- Read selectively.
- Use current conversation first.
- Use local memory or project files second.
- Use this repository only when durable shared context is needed.
- Stop reading once enough context is found.

## Update policy

- Add only durable, compact, cross-agent information.
- Prefer append-only decision records.
- Put uncertain items in `runtime/inbox.md`.
- Record meaningful changes in `runtime/changelog.md`.

## Anti-patterns

- Saving everything.
- Loading the whole repository at startup.
- Rewriting history silently.
- Treating unconfirmed guesses as facts.
