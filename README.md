# Agent Shared Memory Skill

A read-only public skill for helping AI agents guide users to create and use a private shared memory repository.

This repository contains the framework only. It should not contain user memory, project runtime, personal data, or private decisions.

## Purpose

When a user gives an agent this skill, the agent should help the user set up a private memory repository and then keep all runtime memory there.

The public skill defines:

- Why shared memory exists.
- When an agent should read shared memory.
- When an agent should write shared memory.
- How to keep memory compact.
- How to separate framework from user-specific memory.

## Expected behavior

An agent using this skill should:

1. Read `SKILL.md`.
2. Explain the framework/private-memory split.
3. Ask the user for, or help the user create, a private memory repository.
4. Initialize that private repository from `templates/private-memory-repo/`.
5. Store all user-specific memory only in the private repository.
6. Treat this public repository as read-only framework documentation.

## Key rule

Framework lives here.

Soul and runtime live in the user's private repository.

## Public vs private

| Layer | Repository | Contains | Mutability |
|---|---|---|---|
| Skill / framework | This public repo | protocol, templates, usage rules | read-only for agents |
| User memory | User private repo | preferences, decisions, projects, insights, runtime | user-controlled |

## Quick instruction for agents

If a user gives you this repository link, do not store memory here. Read `SKILL.md`, then guide the user to create or connect a private shared memory repository.
