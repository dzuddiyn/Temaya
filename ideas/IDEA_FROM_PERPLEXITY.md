# IDEA — Daripada Sesi Perplexity

- **Sumber:** Sesi brainstorming Perplexity dengan pemilik, 2026-10-03 malam (+08).
- **Jenis:** Koleksi idea/AC sahaja (BUKAN keputusan). Tiada perubahan kepada D-xxx LOCKED.
- **Rujukan kuasa:** AGENTS.md, ZASS_Temaya.md, ZASSIMPLE/DESIGN.md, ZASSIMPLE/ACTION_PLAN.md, ZASSIMPLE/TASKS.md.

---

## 1. Penglihatan stereo & robotik (konteks humanoid)

| Idea / projek | Jenis | Kebaikan untuk projek | Had |
|---|---|---|---|
| Stereo vision (2 kamera) | Konsep | Anggar kedalaman seperti dua mata manusia; radar tidak wajib untuk jarak dekat | Dispariti mengecil pada jarak jauh; bergantung cahaya/tekstur |
| Kedalaman mono (1 kamera, ~5 m) | Perisian | Murah, ringkas | Kurang tepat pada jarak dekat berbanding stereo |
| Stereo bergerak (motion parallax) | Konsep | Satu kamera pada lengan 6 DoF bergerak membentuk baseline | Perlu gerakan terancang |
| Hand-eye calibration (encoder 6 DoF) | Konsep mekatronik | Kedudukan end-effector tepat untuk kalibrasi pandangan | Lengan tidak kesan objek tanpa kamera/sentuhan |
| H2O teleoperation (RGB sahaja) | Projek siap | Kawal humanoid seluruh badan dengan kamera RGB | Peniruan gerakan, bukan autonomi |
| OpenVLA (7B, 970k episod) | Model siap | VLA terbuka, checkpoint di HuggingFace | Prestasi objek baharu terhad |
| NVIDIA GR00T 1.7 (dalam LeRobot) | Model siap | VLA terbuka humanoid; dwi-sistem: VLA perlahan (2–5 Hz) + polisi pantas (200+ Hz) | Ekosistem NVIDIA |
| Gemini Robotics 2 | Model siap | Kawal humanoid penuh kaki ke jari; On-Device adaptasi pantas | Tertutup |
| Isaac Lab 2.3 teleoperation | Platform siap | VR Quest + sarung tangan Manus untuk penjanaan data cepat | Ekosistem NVIDIA |
| Humanoid-Gym | Rangka RL | Sim-to-real zero-shot untuk lokomosi | Fokus lokomosi |
| RealMirror | Platform | Jurang sim-to-real rendah; dakwaan pindahan tanpa penalaan | Dakwaan baru |
| Figure AI (sim RL berjalan) | Kaedah | Ribuan humanoid maya; data bertahun-tahun dalam beberapa jam | Spesifik Figure |

Rumusan idea: rawak terkawal datang daripada sampling (bahasa) dan domain randomization (latihan); kelajuan mesti berlapis (gelung pantas di bawah, gelung perlahan di atas). Evolusi mengesahkan 2 sensor mata cukup untuk kedalaman — ajarannya: sensor khusus untuk fungsi khusus.

---

## 2. Artificial soul — seni bina cadangan (AC, belum LOCK)

Lapisan 1 — Keadaan emosi (teras):
- Model dimensi VAD/PAD (Valence-Arousal-Dominance), bukan label diskret.
- Mood lambat + emosi pantas: contoh terukur berat 70/30 supaya mood bergeser dalam 5–7 iterasi (rasa harian).
- Susut masa (decay) ke garis dasar personaliti LOCKED (hangat, tenang).
- Punca emosi hanya daripada peristiwa self-life atau interaksi semasa pengguna tersebut sahaja — patuh peraturan pengasingan per-pengguna.

Lapisan 2 — Penilaian (appraisal):
- Penilaian peristiwa sebelum mengubah mood (relevan, menyokong nilai, selesai/tidak).
- Episod emosi direkod padat (tekanan → sokongan → penyelesaian) dan mengondisikan jawapan LLM.
- Rujukan: AICO dual emotion system (pengesanan emosi pengguna berasingan daripada simulasi emosi kendiri).

Lapisan 3 — Personaliti & nilai (statik):
- Sudah LOCKED dalam D-019/D-020 sebagai trait vector + sistem nilai + pengesah konsistensi.
- Prinsip: emosi bergerak, personaliti tidak.
- Rujukan struktur: AICO domain Simulation of Personality (trait vector, values, expression mapping, consistency validator).

Lapisan 4 — Memori tiga peringkat (rujukan AICO, model CLS sains kognitif):
- Memori kerja pantas (LMDB) — sembang terkini, cepat lupa.
- Memori semantik (ChromaDB + BM25) — fakta/nota jangka panjang.
- Graf pengetahuan (libSQL) — orang, peristiwa, hubungan, tepi bermasa.
- Adaptive Memory System menentukan naik-taraf pantas → lambat.
- Untuk Temaya: struktur sama, dua ruang nama — stor self-life dan stor per-pengguna — memenuhi model pengasingan LOCKED.

Lapisan 5 — Agency (kehendak):
- Dorongan dalaman supaya Temaya tak sekadar membalas: sistem matlamat (jana/keutamaan/jejak), enjin rasa ingin tahu, pengurus inisiatif yang boleh memulakan perbualan.
- Menjawab syarat "rawak tetapi tidak lari konteks": inisiatif rawak bergerak dalam watak persona.

---

## 3. Pelaksanaan — OpenClaw skill sedia ada

- Emotion Engine (PioneerJeff Labs): skill OpenClaw menyimpan keadaan PAD + pekali kepercayaan bergerak perlahan + appraisal deterministik + memori emosi sedar situasi.
- Sejajar dengan OpenClaw-native-first (rujuk D-022):
  1. Pasang Emotion Engine sebagai skill OpenClaw (Fasa 1, pembuktian).
  2. Bina stor self-life berasingan (D-021–D-026).
  3. Tambah subsistem tersuai hanya jika had skill memaksa.
- AICO (MIT) kekal rujukan seni bina: bas mesej CurveZMQ, modelservice berasingan, hirarki Sistem → Subsistem → Domain → Modul → Komponen. Ambil reka bentuk sebagai contoh, bukan keseluruhan sistem.

---

## 4. Projek memori & persona lain yang disemak

| Projek | Fungsi | Catatan |
|---|---|---|
| AICO | Pendamping AI sepenuh (local-first) | Emosi suara/wajah & Big Five/HEXACO belum siap |
| AffectiveBrain | Lapisan afektif VAD untuk LLM | Ringan, boleh pasang pada sistem sedia ada |
| Amica | Antara muka 3D (suara, speech recognition, emosi) | Fokus UI, bukan otak |
| Mem0 | Memori jangka panjang ejen | Serasi LangGraph/AutoGen/CrewAI; bukan self-life |
| Memary | Memori gaya manusia untuk agen | Alternatif sedang disemak |
| GitHub topic emotional-ai | Enjin persona (personaliti dari dorongan dalaman) | Kualiti projek berbeza-beza |

---

## 5. Status dokumen

- Idea dalam fail ini: AC/idea sahaja. Tiada yang LOCKED di sini.
- Fail ini dijana AI (Perplexity) atas arahan pemilik; belum disahkan semula oleh pemilik.
