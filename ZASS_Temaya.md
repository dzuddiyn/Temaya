# ZASS — Temaya

**Project:** Temaya / `dzuddiyn_family_assistant`  
**Repository:** `dzuddiyn/Temaya`  
**Methodology:** ZASSIMPLE v0.1.6  
**Document version:** 0.1.0  
**Date:** 2026-09-30  
**Status:** DISCOVERY — idea dump dahulu, padanan kemudian  
**Owner:** Project Owner

> Fikir santai. Rekod yang penting. Setuju jadi calon. Lock jadi keputusan. Architecture hanya apabila disahkan.

---

## SOURCE OF TRUTH STATUS

Fail ini ialah source of truth perbincangan projek Temaya selepas commit pertama.

Aturan:
- Jangan invent fakta.
- Bezakan `EXPLICIT`, `INFERRED`, dan `UNKNOWN`.
- Cadangan AI tidak menjadi keputusan secara senyap.
- Persetujuan boleh menjadi `AC` jika sasaran jelas.
- Hanya arahan `LOCK` / `LOCK DECISION` boleh menghasilkan `D-xxx | LOCKED`.
- Architecture belum disahkan.
- Fasa semasa: **lambak idea dahulu; bentuk kemungkinan padanan kemudian**.

---

# RAW IDEA

## RAW-001 — OpenClaw

**Source:** EXPLICIT

> "dzuddiyn_family_assistant guna OpenClaw"

---

## RAW-002 — Adapt Dzuddiyn Library

**Source:** EXPLICIT

> "ambil idea dari Dzuddiyn Library (DL). tapi bukan rule. adapt dengan OpenClaw. bagi cadangan elok urus library personal aku (ko bahasakan diri saya & awak) baik guna App Script atau direct agent OpenClaw, anggap library besar, library ahli keluarga lain mula dari kosong"

---

## RAW-003 — Mini PC wajib

**Source:** EXPLICIT

> "wajib guna mini PC, host HA & OpenClaw + semua yang perlu"

---

## RAW-004 — Cara discovery projek

**Source:** EXPLICIT

> "saya nak lambak idea dulu, lepastu baru bentuk kemungkinan padanan."

---

## RAW-005 — Meta AI proposal

**Source:** EXPLICIT — external proposal supplied by owner  
**Owner acceptance of details:** UNKNOWN

Owner membekalkan proposal Meta AI yang merangkumi:
- N100 mini PC sebagai family AI hub.
- Home Assistant + OpenClaw.
- Ryzen workstation sebagai heavy AI server.
- faster-whisper, TTS, wake word dan speaker identification.
- memory/per-user separation.
- smart speaker Puspa.
- personalised ball robots.
- e-Paper face.
- Qi docking.
- WhatsApp private assistant.
- WhatsApp sekolah silent listener/summarizer.
- local-first memory/voice concept.

Proposal ini ialah **reference input**, bukan architecture yang diterima secara automatik.

---

## RAW-006 — Gemini proposal

**Source:** EXPLICIT — external proposal supplied by owner  
**Owner acceptance of details:** UNKNOWN

Owner membekalkan proposal Gemini tentang:
- Home Assistant + LLM/tool calling sebagai home automation agent.
- Extended OpenAI Conversation.
- HA native LLM Conversation.
- local LLM melalui Ollama / LocalAI / LM Studio.
- external agent framework seperti AutoGen / LangChain / CrewAI.
- WhatsApp sebagai input untuk grocery, todo, reminders dan calendar.
- Node-RED / HA Automation sebagai pemproses.
- Green API / Whapi / UltraMsg sebagai contoh WhatsApp gateway.

Proposal ini ialah **idea dump/reference**, bukan dependency Temaya.

---

# WHY

## WHY-001
**Source:** EXPLICIT

Personal library awak sudah besar dan Temaya perlu mengambil keadaan itu kira.

## WHY-002
**Source:** EXPLICIT

Library ahli keluarga lain bermula dari kosong.

## WHY-003
**Source:** EXPLICIT

Idea Dzuddiyn Library mahu digunakan, tetapi bukan sebagai rule rigid Temaya.

## WHY-004
**Source:** INFERRED — perlu validation kemudian

Temaya berpotensi menjadi family AI hub yang menghubungkan knowledge/library, interaksi keluarga dan household operations.

---

# GOALS

## G-001 | ACTIVE
**Source:** EXPLICIT

Gunakan OpenClaw untuk `dzuddiyn_family_assistant`.

## G-002 | ACTIVE
**Source:** EXPLICIT

Gunakan mini PC sebagai host wajib untuk Home Assistant, OpenClaw dan komponen yang diperlukan.

## G-003 | ACTIVE
**Source:** EXPLICIT

Adapt prinsip berguna Dzuddiyn Library tanpa menjadikannya rule mutlak.

