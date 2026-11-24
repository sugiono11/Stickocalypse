# STICKOCALYPSE — Rencana Database

Universe: **THE LAST SURVIVORS**
Project: STICKOCALYPSE
Current episode: 1
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
| CHAR_003 | Luna | black stickman | distinctive expressive eyes | dark survival jacket | medical backpack | intelligent, calm, resourceful, compassionate | luna_voice_01 | null — belum ada |
| CHAR_004 | Shadow | dark black silhouette | glowing eyes | hooded clothing | lightweight equipment | quiet, mysterious, observant, secretive | shadow_voice_01 | null — belum ada |

Catatan Episode 1: file `project.json` saat ini baru berisi Alex dan Max.
Luna dan Shadow tetap tercatat di sini sebagai karakter permanen Master Brain,
untuk dikenalkan di episode berikutnya.

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

Episode 1: belum ada judul, ringkasan, atau event — masih pending.

## 4. PRODUCTION_MEMORY

Per episode:
- script_status, image_status, video_status, audio_status
- editing_status, export_status, quality_score, final_file_location

Episode 1 saat ini: image_status pending, video_status pending,
audio_status pending, render_status pending, quality_score null,
final_video null.

## 5. STYLE_MEMORY

- character design references
- lighting style, color palette
- camera language, animation style
- subtitle design, sound identity

Aturan kunci:
- Visual consistency wajib — setiap scene harus terlihat seperti satu film yang sama.
- Jangan ubah identitas visual secara acak.
- Gunakan reference image untuk image dan video generation.
- Pertahankan voice identity yang sama untuk karakter yang berulang.
- Simpan memory setelah setiap episode selesai. Jangan timpa record episode sebelumnya.
