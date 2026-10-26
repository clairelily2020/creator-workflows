---
name: comic-story-pipeline
description: Turn a rough comic or short-video idea into a production-ready story package. Use when the user wants a comic, storyboard, short visual story, character brief, scene plan, image prompt set, or story-to-video workflow.
---

# Comic Story Pipeline

Use this skill to turn a rough idea into a production brief that another tool, artist, or editor can execute.

The goal is not to write a long generic story. The goal is to create enough structure for consistent characters, clear scenes, useful panels, and publishable pacing.

## Inputs To Ask For

Ask only for missing details that change the output:

- story idea or logline
- target format: comic panels, carousel, vertical short, horizontal video, storyboard doc
- duration or panel count
- audience and tone
- visual style
- language
- platform if known
- any fixed character, setting, or brand constraints

If the user only gives one sentence, proceed with reasonable assumptions and state them briefly.

## Production Stages

### 1. Logline And Story Shape

Clarify:

- protagonist
- desire
- obstacle
- escalation
- ending beat

### 2. Beat Sheet

Create 5 to 9 beats, depending on length.

Each beat should contain:

- what changes
- emotional turn
- visual anchor

### 3. Script

Write concise scene text:

- action
- dialogue or narration
- sound cues if needed
- duration or panel estimate

Avoid over-explaining. Visual stories need playable moments.

### 4. Storyboard

Create a panel or shot list.

Each row should include:

- panel or shot number
- framing
- camera angle or movement
- character action
- background
- text or subtitle
- image prompt notes

### 5. Character Consistency

For each recurring character, define:

- age range
- body type
- face and hair cues
- clothing
- color cues
- expression range
- no-change details

### 6. Scene And Asset Plan

List:

- locations
- key props
- required generated images
- required video clips
- required audio or captions
- publishing format

## Output Format

```markdown
## Production Brief: {title}

Assumptions:
- {assumption}

Logline:
{one sentence}

Format:
{comic / carousel / vertical short / horizontal video}

Beat sheet:
1. {beat}
2. {beat}

Script:
| Scene | Action | Dialogue/Narration | Notes |
| --- | --- | --- | --- |

Storyboard:
| # | Framing | Action | Background | Text | Prompt notes |
| --- | --- | --- | --- | --- | --- |

Character consistency:
{character notes}

Asset plan:
- {asset}

Production risks:
- {risk}

Next step:
{generate panels / review storyboard / run preflight}
```

## Rules

- Keep the story visually playable.
- Do not create more characters than the format can support.
- Lock recurring character details before scene prompts.
- If the concept is too broad, shrink it to one scene or one emotional turn.
- If the user wants review rather than creation, route to `comic-review`.
- If the user is ready to publish, route to `comic-preflight`.
