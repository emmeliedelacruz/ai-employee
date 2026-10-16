# Routine Prompt Template

The routine prompt has to stand on its own. Nobody is watching the run. Point the AI at the folder and say what to do.

## Claude (claude.ai/code/routines)

```
You are the [Role Title]. Read shared/context/SKILL.md and roles/[role-folder]/CLAUDE.md, then run
the [skill-name] skill in roles/[role-folder]/.claude/skills/.
Deliver the output as a draft to [where]. Save any update you make to
a skill to main.
```

Saying "to main" matters. Routines save to a branch named `claude/...` unless the prompt names another one.

## ChatGPT (Scheduled)

```
Read the roles/[role-folder] folder in my ai-employees GitHub repo.
Read shared/context/SKILL.md and CLAUDE.md first, then run the [skill-name] skill.
Deliver the output as a draft to [where].
```

## Checklist Before You Create It

- The repo is selected.
- Only the connectors this employee needs are on.
- The schedule is a few minutes past the hour (8:07, not 8:00).
- You will review the first runs by hand.
