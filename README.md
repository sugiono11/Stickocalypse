# STICKOCALYPSE

**Universe:** THE LAST SURVIVORS
**Format:** Cinematic stickman apocalypse animation for YouTube Shorts
**Duration:** 60 seconds — 8 scenes x 7.5 seconds
**Aspect ratio:** 9:16, 1080x1920, 30 FPS
**Language:** English story and subtitles

This repository is the **single source of truth** for STICKOCALYPSE.
Character designs and voice profiles must not change without Vio's explicit
authorization. Every episode must be checked against the database plan here
before production.

## Files

- `DATABASE_PLAN.md` — the database plan: CHARACTER_MEMORY, WORLD_MEMORY,
  STORY_MEMORY, PRODUCTION_MEMORY, and STYLE_MEMORY. This is the lock for
  characters and voices.
- `project.json` — the same project state as machine-readable JSON
  (Episode 1, Alex and Max, production complete, quality score 94).
- `episode-01/` — Episode 1 "THE LAST DAY" continuity record, script,
  storyboard, subtitles, and YouTube package.

## Permanent characters

- **Alex (CHAR_001)** — main protagonist, black stickman, expressive white
  eyes, red bandana, dark tactical outfit. Brave, intelligent, protective.
  Voice: `alex_voice_01`.
- **Max (CHAR_002)** — defender, dark charcoal stickman, dark green tactical
  vest. Loyal, strong, protective. Voice: `max_voice_01`.
- **Luna (CHAR_003)** — medical and strategic specialist, dark survival
  jacket, medical backpack. Intelligent, calm, resourceful, compassionate.
- **Shadow (CHAR_004)** — mysterious survivor, dark black silhouette, hooded
  clothing, glowing eyes. Quiet, mysterious, observant, secretive.

Full details are in `DATABASE_PLAN.md`.

## Status — Episode 1

**Complete, v4** — 60 seconds, 1080x1920, 30 FPS, verified with ffprobe.
Quality score **94/100**. Audio v2: 18 dialogue lines, 20 SFX events.
Motion: 7 of 8 scenes are true generated video; only Scene 3 (horde wide)
is still an animated still (video generation failed upstream, HTTP 502).
Known issue: Scenes 5 and 8 render Alex/Max with square/blocky heads,
other scenes have round heads — fix attempts failed upstream (HTTP 502/503),
see `episode-01/EPISODE_01.md`. Strict anatomical consistency rule applies:
the supplied reference image is the absolute source of truth.
