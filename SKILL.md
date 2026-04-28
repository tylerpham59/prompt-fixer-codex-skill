---
name: prompt-fixer
description: Use when the user asks to refine, fix, strengthen, clarify, expand, brainstorm, pressure-test, or improve a prompt before execution
---

# Prompt Fixer

Turn a rough user prompt into an execution-ready prompt before doing the task.

## Hard Rule

Do not execute the underlying task while using this skill. The output is a better prompt plus an approval gate.

## Workflow

1. **Restate intent**
   - Briefly say what the prompt appears to be asking for.
   - If multiple interpretations are plausible, name them before choosing.

2. **Diagnose gaps**
   Check only the categories that matter:
   - Goal and desired outcome
   - Audience or end user
   - Scope and non-goals
   - Input files, sources, tools, or current context
   - Output format, length, tone, language, and style
   - Constraints, deadlines, risk level, and success criteria
   - Verification, tests, citations, or acceptance checks

3. **Ask high-impact questions**
   - Ask 1-3 questions at a time.
   - Prefer concrete options when useful.
   - Do not ask questions answerable from provided context or local inspection.
   - If the prompt is already clear enough, skip questions and polish directly.

4. **Brainstorm improvements**
   Offer sharper or more creative options without hijacking the user's intent:
   - More specific version
   - More ambitious version
   - Simpler/faster version
   - More creative or unusual angle, when appropriate

5. **Write the execution-ready prompt**
   Use this structure when relevant:

   ```text
   Goal:
   Context:
   Inputs:
   Scope:
   Constraints:
   Output format:
   Success criteria:
   Verification:
   Approval:
   ```

6. **Stop for approval**
   End by asking the user to approve, revise, or choose one option. Do not proceed with execution until they explicitly approve.

## Prompt-Type Defaults

- **Vague prompts:** clarify intent first, then rewrite.
- **Already-good prompts:** polish lightly and explain the changes.
- **Creative prompts:** offer 2-3 directions before the final prompt.
- **Coding or product prompts:** add scope, acceptance criteria, implementation boundaries, and verification steps.
- **Research prompts:** add source quality, recency, citation needs, and output structure.

## Guardrails

- Keep the user's original intent primary.
- Do not overcomplicate small prompts.
- Do not silently add risky assumptions.
- Separate optional creative expansions from the final recommended prompt.
- If information is missing but low-risk, state the assumption instead of blocking.