## G-004 | ACTIVE
**Source:** EXPLICIT

Cari cara sesuai mengurus personal library yang besar menggunakan OpenClaw, Apps Script atau gabungan yang sesuai.

## G-005 | ACTIVE
**Source:** EXPLICIT

Benarkan library ahli keluarga lain bermula kosong dan berkembang kemudian.

## G-006 | ACTIVE
**Source:** EXPLICIT

Dalam fasa semasa, utamakan **idea capture** sebelum memilih padanan architecture.

---

# NON-GOALS

## NG-001
**Source:** EXPLICIT

Tidak wajib menyalin semua struktur/rule Dzuddiyn Library.

## NG-002
**Source:** INFERRED — agreed candidate, belum LOCKED

Tidak perlu menyusun semula seluruh legacy personal library sebelum Temaya boleh mula memberi nilai.

## NG-003
**Source:** INFERRED — agreed candidate, belum LOCKED

OpenClaw memory/workspace tidak semestinya menggantikan seluruh Dzuddiyn Library.

## NG-004
**Source:** EXPLICIT from current discovery mode

Belum memilih final architecture ketika idea masih sedang dilambakkan.

---

# CONSTRAINTS

## C-001
**Source:** EXPLICIT

Mini PC wajib digunakan.

## C-002
**Source:** EXPLICIT

Mini PC mesti host Home Assistant dan OpenClaw serta komponen yang diperlukan.

## C-003
**Source:** EXPLICIT

OpenClaw ialah runtime/platform family assistant yang mahu digunakan.

## C-004
**Source:** EXPLICIT

Personal library awak dianggap besar.

## C-005
**Source:** EXPLICIT

Library ahli keluarga lain bermula kosong.

## C-006
**Source:** EXPLICIT

Dzuddiyn Library ialah sumber idea/prinsip, bukan rule wajib.

## C-007
**Source:** UNKNOWN

Spesifikasi sebenar mini PC belum direkodkan sebagai keputusan Temaya.

---

# AGREED CANDIDATES

> `AC` = arah yang dipersetujui untuk diteroka. BUKAN keputusan LOCKED.

## AC-001 | AGREED
**Source:** EXPLICIT

Temaya / `dzuddiyn_family_assistant` menggunakan OpenClaw.

## AC-002 | AGREED
**Source:** EXPLICIT

Mini PC menjadi mandatory host bagi Home Assistant, OpenClaw dan komponen asas yang diperlukan.

**Open boundary:** deployment model belum diputuskan.

## AC-003 | AGREED
**Source:** EXPLICIT

Temaya mengambil prinsip Dzuddiyn Library tetapi tidak mewarisi semua rule DL secara rigid.

## AC-004 | AGREED
**Source:** EXPLICIT

Architecture library mesti mengambil kira dua keadaan:
1. personal library awak sudah besar;
2. library ahli keluarga lain bermula kosong.

## AC-005 | AGREED
**Source:** EXPLICIT

Workflow discovery projek: **lambak idea dahulu, kemudian baru bentuk kemungkinan padanan**.

## AC-006 | AGREED
**Source:** INFERRED from previous owner agreement

OpenClaw diteroka sebagai primary intelligence/librarian layer; Apps Script kekal sebagai helper jika sesuatu kerja Google-specific lebih sesuai dibuat secara deterministic.

## AC-007 | AGREED
**Source:** INFERRED from previous owner agreement

Legacy personal library diteroka melalui index/search dahulu, bukan terus reorganize semua bahan.

## AC-008 | AGREED
**Source:** INFERRED from previous owner agreement

Home Assistant sepatutnya kekal mampu menjalankan fungsi automasi asas walaupun OpenClaw/LLM gagal.

## AC-009 | AGREED
**Source:** INFERRED from previous owner agreement

Sensitive material seperti credentials, auth state dan voice embeddings patut dipisahkan daripada ordinary searchable library.

## AC-010 | AGREED
**Source:** INFERRED from previous owner agreement

Per-user isolation untuk ahli keluarga ialah arah yang patut diteroka.

---

# IDEA LOG

## I-001 | OPEN
**Source:** INFERRED

OpenClaw sebagai intelligence/librarian layer, bukan tempat menyimpan semua dokumen sebenar.

## I-002 | OPEN
**Source:** INFERRED

Apps Script sebagai helper untuk inventory, metadata, trigger atau housekeeping Google Drive yang deterministic.

## I-003 | OPEN
**Source:** INFERRED

Legacy library: index/search dahulu; physical reorganization hanya jika kemudian terbukti perlu.

## I-004 | OPEN
**Source:** INFERRED

Bezakan logical knowledge boundary:
- Personal Library
- Individual Family Library
- Family Shared

## I-005 | OPEN
**Source:** INFERRED

