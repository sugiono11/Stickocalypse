# STICKOCALYPSE — Episode 1: "THE LAST DAY"
## Continuity record

- Universe: THE LAST SURVIVORS
- Episode: 1 of the series
- Duration: 60 seconds (8 scenes x 7.5 s), 9:16, 1080x1920, 30 FPS
- Final video: `stickocalypse-ep01-the-last-day-1080x1920.mp4` (43 MB, H.264/AAC) — **v4** (see below). V1, v2, v3 files kept as `stickocalypse-ep01-the-last-day-1080x1920-v1.mp4` / `-v2.mp4` / `-v3.mp4`.
- Quality score: 94/100 (see QC section)
- Status: complete, verified with ffprobe (60.000 s, 1080x1920, 30 fps, audio present)

## Strict anatomical consistency (Vio, 2026-11-24)

Use the exact same approved 3D stickman character from the supplied reference image — the reference is the absolute source of truth. Preserve the original head size, head shape, shoulder width, torso length, arm length, leg length, limb thickness, eye placement and overall silhouette. The character must retain the exact same body model throughout the entire animation. Animate only the required movements; natural body movement is allowed, but do not redesign, stretch, shrink, morph or deform the character. Maintain the same clothing, accessories and visual identity. Use physically coherent movement with consistent anatomy across all frames.

## Summary

Day 47 after the fall. Alex stands alone on a rooftop above the burning city,
holding his glowing baton, when Max arrives with a warning: the horde has
found the bridge. The radio promises a safe zone, but Max says dawn is too
late. They run the rooftops, Max slips at the edge and Alex pulls him up, and
they reach the bunker door — locked. A strange signal crackles on the radio.
Then the door opens by itself, glowing eyes appear in the dark, and a
mysterious voice says: "You shouldn't be here."

## Timeline (story)

1. Day 47: the city fell in one night.
2. Alex alone on the rooftop at sunset, glowing baton, helicopter overhead.
3. Max warns: the horde found the bridge.
4. The horde is seen moving through the ruined city and across rooftops.
5. The radio mentions a safe zone. Alex: move at dawn. Max: dawn is too late.
6. Rooftop chase; Alex and Max jump the gap between buildings.
7. Max slips at the rooftop edge; Alex pulls him up as the baton flares.
8. The bunker door is locked; the radio crackles with a strange signal.
9. The bunker door opens by itself; glowing eyes in the dark; "You shouldn't be here."

## Locations

- Rooftop over the burning city (sunset, then night)
- The bridge (horde crossing point, mentioned)
- Ruined city streets and rooftops (horde)
- Steel bunker door — sign reads "RESTRICTED - LEVEL 3 - NO ENTRY"

## Characters

- Alex (CHAR_001): protagonist. Black stickman, red bandana, dark tactical outfit, glowing orange baton. Brave, intelligent, protective.
- Max (CHAR_002): defender. Dark charcoal stickman, broad shoulders, dark green tactical vest. Loyal, strong, protective.
- Shadow (CHAR_004): NOT introduced. Only teased — glowing eyes in the dark + one low mysterious voice line at the cliffhanger.
- Luna (CHAR_003): does not appear in Episode 1.

## Relationships

- Alex and Max: survival partners. Alex leads and plans; Max defends and warns. Alex saves Max at the rooftop edge (Scene 6).

## Unresolved mysteries (for Episode 2+)

- Who is inside the bunker? Whose glowing eyes are they?
- What is the strange radio signal, and who is sending it?
- Where is the safe zone, and is it real?
- What happened on the night the city fell (Day 1)?
- Where are Luna and the other survivors?

## Next episode direction

Episode 2: Alex and Max must decide whether to enter the bunker or run.
The voice inside knows their names — or knows the safe zone is a trap.
Introduce Shadow properly; Luna's first appearance (medical aid after the
rooftop fallout). Keep the bunker as the central location.

## Production notes (what was actually made)

