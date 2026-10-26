---
name: comic-preflight
description: Run a final publishing checklist for comics, carousels, short videos, storyboards, covers, and visual storytelling assets. Use before publishing or handing off final files.
---

# Comic Preflight

Catch avoidable publishing problems before the asset goes out.

This is a final check. If the story or storyboard itself is weak, route back to `comic-review`.

## Checks

### Content

- First panel or first seconds create a reason to continue.
- Story setup is understandable without extra explanation.
- Ending beat is clear.
- Captions or subtitles have no placeholders.
- No accidental private notes, prompt fragments, or draft comments.

### Visual

- Character design stays consistent.
- Important text is readable on mobile.
- Cover or first frame is legible at small size.
- Color and lighting are consistent enough for the format.
- No obvious generation artifacts in important areas.

### Format

- Aspect ratio matches the target platform.
- Resolution is high enough.
- File type is accepted by the platform.
- Duration fits the intended channel.
- Safe area is respected for captions and UI overlays.

### Audio And Captions

- Audio is present if expected.
- Loudness is reasonable.
- Captions are synced.
- Captions do not cover key faces or action.
- Licensed music or audio rights are clear.

### Publishing

- Title supports the hook.
- Description does not over-explain.
- Hashtags or tags are limited and relevant.
- CTA is clear if needed.
- Final files are archived.

## Output Format

```markdown
## Preflight: {asset}

Target platform:
{platform or format}

Status:
{clear to publish / publish after fixes / blocked}

Blockers:
- {issue and fix}

Fix before publishing:
- {issue and fix}

Passed checks:
- {selected checks}

Final export notes:
- aspect ratio: {value}
- resolution: {value}
- duration: {value}
- file type: {value}

Next step:
{publish / fix and rerun preflight / return to review}
```

## Rules

- Be strict about unreadable text, wrong aspect ratio, and broken captions.
- Do not pretend to verify files you cannot inspect.
- If only a description is provided, clearly mark checks that need the actual file.
- If the platform is unknown, check common formats and ask where it will publish.
