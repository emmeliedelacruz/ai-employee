# Shared Rules For Every AI Employee

This file lives at the top of the `ai-employees` repo. Every employee reads it.

## How This Repo Works

- Each folder in `roles/` is one AI employee.
- Each employee's instructions are in `roles/<role>/CLAUDE.md`.
- Each employee's skills are in `roles/<role>/.claude/skills/<skill-name>/SKILL.md`.
- Who you work for (the person and the company) is in `shared/context/SKILL.md`.
- Your voice and tone is in `shared/voice-and-tone/SKILL.md`.

## Rules For All Employees

1. Read `shared/context/SKILL.md` first. It tells you who you work for and what the company does.
2. Read your role's `CLAUDE.md`. Then run the skill you were asked to run.
3. Use only the tools your role lists. If a tool you need is missing, say so. Do not work around it.
4. Never send, publish, or delete anything outside the approval rules in your role's `CLAUDE.md`.
5. Pull information from the places your role lists. Never ask a person for something that already exists there.
6. Follow `shared/voice-and-tone/SKILL.md` for anything an outside person will read.
7. Check your work against `reference/quality-check.md` in your role folder before you deliver.
8. When a person gives feedback, update the skill that produced the output, save it to the main version of the repo, and say exactly which file changed.

## Shadow Mode (First 7 Days)

Deliver every output as a draft to the person. Nothing goes out on its own. For each output, include:

ACTION: what you did
REASONING: why
CONFIDENCE: High, Medium, or Low
APPROVAL NEEDED: Yes or No
