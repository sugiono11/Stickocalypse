# STICKOCALYPSE — Episode 2: "THE DOOR OPENS"
## Continuity record

- Universe: THE LAST SURVIVORS
- Episode: 2 of the series
- Duration: 60 seconds (8 scenes x 7.5 s), 9:16, 1080x1920, 30 FPS
- Final video: `stickocalypse-ep02-1080x1920.mp4` (30 MB, H.264/AAC) — **v3** (see below). V1 (28 MB) and v2 (32 MB) kept as `stickocalypse-ep02-1080x1920-v1.mp4` / `-v2.mp4`.
- Quality score: 97/100 (v3; v2 was 96/100, v1 was 91/100 — see QC section)
- Status: complete, verified with ffprobe (60.000 s, 1080x1920, 30 fps, audio present) and full decode test; one frame per scene inspected.

## Strict anatomical consistency (Vio, 2026-11-24)

Use the exact same approved 3D stickman character from the supplied reference image — the reference is the absolute source of truth. Preserve the original head size, head shape, shoulder width, torso length, arm length, leg length, limb thickness, eye placement and overall silhouette. The character must retain the exact same body model throughout the entire animation. Animate only the required movements; natural body movement is allowed, but do not redesign, stretch, shrink, morph or deform the character. Maintain the same clothing, accessories and visual identity. Use physically coherent movement with consistent anatomy across all frames. ROUND spherical heads, NOT square, NOT blocky, NOT cube-shaped.

## Summary

Shadow steps out of the bunker darkness — and he knows Alex's name. Max
wants to run; Alex demands answers. Shadow reveals the safe zone is a lie.
Then Luna appears from the shadows and bandages Max's bleeding arm: she
heard the radio too. Inside the bunker, Shadow shows them his home since
Day One — but the horde followed Alex's baton light, and the steel door
won't hold. They escape down a tunnel under the floor. As they descend, the
radio in Shadow's hand crackles with an order: "Shadow... the trap is set.
Bring them to the safe zone." Is Shadow a friend — or the trap?

## Timeline (story)

1. Shadow steps out of the bunker dark: "Lower the baton, Alex." Alex: "How do you know my name?"
2. Max wants to run right now; Alex refuses to leave until Shadow talks.
3. Shadow reveals: "The safe zone is a lie." Alex: "Then who sent the signal?"
4. Luna appears and treats Max's bleeding arm from the rooftop fall: "Hold still. You're bleeding." / "Luna. I heard the radio too."
5. Inside the bunker: supplies, wall map, radio equipment. Shadow has lived here since Day One: "Someone had to keep the door locked."
6. The horde followed the baton light; the steel door rattles and bulges. Luna: "The door won't hold them."
7. Escape plan: a tunnel under the floor. Max: "Then we go. Together."
8. Descending the ladder, the radio orders Shadow: "Shadow... the trap is set. Bring them to the safe zone."

## Locations

- Steel bunker door ("RESTRICTED - LEVEL 3 - NO ENTRY"), open, fog rolling out
- Bunker interior: concrete room, supply shelves, pinned wall map, old radio equipment, candles
- Floor hatch + tunnel ladder descending into the dark
- Burning city at night outside (embers, orange firelight)

## Characters

- Alex (CHAR_001): protagonist. Black stickman, round head, red bandana, dark tactical outfit, glowing orange baton. Brave, intelligent, protective.
- Max (CHAR_002): defender. Dark charcoal stickman, round head, broad shoulders, dark green tactical vest. Loyal, strong, protective. Hurt arm from the Episode 1 rooftop fall; Luna bandages it.
- Shadow (CHAR_004): PROPERLY INTRODUCED. Dark black silhouette, hooded clothing, glowing eyes, lightweight equipment, carries the old radio. Quiet, mysterious, observant, secretive. Has lived in the bunker since Day One. His loyalty is now in doubt: the radio orders him to bring Alex and Max to the "safe zone".
- Luna (CHAR_003): FIRST APPEARANCE. Black stickman, round head WITH LONG DARK HAIR TIED IN A PONYTAIL (permanent design since v3, Vio 2026-11-24), dark survival jacket, medical backpack with white cross, NEVER wears Alex's red bandana (the bandana is Alex's only). Intelligent, calm, resourceful, compassionate. Heard the radio signal too; found the bunker on her own.

## Relationships

- Alex and Max: survival partners. Alex leads and plans; Max defends and warns. Max trusts Alex's call to stay and hear Shadow out.
- Shadow and the group: uneasy ally. He saved them a hiding place and told them the truth about the safe zone — but he takes orders from the radio voice.
- Luna and the group: new ally. She treats Max without being asked and joins the escape without hesitation.
- Luna and Shadow: strangers who both found the bunker through the radio signal.

## Unresolved mysteries (for Episode 3+)

