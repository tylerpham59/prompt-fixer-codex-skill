# prompt-fixer

A Codex skill for fixing the "skill issue" before the agent starts working.

Inspired by Andrej Karpathy's framing that agents get better when we give them reusable skills, `prompt-fixer` turns rough prompts into execution-ready prompts with clear goals, missing-context checks, sharper alternatives, success criteria, verification steps, and an approval gate.

## What It Does

- Restates the user's intent before changing anything.
- Diagnoses gaps in goal, scope, inputs, constraints, output format, and verification.
- Asks only 1-3 high-impact questions when needed.
- Offers sharper, simpler, more ambitious, or more creative versions.
- Writes an execution-ready prompt.
- Stops for approval instead of immediately executing.

## Install

```bash
mkdir -p ~/.codex/skills/prompt-fixer
curl -L https://raw.githubusercontent.com/tylerpham59/prompt-fixer-codex-skill/main/SKILL.md \
  -o ~/.codex/skills/prompt-fixer/SKILL.md
```

Restart Codex if the skill does not appear right away.

## Files

- `SKILL.md` - the Codex skill definition.

## Why

If Codex cannot build it, the next question is not always "which model?"

Sometimes it is a skill issue: the agent needs a better reusable way to clarify, scope, and verify work before acting.
