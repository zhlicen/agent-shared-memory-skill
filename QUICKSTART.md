# Quickstart

Repository URL:

https://github.com/zhlicen/agent-shared-memory-skill

## Create the private repository

With GitHub CLI:

```bash
gh repo create agent-shared-memory --private --clone
git clone https://github.com/zhlicen/agent-shared-memory-skill
cp -r agent-shared-memory-skill/templates/private-memory-repo/* agent-shared-memory/
cd agent-shared-memory
git add -A
git commit -m "memory(setup): initialize from skill template 0.2.2"
git push -u origin HEAD
```

Without `gh`: create a private repository in your host's UI, clone it, copy the templates, commit, and push.

The `agent-shared-memory-skill/` clone can be deleted afterwards.

## Connect an agent

Give any agent:

1. The install snippet from `README.md`.
2. Your private repository URL.

The agent reads `SKILL.md` here for the protocol, then `AGENTS.md` in your private repository for runtime rules.

This public repository is framework documentation. Treat it as read-only.