- Who is the voice on the radio giving Shadow orders — and what is the trap?
- Is Shadow a friend, a prisoner of the voice, or the trap itself?
- What is down the tunnel — and where does it lead?
- Where is the safe zone, and is it real? (Now known: the safe-zone message is a lie / lure.)
- What happened on the night the city fell (Day 1)?
- Are there other survivors besides Luna — and who else heard the radio?

## Next episode direction

Episode 3: THE TUNNEL. Alex, Max, Luna and Shadow descend into the dark —
but the tunnel is not empty. The voice on the radio knows the way out, and
the horde is already inside. Trust breaks: Alex confronts Shadow about the
order. Someone gets left behind — or someone stays behind on purpose.

## Production notes (what was actually made)

- Generated video (4 clips, 10 s each, 720x1280 vertical, trimmed to 7.5 s): Scenes 1, 4, 5, 6. Video budget: 6/6 successful `media.generate_video` calls used, exactly at the cap. No upstream failures (no HTTP 502/503).
- FFmpeg-animated stills (slow push-in / zoompan, 7.5 s each): Scenes 2, 3, 7, 8 (generated stills). Scene 7 was dropped from video to pay for the Scene 6 re-roll within the 6-call cap. Scene 8 video was rejected (see below) and replaced with an animated still.
- Scene 6 v1 REJECTED: square orange cube-headed character in the background, and Shadow rendered as a spiky hedgehog-like animal. Re-rolled once with an explicit "only four humanoid stickmen, no animals, no hedgehog, no cube characters" prompt; re-roll accepted (round heads, cube character gone).
- Scene 8 video REJECTED (character break, not square heads): heads were round and the radio close-up was excellent, but Shadow was again rendered as a hedgehog-like animal (spiky quills, red stripe, pointed ears, muzzle) in the close-ups — the generator persistently reads the name "Shadow" that way in video mode. No video calls remained for a re-roll, so a generated still (correct hooded humanoid Shadow) was substituted. The rejected S8 video is kept in `assets/video/` (unused).
- Audio: 17 original TTS dialogue lines (every scene has conversation), 17 SFX placements / 12 types, all synthesized with ffmpeg lavfi. Mix `assets/audio/mix.wav`: 60.000 s, mean -29.0 dB, max -4.9 dB; per-scene means S1 -29.5, S2 -30.3, S3 -28.8, S4 -25.3, S5 -29.2, S6 -30.2, S7 -32.0, S8 -30.3 dB; no silent gap longer than 1.5 s at -45 dB (checked at 0.5 s too). Voices: Alex = Helio (avocado_v2:MAI_03), Max = Bold Flag (avocado_v2:Twenty), Shadow = Calm Bridge, uneasy low (avocado_v2:NoSugar), Luna = Aria (avocado_v2:MAI_01) — calm, warm, clear female voice, distinct from the other three. Radio voice line is the Shadow voice processed into a distorted transmission (highpass 300 Hz, lowpass 2800 Hz, tremolo 7 Hz depth 0.6). Subtitle timings updated to actual TTS durations (5 entries shifted: #8, #9, #11, #15, #17); original script timings saved as `subtitles-script.srt`. Build scripts: `build-audio.sh`, `assemble.sh`, `build-scenes.sh`.
- **Revision v3 (2026-11-24, Vio: "give the woman hair — there is a scene where she has no hair — and fix subtitles that stack/overlap"):** LUNA'S HAIR — new permanent design, authorized by Vio: long dark hair tied in a ponytail, no red bandana. Scenes 4, 5, 6, 7, 8 regenerated as true video (6 successful video calls total, exactly at cap: Scene 6 v1 was REJECTED — Alex rendered with a square yellow cube head — and re-rolled once with stronger round-head wording; re-roll accepted, all heads round). All 5 v3 clips: 10.0 s, vertical 704x1248, 24 fps, Luna's ponytail visible in every scene she appears in, no bandana on her, hooded figure humanoid (the name "Shadow" was never used in prompts). SUBTITLES — real overlap fixed: entry 7 "Hold still. You're bleeding." ended 25.5 while entry 8 "Who are you?" started 25.2 (0.3 s stacked); entry 7 now ends 25.0 (0.2 s gap) and entry 16 now ends 54.9 instead of 55.0 (0.1 s gap before entry 17); whole SRT re-checked programmatically — 17 entries, zero overlaps. Old SRT kept as `subtitles-v2.srt`. Audio unchanged (louder mix-v2.wav). V3 final: 31,416,502 bytes, 60.000 s, 1080x1920, 30 fps, decode OK, one frame per scene inspected plus a frame at 25.35 s showing only the single subtitle "Who are you?". QC 97/100 (character consistency 20/20 — bandana slip resolved). Build script: `assemble-v3.sh`.
- Subtitles: burned-in English, SRT in `subtitles.srt`, same PlayResX=1080/PlayResY=1920, FontSize 52 fix as Episode 1. Verified readable in final frames (Scenes 1, 4, 8 checked).
- Colour grade: saturation 1.08, contrast 1.05, uniform across all 8 scenes (same as Episode 1).
- **Revision v2 (2026-11-24, Vio: "some scenes don't move and the sound is too quiet — fix it so all scenes move"):** MOTION — Scenes 2, 3, 7, 8 regenerated as true video (6 successful video calls total: Scene 2 needed one re-roll — v1 drifted into a sunset rooftop run at ~5 s; Scene 8 needed one re-roll — v1 rendered the hooded figure with a realistic human face in the extreme close-up; both re-rolls accepted). The name "Shadow" was never used in any v2 prompt ("the hooded figure" instead) — no hedgehog/animal renders this time. All 4 v2 clips: 10.0 s, vertical (720x1280, Scene 8 704x1248), 24 fps, heads round, hooded figure humanoid with face in shadow. AUDIO — mix remixed from the same stems (no re-recording): loudnorm to about -14 LUFS. v1 mix: integrated -23.17 LUFS, true peak -3.08 dBTP, mean -29.0 dB. v2 mix (`assets/audio/mix-v2.wav`): integrated -15.47 LUFS, true peak -0.99 dBTP, mean -19.9 dB, max -1.0 dB, LRA 10.5 — about 9 dB louder, no clipping; the -14 target could not be hit exactly without heavy compression because a few loud peaks (door pounding, hatch clang) cap the linear gain, so -15.5 LUFS is the clean maximum. Per-scene means v2: S1 -19.8, S2 -20.3, S3 -19.8, S4 -18.4, S5 -20.9, S6 -19.2, S7 -21.2, S8 -20.3 dB; no silent gaps. V2 final: 33,721,892 bytes, 60.000 s, 1080x1920, 30 fps, decode OK, one frame per scene inspected, final-track loudness -15.54 LUFS / TP -0.84 dB / mean -19.9 dB. **All 8 scenes are now true generated motion.** QC 96/100 (animation 15/15, character 19/20). Build script: `assemble-v2.sh`.

## QC score: 97/100 (minimum 85 — PASS; v1 was 91/100, v2 was 96/100)

- Story 19/20 — complete 8-beat arc: hook (knows our names), decision, revelation (safe zone is a lie), new ally (Luna), bunker interior, rising danger (horde followed the light), escape plan (tunnel), cliffhanger (radio order). Deduct 1: who gives Shadow orders is deliberately deferred to Episode 3.
- Visual 19/20 — consistent cold blue-grey bunker look, uniform grade; all scenes read as one film.
- Character Consistency 20/20 — round heads in every scene, all four characters identifiable, hooded figure humanoid with face in shadow in all scenes; Luna now has her long dark ponytail in every scene she appears in and never wears the red bandana (v3 fixed the Scene 4 slip).
- Animation 15/15 — v2: all 8 scenes are true generated motion (1, 4, 5, 6 from v1; 2, 3, 7, 8 new v2 clips). No still-based scenes remain.
- Audio 10/10 — v2: same 17 dialogue lines and 17 SFX placements, now about 9 dB louder (integrated -15.5 LUFS, true peak -1.0 dB, no clipping), no silent gap over 1.5 s. Remaining caveat, not scored down further: voices are TTS stand-ins, not recordings of the locked voice profiles.
- Audience Retention 14/15 — hook in the first 3 seconds, rising danger, hard cliffhanger + "TO BE CONTINUED" end card.

## Deviations from the bible (honest list)

1. Characters are rendered as detailed 3D figures (tactical gear, round heads, detailed faces in close-up) rather than flat line stickmen — this matches Vio's uploaded reference image, which is itself 3D, so the look is consistent across the episode (same as Episode 1).
2. Luna's red bandana slip (v1/v2 Scene 4 close-up) — FIXED in v3: Luna now has long dark hair tied in a ponytail and never wears the bandana; the bandana is Alex's only. This is her permanent design going forward.
3. Shadow's hood renders pointed/spiky in Scene 6, and his video-mode renders twice became a hedgehog-like animal character (Scene 6 v1 and Scene 8 video — both rejected; Scene 8 replaced with a correct still). The name "Shadow" persistently misleads the video generator; stills render him correctly as a hooded humanoid.
3. Shadow's hood renders pointed/spiky in Scene 6, and his video-mode renders twice became a hedgehog-like animal character (Scene 6 v1 and Scene 8 video — both rejected; Scene 8 replaced with a correct still). The name "Shadow" persistently misleads the video generator; stills render him correctly as a hooded humanoid.
4. V2 fixes: all 8 scenes are now true video; the hooded figure stayed humanoid in all v2 generations because the name "Shadow" was never used in prompts. Two v2 re-rolls were needed: Scene 2 v1 drifted into a sunset rooftop run (location break) and Scene 8 v1 gave the hooded figure a realistic human face in the extreme close-up (character break); both were rejected and re-rolled within the 6-video cap. Luna's red bandana slip was fixed in v3 (ponytail design).
5. Voices are TTS stand-ins (Helio / Bold Flag / Calm Bridge / Aria), not recordings of alex_voice_01 / max_voice_01 / shadow_voice_01 / luna_voice_01 — those voice profiles have no audio files yet.