Gunakan OpenClaw identity/workspace/agent isolation jika ia sesuai selepas mapping dibuat.

## I-006 | OPEN
**Source:** INFERRED

Candidate host model:
```text
Mini PC
└── Hypervisor
    ├── Home Assistant OS VM
    └── Linux AI VM
        ├── OpenClaw
        ├── MQTT
        ├── voice services
        └── library/index services
```

**Proxmox/VM model belum LOCKED.**

## I-007 | OPEN
**Source:** INFERRED

Home Assistant sebagai deterministic execution layer; OpenClaw/LLM sebagai interpretation/reasoning layer.

## I-008 | OPEN
**Source:** EXPLICIT as Meta AI proposal; owner acceptance UNKNOWN

Ryzen workstation sebagai optional heavy compute server untuk model/RAG/voice workload.

## I-009 | OPEN
**Source:** EXPLICIT as Meta AI proposal; owner acceptance UNKNOWN

Voice interface dengan wake word, STT dan TTS.

## I-010 | OPEN
**Source:** INFERRED

Local-first voice stack boleh dipisahkan kepada lightweight always-on workload di mini PC dan heavier workload di Ryzen.

## I-011 | OPEN
**Source:** INFERRED

Sensitive data boleh mempunyai private local vault berasingan daripada searchable library.

## I-012 | OPEN
**Source:** EXPLICIT as Meta AI proposal; owner acceptance UNKNOWN

WhatsApp boleh menjadi interface Temaya.

## I-013 | OPEN
**Source:** INFERRED

Cuba native OpenClaw account/channel routing dahulu sebelum membina custom WhatsApp bridge.

## I-014 | OPEN
**Source:** EXPLICIT as Meta AI proposal; owner acceptance UNKNOWN

School channel sebagai silent reader/summarizer yang mengeluarkan homework, exam, fees, events dan notices.

## I-015 | OPEN
**Source:** INFERRED

Dedicated device identity + wake word boleh menjadi signal identity utama; speaker ID sebagai secondary signal.

## I-016 | OPEN
**Source:** EXPLICIT as Meta AI proposal; owner acceptance UNKNOWN

Puspa smart speaker dan personalised robot/device sebagai kemungkinan physical interface.

## I-017 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

Home Assistant + LLM/tool calling boleh bertindak sebagai `Home Automation Agent`.

Candidates supplied:
- HA native LLM Conversation
- Extended OpenAI Conversation
- Ollama / LocalAI / LM Studio
- LangChain / CrewAI / AutoGen

## I-018 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

Gabungkan deterministic HA automation dengan LLM/agent reasoning.

## I-019 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

HA boleh menjadi execution layer untuk household action, manakala AI menafsir intent dan memilih action.

## I-020 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

WhatsApp sebagai household input bagi grocery, reminder, calendar dan natural-language command.

## I-021 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

Operational household stores yang mungkin berbeza daripada long-term library:
- Shopping/Grocery
- To-Do
- Calendar
- Reminder

## I-022 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

Natural-language message boleh diparse kepada structured action menggunakan rule-based parser, LLM parser atau gabungan.

## I-023 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

Node-RED atau HA native automation sebagai candidate orchestration layer bagi sesetengah workflow.

## I-024 | OPEN
**Source:** EXPLICIT — Gemini proposal; owner acceptance UNKNOWN

Local LLM sebagai candidate untuk privacy/offline operation.

---

# OPEN QUESTIONS

## Q-001 | OPEN
**Source:** UNKNOWN

Apakah host architecture mini PC yang akhirnya dipilih?

## Q-002 | OPEN
**Source:** UNKNOWN

Apakah boundary sebenar antara direct OpenClaw library access dan Apps Script helper?

## Q-003 | OPEN
**Source:** UNKNOWN

Di manakah authoritative personal library akan berada: Google Drive, local storage, atau combination?

## Q-004 | OPEN
**Source:** UNKNOWN

Adakah setiap ahli keluarga perlu mempunyai agent/workspace sendiri?

## Q-005 | OPEN
**Source:** UNKNOWN

Apakah privacy boundary antara personal, family shared, children, school information dan Home Assistant?

## Q-006 | OPEN
**Source:** UNKNOWN

Bila WhatsApp patut masuk scope implementasi?

## Q-007 | OPEN
**Source:** UNKNOWN

Apakah maksud sebenar local-first bagi Temaya: data local, voice/memory local, atau semua inference local?

## Q-008 | OPEN
**Source:** UNKNOWN

Adakah Ryzen workstation sebahagian architecture Temaya atau optional extension?

## Q-009 | OPEN
**Source:** UNKNOWN

Adakah Puspa smart speaker prototype physical pertama?

## Q-010 | OPEN
**Source:** UNKNOWN

Adakah ball robots core Temaya atau peripheral/subproject kemudian?

