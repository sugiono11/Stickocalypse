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
  (Episode 2, all four characters, production complete, quality score 97).
- `episode-01/` — Episode 1 "THE LAST DAY" continuity record, script,
  storyboard, subtitles, and YouTube package.
- `episode-02/` — Episode 2 "THE DOOR OPENS" continuity record, script,
  storyboard, subtitles, and YouTube package.
- `channel-description.md` — the YouTube channel description for STICKOCALYPSE.

## Permanent characters

- **Alex (CHAR_001)** — main protagonist, black stickman, expressive white
  eyes, red bandana, dark tactical outfit. Brave, intelligent, protective.
  Voice: `alex_voice_01`.
- **Max (CHAR_002)** — defender, dark charcoal stickman, dark green tactical
  vest. Loyal, strong, protective. Voice: `max_voice_01`.
- **Luna (CHAR_003)** — medical and strategic specialist, dark survival
  jacket, medical backpack, long dark hair tied in a ponytail (permanent
  design since Episode 2 v3). Intelligent, calm, resourceful, compassionate.
- **Shadow (CHAR_004)** — mysterious survivor, dark black silhouette, hooded
  clothing, glowing eyes. Quiet, mysterious, observant, secretive.

Full details are in `DATABASE_PLAN.md`.

## Status — Episode 1

**Complete, v5** — 60 seconds, 1080x1920, 30 FPS, verified with ffprobe.
Quality score **96/100**. Audio v2: 18 dialogue lines, 20 SFX events.
Motion: 7 of 8 scenes are true generated video; only Scene 3 (horde wide)
is still an animated still (video generation failed upstream, HTTP 502).
Square-head issue in Scenes 5 and 8 RESOLVED in v5 — all heads round.
Strict anatomical consistency rule applies: the supplied reference image
is the absolute source of truth.

## Status — Episode 2

**Complete, v3** — "THE DOOR OPENS", 60 seconds, 1080x1920, 30 FPS,
verified. Quality score **97/100**. All 8 scenes are true generated video.
Audio remixed louder (-15.5 LUFS). Luna's permanent design: long dark hair
tied in a ponytail, never wears Alex's red bandana. Subtitles: 17 entries,
zero overlaps. Shadow steps out of the bunker, Luna bandages Max, and the
radio orders Shadow to bring them to the safe zone — which is a lie.
Next: Episode 3 "THE TUNNEL".
