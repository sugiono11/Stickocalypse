# STICKOCALYPSE — Rencana Database

Universe: **THE LAST SURVIVORS**
Project: STICKOCALYPSE
Current episode: 2
Visual style: cinematic_3d
Aspect ratio: 9:16
Duration: 60 seconds, 8 scenes x 7.5 seconds

Dokumen ini adalah **rencana database** (bukan file produksi final).
Tujuannya: mengunci karakter dan suara supaya tidak berubah antar episode.

## 1. CHARACTER_MEMORY

Satu record per karakter. Desain tidak boleh diubah tanpa izin Vio.

| id | name | body | eyes | clothing | accessory | personality | voice_profile | reference_image |
|---|---|---|---|---|---|---|---|---|
| CHAR_001 | Alex | black stickman | expressive white eyes | dark tactical outfit | red bandana | brave, intelligent, protective | alex_voice_01 | null — belum ada |
| CHAR_002 | Max | dark charcoal stickman | — | dark green tactical vest | — | loyal, strong, protective | max_voice_01 | null — belum ada |
| CHAR_003 | Luna | black stickman | distinctive expressive eyes | dark survival jacket | medical backpack; long dark hair tied in a ponytail (permanent design since Ep 2 v3, Vio 2026-11-24), NEVER wears a red bandana | intelligent, calm, resourceful, compassionate | luna_voice_01 | null — belum ada |
| CHAR_004 | Shadow | dark black silhouette | glowing eyes | hooded clothing | lightweight equipment | quiet, mysterious, observant, secretive | shadow_voice_01 | null — belum ada |

Catatan Episode 2: `project.json` kini berisi keempat karakter
(Alex, Max, Luna, Shadow) dan `current_episode` 2.

Field wajib per karakter:
- character_id, name, appearance, clothing, personality
- voice_identity / voice_profile — harus sama di setiap episode
- reference_image — diisi begitu gambar referensi dibuat
- relationships, character_development

## 2. WORLD_MEMORY

- locations, geography, environment, weather
- apocalypse conditions, important objects
- safe zones, dangerous zones

Saat ini masih kosong (story_memory di `project.json`: timeline, locations,
important_events, unresolved_mysteries, relationships semuanya []).

## 3. STORY_MEMORY

Per episode:
- episode_number, episode_title, summary, timeline
- main_events, character_appearances
- unresolved_mysteries, next_episode_direction

Episode 1 "THE LAST DAY" (2026-11-24, QC 96/100 v5): Alex di atap kota
terbakar, Max memperingatkan horde menemukan jembatan; mereka lari di atap,
melompat antar gedung, dan mencapai pintu bunker — pintu terbuka sendiri.

Episode 2 "THE DOOR OPENS" (2026-11-24, QC 97/100 v3; v1 91, v2 96): Shadow keluar dari
bunker dan tahu nama Alex; safe zone terungkap sebagai jebakan/kebohongan;
Luna muncul pertama kali dan membalut lengan Max yang berdarah; interior
bunker terungkap (Shadow tinggal di sana sejak Day One); horde mengikuti
cahaya baton ke bunker; pelarian lewat terowongan di bawah lantai;
cliffhanger: radio memerintah Shadow, "the trap is set. Bring them to the
safe zone." Karakter baru tercatat: Luna (CHAR_003) dan Shadow (CHAR_004)
kini masuk `project.json` (current_episode 2).

## 4. PRODUCTION_MEMORY

Per episode:
- script_status, image_status, video_status, audio_status
- editing_status, export_status, quality_score, final_file_location

Episode 1: v5 selesai, QC 96/100, 7 dari 8 scene video asli (Scene 3
masih still), file final `episode-01/stickocalypse-ep01-the-last-day-1080x1920.mp4`.

Episode 2: v3 selesai, QC 97/100, 8 dari 8 scene video asli, audio
-15,5 LUFS, file final `episode-02/stickocalypse-ep02-1080x1920.mp4`.

## 5. STYLE_MEMORY

- character design references
- lighting style, color palette
- camera language, animation style
- subtitle design, sound identity

Aturan kunci:
- STRICT ANATOMICAL CONSISTENCY (Vio, 2026-11-24): use the exact same approved 3D stickman character from the supplied reference image — the reference is the absolute source of truth. Preserve the original head size, head shape, shoulder width, torso length, arm length, leg length, limb thickness, eye placement and overall silhouette. The character must retain the exact same body model throughout the entire animation. Animate only the required movements; natural body movement is allowed, but do not redesign, stretch, shrink, morph or deform the character. Maintain the same clothing, accessories and visual identity. Use physically coherent movement with consistent anatomy across all frames.
- Visual consistency wajib — setiap scene harus terlihat seperti satu film yang sama.
- Jangan ubah identitas visual secara acak.
- Gunakan reference image untuk image dan video generation.
- Pertahankan voice identity yang sama untuk karakter yang berulang.
- Simpan memory setelah setiap episode selesai. Jangan timpa record episode sebelumnya.