- Generated video (3 clips, 10 s each, 720x1280, trimmed to 7.5 s): Scenes 1, 2, 4.
- FFmpeg-animated stills (slow push-in / pan, 7.5 s each): Scenes 3, 6, 7, 8 (generated stills) and Scene 5 (pan across Vio's uploaded reference image).
- Scenes 5, 6, 8 video generation failed upstream (HTTP 502 after 3 attempts) and was NOT retried, per instruction; the still-based fallback was used instead.
- Audio: 6 original TTS dialogue lines (Alex = Helio, Max = Bold Flag, Shadow = uneasy low voice), original synthesized ambient bed (low drone + wind + fire hiss), SFX (radio static, door thud, heartbeat thumps, baton whoosh). Mix: 60.0 s, mean -33.4 dB, max -4.8 dB.
- **Audio revision v2 (2026-11-24, Vio: "sound effects too few, add more conversation"):** 18 dialogue lines (12 new, same 3 voices), 20 SFX events (9 new types: helicopter rotor, distant siren, horde groans x2, fire crackle, running footsteps x6, wind rush, baton hum, radio tuning, metal door creak). New mix `assets/audio/mix-v2.wav`: 60.0 s, mean -28.1 dB, max -4.7 dB; per-scene means S1 -28.9, S2 -29.9, S3 -28.7, S4 -30.3, S5 -25.1, S6 -26.8, S7 -28.0, S8 -30.0 dB; no silent gap longer than 1.5 s at -45 dB. Subtitles updated to 18 entries in `subtitles.srt` (v1 kept as `subtitles-v1.srt`). Dropped for crowding (no room without overlap): Scene 2 "How long do we have?" / "Minutes. Not hours." and Scene 4 "Then we move now. Pack light, stay quiet." / "And if the safe zone is a trap?" / "Then we find out together." Video picture unchanged in v2; v2 was verified (60.000 s, 1080x1920, 30 fps, 8 frames inspected, subtitles small/readable and matching the spoken lines) and swapped in as the main final. The v2 mix is built to be reused for the v3 assembly with new motion clips. New TTS files: `assets/audio/alex-no-power.mp3`, `max-hundreds.mp3`, `alex-used-to-be.mp3`, `max-dont-look.mp3`, `max-run.mp3`, `alex-jump-three.mp3`, `max-dont-let-go.mp3`, `alex-i-wont.mp3`, `alex-door-locked.mp3`, `max-just-static.mp3`, `alex-whos-there.mp3`, `max-door-opened.mp3`. Build scripts: `build-audio-v2.sh`, `assemble-v2.sh`.
- Subtitles: burned-in English, SRT in `subtitles.srt`. First assembly rendered subtitles at ~6x intended size (libass default PlayRes); fixed by setting PlayResX=1080/PlayResY=1920 and re-assembled; verified with fresh frames.
- Colour grade: saturation 1.08, contrast 1.05, uniform across all 8 scenes.
- **Motion revision v3 (2026-11-24):** Scenes 6 and 7 got real-motion clips (Alex pulling Max up in rain; bunker door with radio). Scenes 3, 5, 8 failed upstream (HTTP 502). V3 final 35 MB, QC 92/100 (animation 12/15).
- **Motion revision v4 (2026-11-24):** Scenes 5 (rooftop chase, helicopter, zombies) and 8 (bunker door opens, glowing eyes) got real-motion clips on first attempt. Scene 3 failed again (HTTP 502). V4 final 43 MB, QC 94/100 (animation 14/15). Now 7 of 8 scenes are true generated motion; only Scene 3 is still-based.
- **Known character issue (2026-11-24):** Scenes 5 and 8 render Alex/Max with square/blocky cube heads, while Scenes 1, 2, 4, 6, 7 have round heads. Three fix attempts (12:44, 12:53, 14:04 WIB) all failed upstream (HTTP 502 / 503), 0 clips produced, no v5 exists. The strict anatomical consistency rule above is the fix criteria for the next retry.

## QC score: 94/100 (minimum 85 — PASS; v1 was 89, v2 was 90, v3 was 92)

- Story 19/20 — complete 8-beat arc: hook, threat, scale, plan, chase, rescue, locked door, cliffhanger.
- Visual 19/20 — consistent orange-sunset burning-city look, uniform grade; Scene 5 is a pan over the reference image rather than new footage.
- Character Consistency 18/20 — Alex (red bandana + baton) and Max (green vest) identifiable in every scene; deduction: the generator renders them as detailed 3D figures rather than flat line stickmen, and Scenes 5 and 8 render square/blocky heads while other scenes have round heads (known issue, fix pending).
- Animation 14/15 — 7 of 8 scenes are true generated motion; only Scene 3 is a Ken Burns-style still. (Motion revision for Scenes 3, 5, 6, 7, 8 is being handled separately as v3.)
- Audio 10/10 — v2: 18 dialogue lines (every scene has conversation), 20 SFX events, no silent gap over 1.5 s, dialogue scenes clearly audible (per-scene means -25.1 to -30.3 dB). Remaining caveat, not scored down further: voices are TTS stand-ins, not recordings of the locked voice profiles.
- Audience Retention 14/15 — hook in the first 3 seconds, rising danger, hard cliffhanger + "TO BE CONTINUED" end card.

## Deviations from the bible (honest list)

1. Characters are rendered as detailed 3D figures (tactical gear, round heads, detailed faces in close-up) rather than flat line stickmen — this matches Vio's uploaded reference image, which is itself 3D, so the look is consistent across the episode.
2. Scene 6 still adds rain, which was not in the storyboard; it reads as night atmosphere and was kept.
3. Scenes 5, 6, 8 are still-based, not generated video (upstream video failure, see above).
4. Voices are TTS stand-ins (Helio / Bold Flag / uneasy low voice), not recordings of alex_voice_01 / max_voice_01 — those voice profiles have no audio files yet.
