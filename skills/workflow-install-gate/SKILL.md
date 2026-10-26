---
name: workflow-install-gate
description: Evaluate whether to install, update, create, or skip an external AI skill, GitHub workflow, plugin, MCP server, connector, automation, or agent package. Use when the user asks about installing a skill repo, adding a plugin, adopting a workflow framework, comparing a new tool with existing local workflows, avoiding duplicate skills, checking maintenance quality, or deciding whether to fold an idea into an existing skill. Outputs an install decision with overlap, useful delta, risk, local changes, and rollback notes.
metadata:
  output: install-decision
---

# Workflow Install Gate

Use this skill before installing or creating any external skill, plugin, MCP server, automation, or workflow package.

## Decision Rule

Only act when the new package has a clear advantage over the current local setup.

## Workflow

1. **Check local overlap**
   - Search existing skills, agents, automations, scripts, docs, and memory notes.
   - If an existing workflow covers 70% or more of the task, update that workflow instead of installing a generic package.

2. **Check freshness**
   - Review release notes, recent commits, examples, issues, and maintenance signals.
   - Prefer actively maintained packages with concrete examples.

3. **Check real delta**
   - Identify what the package improves: speed, quality, reliability, repeatability, safety, or integration coverage.
   - Reject vague benefits like "looks useful" or "popular repo."

4. **Choose the smallest action**
   - `Skip`: duplicate, stale, irrelevant, or no clear upgrade.
   - `Update existing workflow`: good idea, already mostly covered locally.
   - `Create focused local workflow`: repeated local task with stable inputs and outputs.
   - `Install`: actively maintained package with a meaningful advantage.

5. **Skill optimization gate**
   - If the action changes an existing skill, first write 2-3 test prompts that represent normal user requests for that skill.
   - Change only one dimension at a time, such as trigger wording, workflow steps, fallback behavior, output format, or safety rules.
   - After the edit, show a before/after comparison against the test prompts or the changed section.
   - Do not keep a skill change based only on the editor's self-score. Require human review or an independent review pass.
   - Keep a rollback path for every skill edit, using git revert or a file backup when the workspace is not a git repo.

6. **Protect the workspace**
   - Do not install broad packs when only one small rule is useful.
   - Do not overwrite local custom workflows.
   - Keep a rollback note for every install or update.

## Output Format

```text
Decision: Skip / Update existing workflow / Create focused workflow / Install
Reason:
Overlap with existing tools:
Useful delta:
What changes locally:
Validation:
Risk:
Rollback:
```