## Q-011 | OPEN
**Source:** INFERRED

Nanti perlu tentukan:
- apa OpenClaw patut fikir;
- apa Home Assistant patut execute;
- apa automation biasa patut buat.

**Jangan selesaikan semasa idea-dump phase.**

## Q-012 | OPEN
**Source:** INFERRED

Nanti perlu tentukan sama ada tiga jenis data berikut memang perlu boundary berbeza:
1. Knowledge / Library
2. Personal / conversational memory
3. Operational household state

---

# RISKS

## R-001 | OPEN
**Source:** INFERRED

Migration/reorganization awal bagi personal library yang besar boleh menjadi terlalu berat.

## R-002 | OPEN
**Source:** INFERRED

Jika household automation bergantung terus pada OpenClaw/LLM, kegagalan AI boleh mengganggu fungsi rumah.

## R-003 | OPEN
**Source:** INFERRED

Credentials, voice embeddings, auth state atau private notes boleh terdedah jika disimpan bersama general searchable library.

## R-004 | OPEN
**Source:** INFERRED

Speaker identification sahaja mungkin tidak stabil sebagai sole identity mechanism.

## R-005 | OPEN
**Source:** INFERRED

Meta AI proposal mencampurkan terlalu banyak subsystem serentak dan boleh menyebabkan overbuild.

## R-006 | OPEN
**Source:** INFERRED

Apps Script sebagai mandatory middleware untuk semua library operation boleh mewujudkan maintenance layer yang tidak perlu.

## R-007 | OPEN
**Source:** INFERRED — perlu hardware validation

Ball-robot dimensions/components daripada Meta AI proposal mungkin mempunyai compatibility conflict.

## R-008 | OPEN
**Source:** INFERRED

Colour e-Paper dan fast partial-refresh animation mungkin mempunyai hardware trade-off.

## R-009 | OPEN
**Source:** INFERRED

Fungsi boleh overlap antara OpenClaw, HA LLM, Node-RED, Apps Script dan external agent framework.

## R-010 | OPEN
**Source:** INFERRED

Implementation-specific services yang disebut oleh external proposals jangan dianggap dependency Temaya secara automatik.

---

# CONFLICT / DISAGREEMENT LOG

## CF-001 | OPEN

Meta AI proposal menyifatkan sistem sebagai bukan cloud assistant tetapi turut mencadangkan komponen yang mungkin menggunakan cloud/external provider.

**Decision:** NONE.

## CF-002 | OPEN

Meta AI proposal meletakkan voice embedding dalam DL, sedangkan candidate lain memisahkan biometric/secrets ke local private vault.

**Decision:** NONE.

## CF-003 | OPEN

Meta AI proposal mencadangkan custom dual WhatsApp/Baileys containers, sedangkan candidate lain ialah cuba native OpenClaw routing dahulu.

**Decision:** NONE.

---

# DECISIONS

**Tiada `D-xxx | LOCKED`.**

Owner belum memberikan arahan LOCK / LOCK DECISION bagi mana-mana architecture choice.

---

# ARCHITECTURE

**Status:** PENDING CONFIRMATION

Belum ada architecture disahkan.

## Working map — NOT architecture

```text
TEMAYA
├── Family interaction
├── Knowledge / Library / Memory
└── Household operations
    ├── Home Assistant devices
    ├── Calendar
    ├── To-do / Grocery
    └── Reminders

Mini PC
├── Home Assistant
└── OpenClaw + required services
```

Map ini hanya membantu menyimpan kawasan idea. Ia bukan keputusan architecture.

---

# CURRENT DISCOVERY MODE

**EXPLICIT**

> "saya nak lambak idea dulu, lepastu baru bentuk kemungkinan padanan."

Maka tindakan semasa:
1. Tangkap idea.
2. Kekalkan source dan statusnya.
3. Jangan paksa padanan awal.
4. Jangan promote external proposal menjadi dependency.
5. Selepas owner nyatakan idea dump cukup, barulah bentuk beberapa kemungkinan padanan.

---

# VERSION HISTORY

| Version | Date | Change |
|---|---|---|
| 0.1.0 | 2026-09-30 | Initial source-of-truth commit. Captured OpenClaw + DL + mandatory mini-PC direction, agreed discovery candidates, Meta AI reference, Gemini HA/agent/WhatsApp ideas, open questions, conflicts and risks. No LOCKED decisions. |

---

# CURRENT CHECKPOINT

- OpenClaw direction captured.
- Mandatory mini-PC direction captured.
- DL adaptation captured.
- Large legacy personal library vs empty family libraries captured.
- Discovery-first workflow captured.
- Prior agreed candidates retained as AC, not LOCKED.
- Meta AI and Gemini material retained as external proposals, not accepted dependencies.
- Architecture remains PENDING CONFIRMATION.
