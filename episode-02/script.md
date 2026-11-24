# STICKOCALYPSE — Episode 2: "THE DOOR OPENS"
## Script

- Project: STICKOCALYPSE — Universe: THE LAST SURVIVORS
- Format: 60 seconds, 8 scenes x 7.5 seconds, 9:16 vertical, 1080x1920, 30 FPS
- Language: English dialogue + English subtitles
- Characters in this episode: Alex (CHAR_001), Max (CHAR_002), Shadow (CHAR_004 — properly introduced), Luna (CHAR_003 — first appearance).
- Continues directly from Episode 1 v5: Alex and Max stand at the open steel bunker door, glowing eyes in the dark, Shadow's voice: "You shouldn't be here."
- Audio: 17 dialogue lines, at least 10 SFX events. Voices (TTS stand-ins, same as Ep 1): Alex = Helio (avocado_v2:MAI_03), Max = Bold Flag (avocado_v2:Twenty), Shadow = Calm Bridge, uneasy low (avocado_v2:NoSugar). Luna = pick a calm, warm, clear female TTS voice, distinct from the other three, and record which one was used in EPISODE_02.md.

### Dialogue (original, in story order)

- SHADOW (Scene 1, low, stepping out of the dark): "Lower the baton, Alex." (0.5-3.2 s)
- ALEX (Scene 1, shocked): "How do you know my name?" (3.5-6.2 s)
- MAX (Scene 2, urgent): "We run. Right now." (8.0-10.2 s)
- ALEX (Scene 2, firm): "No. Not until he talks." (10.5-13.2 s)
- SHADOW (Scene 3, grave): "The safe zone is a lie." (15.5-18.0 s)
- ALEX (Scene 3): "Then who sent the signal?" (18.3-21.0 s)
- LUNA (Scene 4, calm, kneeling by Max): "Hold still. You're bleeding." (23.0-25.5 s)
- MAX (Scene 4, confused): "Who are you?" (25.8-27.0 s)
- LUNA (Scene 4, steady): "Luna. I heard the radio too." (27.3-29.8 s)
- ALEX (Scene 5, inside the bunker): "You've been hiding here since Day One?" (30.5-33.5 s)
- SHADOW (Scene 5, quiet): "Someone had to keep the door locked." (33.8-36.5 s)
- SHADOW (Scene 6, alarmed): "They followed your light." (38.0-40.5 s)
- LUNA (Scene 6, urgent): "The door won't hold them." (40.8-43.2 s)
- ALEX (Scene 7, pointing down): "There's a tunnel. Under the floor." (45.5-48.2 s)
- MAX (Scene 7, determined): "Then we go. Together." (48.5-51.0 s)
- SHADOW (Scene 8, rushing them down): "Down. Quick. Before—" (53.0-55.0 s)
- RADIO VOICE (Scene 8, distorted, from the radio in Shadow's hand): "Shadow... the trap is set. Bring them to the safe zone." (55.3-59.5 s)
- On-screen text (Scene 8, end card): "TO BE CONTINUED"

### Music / sound design

- Continuous bed: low drone + wind, cold bunker ambience (dripping water, distant metal groans), horde groans rising in Scenes 6-7.
- SFX (all synthesized with ffmpeg lavfi, no copyrighted audio — reuse Ep 1 SFX recipes where they fit): metal door creak (Scene 1, door opening wider), low reversed drone (Scene 1, Shadow steps out), radio static burst + tuning (Scene 3, the lie revealed), bandage rip + soft medical kit click (Scene 4, Luna treats Max), echoing footsteps on concrete (Scene 5, inside the bunker), horde groans x2 + pounding on the steel door (Scene 6), hatch clang + tunnel wind (Scene 7), distorted radio voice effect (Scene 8, radio voice line processed with tremolo/lowpass so it sounds like a transmission, not a clean voice).
- Mix (`mix.wav`): 60.0 s, target mean around -28 dB, max below -4 dB. No silent gap longer than 1.5 s at -45 dB anywhere in the mix.
- Voices are TTS stand-ins, not recordings of the locked voice profiles.

### Story beats

Hook (Shadow steps out and knows Alex's name) -> decision (run or stay) -> revelation (the safe zone is a lie) -> new ally (Luna appears, treats Max) -> the bunker interior (Shadow's secret life since Day One) -> rising danger (the horde followed their light) -> escape plan (the tunnel under the floor) -> cliffhanger (the radio orders Shadow to bring them to the "safe zone" — is Shadow friend or trap?).
