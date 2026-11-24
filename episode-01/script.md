# STICKOCALYPSE — Episode 1: "THE LAST DAY"
## Script (audio revision v2)

- Project: STICKOCALYPSE — Universe: THE LAST SURVIVORS
- Format: 60 seconds, 8 scenes x 7.5 seconds, 9:16 vertical, 1080x1920, 30 FPS
- Language: English dialogue + English subtitles
- Characters in this episode: Alex (CHAR_001), Max (CHAR_002). Shadow (CHAR_004) is only teased: glowing eyes in the dark + one mysterious voice line. Luna (CHAR_003) does not appear.
- Audio v2: 18 dialogue lines (was 6), 20 SFX events (was 5). Video picture unchanged from v1.

### Dialogue (original, in story order)

- ALEX (VO, Scene 1): "Day 47. The city fell in one night." (0.4-3.9 s)
- ALEX (Scene 1): "No power. No signal. Just us." (4.0-7.4 s)
- MAX (Scene 2, breathless): "Alex! They're coming. The horde found the bridge." (8.5-12.2 s)
- MAX (Scene 2): "Hundreds of them. Maybe more." (12.4-14.9 s)
- ALEX (Scene 3): "Look at them. They used to be people." (15.5-18.0 s)
- MAX (Scene 3): "Don't look at their faces. Look at their hands." (18.2-21.7 s)
- ALEX (Scene 4): "The radio said there's a safe zone. We move at dawn." (23.5-26.8 s)
- MAX (Scene 4): "Dawn is too late." (27.0-29.2 s)
- MAX (Scene 5): "Run! Don't stop!" (30.3-32.5 s)
- ALEX (Scene 5): "Left! Jump on three! One... two... three!" (32.7-36.6 s)
- MAX (Scene 6): "Don't let go!" (37.6-39.1 s)
- ALEX (Scene 6, straining): "Hold on! I've got you!" (39.3-41.1 s)
- ALEX (Scene 6): "I won't. Not today." (41.3-43.1 s)
- ALEX (Scene 7): "The door is locked. Try the radio again." (45.3-47.8 s)
- MAX (Scene 7): "Static... wait. Hear that?" (48.0-51.4 s)
- ALEX (Scene 8): "Who's there? Show yourself!" (52.6-54.6 s)
- MAX (Scene 8): "The door opened by itself." (54.7-57.8 s)
- SHADOW (Scene 8, mysterious voice, low): "You shouldn't be here." (57.9-60.0 s)
- On-screen text (Scene 8, end card): "TO BE CONTINUED"

### Dropped lines (v2, crowded scenes — no room without overlapping)

- Scene 2: Alex "How long do we have?" / Max "Minutes. Not hours." — Scene 2 was already full after the warning + "Hundreds of them."
- Scene 4: Alex "Then we move now. Pack light, stay quiet." / Max "And if the safe zone is a trap?" / Alex "Then we find out together." — Scene 4 was already full (safe-zone line + "Dawn is too late" fill 23.5-29.2 s).

### Music / sound design (v2)

- Continuous bed: low drone + wind, orange-sunset city ambience, distant fire crackle.
- New SFX in v2 (all synthesized with ffmpeg lavfi, no copyrighted audio): helicopter rotor (Scene 1), distant siren (Scene 2), horde groans x2 + fire crackle (Scene 3), running footsteps x6 + wind rush on the jump (Scene 5), baton hum (Scene 6), radio tuning (Scene 7), metal door creak (Scene 8).
- Kept from v1: radio static burst (Scene 7), locked-door thud (Scene 7), heartbeat thumps (Scenes 5 and 6), baton-flare whoosh (Scene 6).
- Mix v2 (`mix-v2.wav`): 60.0 s, mean -28.1 dB, max -4.7 dB (v1: mean -33.4 dB). Per-scene mean levels: S1 -28.9, S2 -29.9, S3 -28.7, S4 -30.3, S5 -25.1, S6 -26.8, S7 -28.0, S8 -30.0 dB. No silent gap longer than 1.5 s at -45 dB anywhere in the mix.
- Voices: Alex = Helio (avocado_v2:MAI_03), Max = Bold Flag (avocado_v2:Twenty), Shadow = Calm Bridge, uneasy low (avocado_v2:NoSugar). TTS stand-ins, not recordings of alex_voice_01 / max_voice_01.

### Story beats

Hook (Alex alone, burning city) -> immediate threat (horde found the bridge) -> scale of danger (horde on rooftops) -> plan vs. urgency (safe zone at dawn / too late) -> action (rooftop chase + jump) -> sacrifice / rescue (Max slips, Alex pulls him up) -> false hope (locked bunker door, strange radio signal) -> cliffhanger (door opens by itself, glowing eyes, "You shouldn't be here.")
