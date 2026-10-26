---
name: comic-review
description: Review comic, storyboard, short-video, panel, cover, script, character design, or scene plan work from multiple creative roles. Use when the user asks to review, check, critique, or improve visual storytelling assets.
---

# Comic Review

Review the work for story clarity, visual continuity, pacing, and publishing fit.

Lead with problems and fixes. Do not pad the review with praise.

## Identify The Asset

First identify what the user provided:

- logline
- script
- storyboard
- panel sequence
- character sheet
- cover
- image prompt set
- rough cut
- final video

Then choose only the relevant review roles.

## Review Roles

| Role | Checks |
| --- | --- |
| Writer | motivation, conflict, stakes, dialogue, ending |
| Director | pacing, emotional rhythm, camera logic, scene focus |
| Storyboard artist | shot clarity, panel flow, composition, readability |
| Art director | style consistency, character continuity, color, lighting |
| Editor | first seconds, transitions, timing, sound and subtitle rhythm |
| Distribution | platform fit, cover frame, title, aspect ratio, thumbnail readability |

## Severity

- `Blocker`: must fix before generation or publishing.
- `Fix`: should fix, but not fatal.
- `Consider`: optional improvement.

## Output Format

```markdown
## Review: {asset}

Asset type:
{script / storyboard / panel sequence / rough cut / etc.}

Findings:

1. [Blocker] {role}: {issue}
   Fix: {specific change}

2. [Fix] {role}: {issue}
   Fix: {specific change}

What to keep:
- {only if useful}

Ship or continue?
{ready / revise first / not ready}

Next step:
{one concrete action}
```

## Rules

- Do not score the work out of 10.
- Do not list more than 10 findings.
- If the work is an early draft, review structure before details.
- If character consistency is weak, flag it before style polish.
- If the first seconds or first panel fail, treat it as high severity.
- If the user asks for a rewrite, provide it after the review.
