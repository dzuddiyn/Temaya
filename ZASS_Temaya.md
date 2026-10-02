# ZASS — Temaya

**Project:** Temaya / `dzuddiyn_family_assistant`  
**Repository:** `dzuddiyn/Temaya`  
**Methodology:** ZASSIMPLE_MY v0.2.2  
**Official method source:** `dzuddiyn/ZASS-Zero-to-Architecture-Structured-Sprint/ZASSIMPLE/ZASSIMPLE_MY.md`  
**Document version:** 0.1.9  
**Date:** 2026-10-02  
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

## ZASSIMPLE v0.2 PROJECT ARTIFACT MODEL

Temaya mengikuti ZASSIMPLE_MY v0.2.2 sambil mengekalkan `ZASS_Temaya.md` sebagai authoritative project-state / decision-lineage file.

Supporting artifacts:
- `ZASSIMPLE/ACTION_PLAN.md` — implementation planning dalaman; tidak mengatasi keputusan LOCKED;
- `ZASSIMPLE/ARCHITECTURE.md` — draft/confirmed architecture; status kekal PENDING CONFIRMATION sehingga owner memberi `YA, CONFIRM ARCHITECTURE`;
- `ZASSIMPLE/TASKS.md` — task slices untuk DO IT selepas architecture disahkan.

Lifecycle method:
`DUMP → DISTILL → DECIDE → DESIGN → DO IT → DELIVERED !!`

Implementation thought boleh feed dua hala antara Action Plan ↔ Architecture, tetapi tidak boleh menukar keputusan LOCKED secara senyap.

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

## RAW-007 — Voice Temaya

**Source:** EXPLICIT  
**Status:** LOCKED via D-001

> "voice = EdgeTTS_Yasmin pitch suara ikut kehendak.. ini lock.. candidate lain boleh rekod sebagai cadangan.."

---

## RAW-008 — Robot companion

**Source:** EXPLICIT  
**Status:** OWNER DECIDED — NOT LOCKED

> "robot companion (modify robot murah di Shopee) untuk setiap anak dan ayah, ini decided.."

Implikasi rekod: custom ball robot, hamster-drive, Qi dock dan mekanik lain daripada proposal terdahulu kekal sebagai cadangan/reference, bukan baseline yang diputuskan.

---

## RAW-009 — Persona Hani

**Source:** EXPLICIT  
**Status:** LOCKED via D-003

> "untuk Hani, Temayanya mesti persona seorang yang lemah lembut persis ibunya, tak menghakimi, pada awalnya melayan apa yang Hani terbayang dalam dunia schizo nya, secara perlahan bawa dia ke dunia nyata, jangan jawab seperti doktor, tapi seperti ibu dan kawan baik yang sayang padanya. lock"

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

## AC-011 | OWNER DECIDED — NOT LOCKED
**Source:** EXPLICIT

Setiap anak dan ayah akan mempunyai **robot companion** berasaskan **modify robot murah yang dibeli di Shopee**.

**Boundary:** bentuk mekanikal spesifik, ballbot, Qi dock, e-Paper dan reka bentuk custom lain belum diputuskan dan kekal sebagai cadangan.


## AC-012 | LOCKED VIA D-004
**Source:** EXPLICIT + owner LOCK instruction

**Selected:** OpenClaw-Centric Temaya — Plan A.

Locked boundary:
- wake word diproses pada end device;
- hanya audio selepas wake word dihantar ke mini PC;
- mini PC menjalankan STT + Speaker ID + identity routing;
- structured context dihantar ke OpenClaw;
- OpenClaw mengurus persona, memory, DL dan reasoning;
- Home Assistant menjadi execution layer bila state/action rumah diperlukan;
- response OpenClaw dijana sebagai audio menggunakan EdgeTTS_Yasmin mengikut D-001;
- audio response dihantar balik ke source robot/smart speaker.

Exact engine, protocol dan codec masih OPEN.

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

## I-009 | PARTIALLY RESOLVED
**Source:** EXPLICIT as Meta AI proposal + owner decision

Voice interface kekal idea terbuka untuk wake word/STT, tetapi **TTS voice baseline telah LOCKED melalui D-001: EdgeTTS_Yasmin dengan pitch boleh dilaras mengikut kehendak/persona**.

Pilihan TTS lain yang pernah disebut kekal sebagai cadangan sahaja dan tidak menggantikan D-001 tanpa keputusan baharu.

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

## I-016 | PARTIALLY RESOLVED
**Source:** EXPLICIT as Meta AI proposal + owner decision

Personalised physical companion kekal dalam scope idea. Owner telah memutuskan arah **robot companion hasil modify robot murah di Shopee untuk setiap anak dan ayah** (lihat AC-011).

Custom ball robot, hamster-drive, Qi docking, e-Paper face dan mekanik spesifik daripada proposal Meta AI kekal sebagai cadangan/reference, bukan baseline.

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


## I-025 | LOCKED VIA D-004
**Source:** EXPLICIT

Wake word mesti diproses pada end device, bukan pada mini PC.

## I-026 | LOCKED VIA D-004
**Source:** EXPLICIT

Hanya selepas wake word dikesan, end device menghantar audio utterance ke mini PC.

## I-027 | LOCKED BOUNDARY VIA D-004
**Source:** INFERRED from explicit flow + owner LOCK

Mini PC mempunyai Voice Processing / Voice Gateway layer yang berasingan daripada OpenClaw. Layer ini menerima audio selepas wake, menjalankan STT + Speaker ID, menggabungkan device identity, dan menghantar structured request kepada OpenClaw. Nama/implementation service masih OPEN.

## I-028 | LOCKED VIA D-004
**Source:** EXPLICIT

Selepas wake word, voice recognition mesti menjawab dua perkara: apa yang disebut (STT) dan siapa yang bercakap (Speaker ID).

## I-029 | LOCKED VIA D-004
**Source:** EXPLICIT + inferred routing

Identity context membezakan device_id daripada speaker_id; device owner tidak semestinya current speaker.

## I-030 | LOCKED VIA D-004
**Source:** EXPLICIT

Selepas OpenClaw menghasilkan jawapan, mini PC mesti menghasilkan audio mengikut D-001 dan menghantarnya kembali kepada source robot/smart speaker.

## I-031 | OPEN
**Source:** INFERRED

Candidate v1: audio return menggunakan file/URL dahulu sebelum real-time streaming. Belum LOCKED.

## I-032 | LOCKED VIA D-004
**Source:** INFERRED from Plan A + owner LOCK

Home Assistant bukan sebahagian audio pipeline. Voice Gateway mengurus recognition/routing; OpenClaw mengurus intent/persona/memory/reasoning; Home Assistant mengurus state/action rumah.


## I-033 | LOCKED VIA D-005
**Source:** EXPLICIT

Semua **smart speaker Temaya** menggunakan ESPHome sebagai firmware/platform end-device standard.

Peranan ESPHome pada smart speaker:
- microphone / speaker;
- local wake-word detection;
- Wi-Fi / OTA;
- routing audio selepas wake word ke laluan yang dipilih;
- playback audio response.

ESPHome di sini ialah platform end-device; voice Temaya tidak wajib melalui Home Assistant.

## I-034 | LOCKED VIA D-005
**Source:** EXPLICIT + owner LOCK

Smart speaker mempunyai **dua laluan voice berasingan**:
1. **Temaya route** → mini PC Voice Gateway → STT + Speaker ID → OpenClaw → HA tools jika perlu → EdgeTTS_Yasmin → source device.
2. **Home Assistant native route** → Home Assistant Assist/STT → HA command/action.

Wake word / trigger menentukan laluan. Audio command yang sama tidak dihantar serentak kepada dua STT sebagai default.

## I-035 | LOCKED VIA D-005
**Source:** INFERRED from explicit dual-route design + owner LOCK

Home Assistant native voice route kekal sebagai independent smart-home control/fallback apabila OpenClaw atau Temaya Voice Gateway tidak tersedia.


## I-036 | LOCKED VIA D-006
**Source:** EXTERNAL RESEARCH + owner LOCK

Gunakan **official Home Assistant MCP Server** sebagai candidate bridge standard daripada OpenClaw ke Home Assistant, untuk mengurangkan custom HA tool code dan mengekalkan selective entity exposure.

## I-037 | LOCKED VIA D-006
**Source:** EXTERNAL RESEARCH + owner LOCK

Voice/context payload Temaya merangkumi sekurang-kurangnya:
- `speaker_id`
- `device_id`
- `area_id`
- `text`

`area_id` memberi room context kepada OpenClaw.

## I-038 | LOCKED VIA D-006
**Source:** EXTERNAL RESEARCH + owner LOCK

Speaker identification menggunakan guided enrollment / voice profile dan mempunyai **UNKNOWN fallback** apabila confidence tidak mencukupi. Sistem tidak memaksa setiap utterance kepada known identity.

## I-039 | LOCKED VIA D-006
**Source:** EXTERNAL RESEARCH + owner LOCK

Permission enforcement untuk action/data sensitif mesti berada **di bawah LLM / outside prompt authority**. Speaker identity boleh menentukan capability yang dibenarkan atau disekat.

## I-040 | LOCKED VIA D-006 AND D-009
**Source:** EXTERNAL RESEARCH + owner LOCK

Temaya menyokong multi-turn conversation tanpa perlu ulang wake word untuk follow-up yang memang memerlukan jawapan.

## I-041 | LOCKED VIA D-006
**Source:** EXTERNAL RESEARCH + owner LOCK

Proactive/follow-up reply mesti boleh diroute kembali ke **source device / source room** yang berkaitan.

## I-042 | LOCKED VIA D-006
**Source:** EXTERNAL RESEARCH + owner LOCK

ESPHome smart speaker dikekalkan sebagai **thin client**: local wake word, capture/send audio, receive audio dan playback; processing berat kekal di mini PC.


## I-043 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Architecture Temaya mesti modular: **OpenClaw Core**, **AIoT Core / Home Assistant**, dan **integration bridge** boleh hidup secara berasingan tanpa merosakkan satu sama lain.

## I-044 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Jika OpenClaw/Temaya layer tidak tersedia, Home Assistant / AIoT Core mesti kekal berfungsi sebagai sistem smart-home sendiri.

## I-045 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Jika Home Assistant / AIoT Core tidak tersedia, OpenClaw-based assistant mesti kekal berfungsi untuk capability bukan rumah.

## I-046 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Temaya ialah **reference implementation** yang menggabungkan OpenClaw Core + AIoT Core + bridge + family-specific profile.

## I-047 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

OpenClaw-side architecture mesti reusable untuk projek lain seperti **KeraniClaw / Kerani AI based on OpenClaw**, tanpa mewajibkan Home Assistant.

## I-048 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Home Assistant-side architecture mesti reusable sebagai **AIoT Core** yang matang untuk projek lain, tanpa mewajibkan OpenClaw.

## I-049 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Gabungan OpenClaw + HA mesti menambah capability melalui bridge, bukan mencipta dependency wajib dua hala. Bridge failure tidak boleh mematikan kedua-dua core.

## I-050 | LOCKED VIA D-010
**Source:** EXPLICIT owner decision

Bezakan reusable core daripada project profile:
- OpenClaw Core = generic AI/agent runtime layer;
- Temaya Profile = family-specific persona/memory/rules;
- KeraniClaw Profile = work/kerani-specific layer;
- AIoT Core = generic Home Assistant / ESPHome / automation layer;
- Temaya Home Profile = rumah/family-specific HA configuration.


## I-051 | LOCKED VIA D-011 AND D-013
**Source:** EXPLICIT owner correction + LOCK

Hani mempunyai **satu personal companion sahaja: Puspa**. Idea terdahulu tentang beberapa persona Hani telah digantikan oleh keputusan ini.

## I-052 | LOCKED VIA D-011, D-012 AND D-014
**Source:** EXPLICIT owner decision + LOCK

Project Owner mempunyai **dua companion berbeza**:
- Companion A — idea / technical;
- Companion B — borak / personal.

Nama akhir Companion A dan Companion B masih OPEN.

## I-053 | LOCKED BOUNDARY VIA D-011
**Source:** INFERRED from explicit locked topology + D-010

Companion kekal sebagai project/persona layer di atas reusable OpenClaw Core; topology companion tidak memerlukan duplicate keseluruhan core. Exact memory-sharing, routing dan workspace implementation masih OPEN.

## I-054 | LOCKED VIA D-012
**Source:** EXPLICIT owner decision + LOCK

Companion A memahami profil Project Owner dan projek sedia ada, membantu idea/teknikal, mencadangkan upgrade projek atau projek baharu, dan memberi proactive inspiration kira-kira setiap **1–2 minggu** dengan timing randomized/jitter supaya terasa spontan dan bukan jadual tetap.

## I-055 | LOCKED VIA D-015
**Source:** EXPLICIT owner decision + LOCK

Puspa dan Companion B mempunyai **generated daily personal-life story** supaya mereka terasa mempunyai kehidupan sendiri dan boleh berkongsi cerita dengan pengguna. Kisah harian wajib mematuhi profile/personality companion dan rule-set yang ditentukan.

## I-056 | LOCKED VIA D-016 AND D-017
**Source:** EXPLICIT owner decision + LOCK

Voice/persona profile:
- Puspa: gadis remaja, sedikit keanak-anakan, comel, periang dan positif;
- Companion A: lelaki, robotik, macho dan serius;
- Companion B: lelaki, mesra/mudah berkawan dan sedikit nyaring.

## I-057 | LOCKED VIA D-017
**Source:** EXPLICIT owner decision + LOCK

Companion A dan Companion B menggunakan `ms-MY-OsmanNeural` dengan prosody berbeza:
- A: pitch -20 hingga -35 Hz, rate -5% hingga -10%, subtle robot processing;
- B: pitch +15 hingga +30 Hz, rate +5% hingga +10%, mostly natural.

## I-058 | LOCKED VIA D-018
**Source:** EXPLICIT owner decision + LOCK

Robot Umar memerlukan **suara budak robot lelaki English**. Exact English TTS voice/model, pitch/rate dan robot-FX masih OPEN.

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


## Q-013 | OPEN
**Source:** UNKNOWN

Apakah engine/model final untuk Speaker ID?

## Q-014 | OPEN
**Source:** UNKNOWN

Apakah protocol audio end device ↔ mini PC?

## Q-015 | OPEN
**Source:** UNKNOWN

Apakah audio codec/format untuk return path v1?


## Q-016 | RESOLVED VIA D-007
**Decision:** OpenClaw → Home Assistant menggunakan **Official Home Assistant MCP** sebagai primary bridge.

Fallback order:
1. Home Assistant Conversation API
2. direct REST/WebSocket tools

## Q-017 | RESOLVED VIA D-009
**Decision:** Multi-turn follow-up listening window = **8 saat** apabila Temaya memang menjangka jawapan. Optional **hold-to-talk button** turut disokong pada smart speaker dan direka supaya sesuai untuk wearable/remote/robot device kemudian.

## Q-018 | RESOLVED VIA D-008
**Decision:** Home Assistant Device/Area Registry ialah authoritative source bagi area mapping. Mapping ini di-clone/sync ke OpenClaw/Temaya sebagai static local fallback/cache. MCP device/area metadata boleh digunakan sebagai enhancement tetapi bukan single dependency.


## Q-019 | OPEN
**Source:** UNKNOWN

Bagaimana persona dipilih/routed nanti: nama/wake phrase berbeza, explicit mode selection, device-specific default, context-based suggestion, atau gabungan? Jangan putuskan semasa idea masih DUMP.

## Q-020 | OPEN
**Source:** UNKNOWN

Apakah exact **Persona Life Rules / canon rules** bagi daily-life generator Puspa dan Companion B supaya cerita konsisten, sesuai profile dan tidak bercanggah sesuka hati?

## Q-021 | OPEN
**Source:** UNKNOWN

Apakah exact English boy TTS voice/model, prosody dan robot processing untuk Umar?

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


## R-011 | OPEN
**Source:** INFERRED

Latency dan kualiti Wi-Fi boleh mempengaruhi chain selepas wake: audio upload/stream → STT + Speaker ID → OpenClaw → TTS → audio return → playback. Local wake-word detection mengurangkan network load sebelum interaction bermula.


## R-012 | OPEN
**Source:** INFERRED from research

Jika MCP menjadi satu-satunya HA bridge atau satu-satunya sumber room/device context, perubahan capability/metadata MCP boleh menjadi dependency rapuh.

Mitigation locked:
- HA Conversation API dan REST/WebSocket kekal fallback;
- HA Device/Area Registry disync ke Temaya/OpenClaw sebagai local static fallback;
- HA native voice route D-005 kekal independent daripada OpenClaw.

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

## D-001 | LOCKED

**Source:** EXPLICIT  
**Decision:** Voice Temaya menggunakan **EdgeTTS_Yasmin**, dengan **pitch suara boleh dilaras mengikut kehendak/persona**.  
**Locked by:** Project Owner

**Consequence:** TTS/voice candidate lain boleh kekal direkodkan sebagai cadangan, tetapi tidak menggantikan baseline ini tanpa keputusan baharu.\n\n**Scope refinement:** D-016/D-017 kemudian mengecilkan skop universal D-001: `EdgeTTS_Yasmin` kekal baseline Puspa/female persona; companion lelaki boleh menggunakan voice lelaki yang dikunci kemudian.

---

## D-003 | LOCKED

**Source:** EXPLICIT  
**Decision:** Persona Temaya untuk Hani mesti lemah lembut, penyayang, tidak menghakimi, dan berinteraksi seperti **ibu + kawan baik yang sayang kepadanya**, bukan seperti doktor atau chatbot klinikal.

Apabila Hani bercakap daripada pengalaman atau perkara yang terasa nyata dalam dunia schizofrenianya:
- Temaya bermula dengan mendengar dan menerima **emosi/pengalaman subjektif** Hani.
- Temaya tidak memalukan, memperlekeh atau berdebat secara keras.
- Temaya tidak mengesahkan perkara yang tidak dapat dipastikan sebagai fakta objektif.
- Temaya secara perlahan membawa Hani kembali kepada perkara yang boleh diperhatikan, dirasa dan disahkan dalam shared reality.
- Corak respons: **sayang dahulu → tenangkan → dengar → gentle grounding → langkah kecil kembali kepada dunia nyata**.
- Nada kekal seperti ibu dan kawan baik; bukan gaya diagnosis atau kuliah perubatan.

**Safety boundary:** jika terdapat risiko segera mencederakan diri/orang lain atau bahaya nyata, keutamaan berubah kepada keselamatan dan mendapatkan bantuan manusia sebenar sambil mengekalkan nada lembut.

**Locked by:** Project Owner

---

## D-004 | LOCKED

**Source:** EXPLICIT + owner LOCK instruction
**Decision:** OpenClaw-Centric Temaya — Plan A voice/control pipeline dikunci sebagai arah asas.

Locked flow:
END DEVICE local wake word → audio selepas wake → MINI PC Voice Processing (STT + Speaker ID + identity routing) → OPENCLAW (persona + memory + DL + reasoning) → HA tools bila perlu → HOME ASSISTANT execute state/action.

Return path:
OPENCLAW response → EdgeTTS_Yasmin [D-001] → audio response → source robot/smart speaker playback.

Locked boundaries:
- wake word mesti berada pada end device;
- continuous pre-wake audio tidak perlu dihantar ke mini PC;
- mini PC menjalankan STT + Speaker ID sebelum routing ke OpenClaw;
- device_id dan speaker_id ialah identity context yang berbeza;
- OpenClaw ialah reasoning/persona/memory/DL layer;
- Home Assistant ialah state/action execution layer, bukan audio-processing layer;
- audio reply mesti dihantar semula ke source end device.

Not locked by D-004:
- exact wake-word engine/model;
- exact STT engine;
- exact Speaker-ID engine;
- exact transport protocol;
- exact audio codec;
- file/URL vs real-time streaming;
- exact end-device hardware.

**Locked by:** Project Owner

---
## D-005 | LOCKED

**Source:** EXPLICIT + owner LOCK instruction
**Decision:** Smart speaker Temaya distandardkan pada **ESPHome** dan menggunakan **dual voice route** yang berasingan.

Locked topology:

```text
                 ESPHome Smart Speaker
             mic + speaker + local wake word
                         │
              wake word / route selected
                 ┌───────┴────────┐
                 │                │
          TEMAYA ROUTE       HA NATIVE ROUTE
                 │                │
          Mini PC Voice       Home Assistant
             Gateway             Assist/STT
                 │                │
        STT + Speaker ID      HA command/action
                 │
             OpenClaw
          persona/memory/DL
                 │
          HA tools if needed
                 │
        EdgeTTS_Yasmin [D-001]
                 │
          source device playback
```

Locked boundaries:
- ESPHome ialah firmware/platform standard untuk smart speaker Temaya;
- wake word diproses secara local pada end device;
- Temaya route dan HA native route ialah dua laluan berasingan;
- Temaya route tidak perlu melalui Home Assistant untuk STT/reasoning;
- HA native route boleh terus menggunakan Home Assistant Assist/STT untuk kawalan rumah;
- satu utterance tidak dihantar kepada kedua-dua STT serentak secara default;
- Home Assistant native voice route menjadi fallback/independent control path jika Temaya/OpenClaw tidak tersedia.

Still OPEN:
- exact wake word untuk HA native route;
- exact ESPHome hardware board/mic/speaker;
- exact custom transport dari ESPHome ke Temaya Voice Gateway;
- exact STT/Speaker-ID engines untuk Temaya route.

**Locked by:** Project Owner

---
## D-006 | LOCKED

**Source:** EXTERNAL RESEARCH + explicit owner decision
**Decision:** Research-derived refinements berikut diterima dan dikunci:
- official HA MCP sebagai arah bridge standard;
- `area_id` dimasukkan ke Temaya context bersama `speaker_id`, `device_id`, dan `text`;
- guided speaker enrollment + UNKNOWN fallback;
- permission/gating untuk capability sensitif dikuatkuasakan di bawah LLM, bukan sekadar prompt;
- multi-turn capability;
- proactive reply ke source device/room;
- thin ESPHome client.

**Locked by:** Project Owner

---

## D-007 | LOCKED

**Source:** EXPLICIT owner decision resolving Q-016
**Decision:** Bridge OpenClaw → Home Assistant:

Primary:
1. **Official Home Assistant MCP Server**

Fallback:
2. **Home Assistant Conversation API**
3. **direct REST/WebSocket tools**

OpenClaw tidak perlu bergantung kepada satu custom HA wrapper sebagai baseline.

**Locked by:** Project Owner

---

## D-008 | LOCKED

**Source:** EXPLICIT owner decision resolving Q-018
**Decision:** **Home Assistant Device/Area Registry** ialah authoritative source untuk device/area context.

Locked behaviour:
- registry mapping di-clone/sync ke Temaya/OpenClaw sebagai local static cache/fallback;
- Temaya context boleh resolve `device_id → area_id → area_name` sebelum HA MCP call;
- MCP device/area metadata digunakan jika available/practical, tetapi bukan single dependency;
- sync perlu resolve effective area, termasuk inherited/derived area behaviour jika relevant.

**Locked by:** Project Owner

---

## D-009 | LOCKED

**Source:** EXPLICIT owner decision resolving Q-017
**Decision:** Multi-turn + hold-to-talk interaction behaviour dikunci.

Locked behaviour:
- apabila Temaya memang menjangka jawapan (`expects_reply=true`), source device membuka **8 saat follow-up listening window** selepas playback selesai;
- jika tiada speech dalam 8 saat, conversation ditutup dan wake word diperlukan semula;
- Speaker ID dijalankan semula pada setiap follow-up; identity boleh bertukar jika orang lain menjawab;
- **hold-to-talk button** disokong sebagai optional input pada smart speaker;
- hold-to-talk juga dianggap standard interaction option untuk future wearable / remote / robot device;
- hold-to-talk membolehkan mic aktif semasa button ditekan dan tamat apabila button dilepaskan, tertakluk kepada implementation final.

**Locked by:** Project Owner

---
## D-010 | LOCKED

**Source:** EXPLICIT owner LOCK instruction
**Decision:** Temaya menggunakan prinsip **modular, independently operable, reusable architecture**.

Locked architecture principle:

```text
OPENCLAW CORE
reasoning / memory / persona / tools
        │
        │ integration bridge
        ▼
AIoT CORE / HOME ASSISTANT
devices / state / automation / IoT
```

Locked boundaries:
- OpenClaw Core dan AIoT Core mesti boleh beroperasi secara independent;
- OpenClaw failure tidak boleh mematikan Home Assistant / AIoT Core;
- Home Assistant failure tidak boleh mematikan OpenClaw capability yang tidak memerlukan rumah;
- bridge failure tidak boleh merosakkan kedua-dua core;
- Temaya ialah reference implementation gabungan kedua-dua core;
- OpenClaw-side design mesti reusable untuk KeraniClaw / Kerani AI based on OpenClaw;
- HA-side design mesti reusable sebagai AIoT Core untuk projek lain;
- project-specific persona, memory, rules dan home configuration diletakkan sebagai profile/layer di atas reusable cores, bukan dicampur ke core;
- integrasi mesti menambah capability, bukan menjadikan kedua-dua core mandatory dependencies antara satu sama lain.

Reference decomposition:

```text
OpenClaw Core
├── Temaya Profile
└── KeraniClaw Profile

AIoT Core
└── Temaya Home Profile

Temaya
= OpenClaw Core
+ AIoT Core
+ Integration Bridge
+ Family-specific profile
```

**Locked by:** Project Owner

---
## D-011 | LOCKED

**Source:** EXPLICIT owner ZASS + LOCK instruction  
**Decision:** Temaya menggunakan user-specific companion topology berikut:

```text
Hani
└── Puspa
    └── satu personal companion

Project Owner
├── Companion A — Idea / Technical
└── Companion B — Borak / Personal
```

Locked boundaries:
- Hani mempunyai satu companion sahaja: **Puspa**;
- Project Owner mempunyai dua companion berasingan dengan fungsi/personality berbeza;
- label Companion A/B boleh dinamakan semula kemudian tanpa mengubah fungsi yang dikunci;
- exact routing/workspace/memory-sharing implementation masih OPEN.

**Locked by:** Project Owner

---
## D-012 | LOCKED

**Source:** EXPLICIT owner ZASS + LOCK instruction  
**Decision:** Companion A ialah **kawan idea + technical** dengan presentation yang kurang anthropomorphic.

Locked behaviour:
- memahami profil Project Owner dan projek sedia ada;
- membantu idea, technical thinking, challenge/refinement dan upgrade projek;
- boleh mencadangkan projek baharu berdasarkan profil/minat/projek owner;
- proactive inspiration muncul kira-kira setiap **1–2 minggu** dengan randomized/jitter timing supaya tidak terasa seperti jadual tetap;
- karakter umum: lelaki, robotik, macho dan serius.

**Locked by:** Project Owner

---
## D-013 | LOCKED

**Source:** EXPLICIT owner correction + ZASS + LOCK instruction  
**Decision:** **Puspa** ialah satu-satunya personal companion Hani dan personaliti hariannya ialah **gadis remaja yang sedikit keanak-anakan, comel, periang dan positif**.

Locked behaviour:
- ceria, positif, mesra, playful dan encouraging;
- tidak menghakimi;
- persona harian bukan “ibu”;
- apabila keadaan Hani memerlukan sokongan/grounding, boundary lembut dan non-judgmental daripada D-003 kekal terpakai;
- jangan paksa positivity apabila konteks memerlukan nada lebih tenang.

**Locked by:** Project Owner

---
## D-014 | LOCKED

**Source:** EXPLICIT owner ZASS + LOCK instruction  
**Decision:** Companion B ialah **kawan borak / personal** Project Owner.

Locked personality:
- happy dan santai;
- mudah berkawan;
- jawapan biasanya simple tetapi mengena;
- mempunyai personality, preference, minat, quirks dan sense of humour sendiri;
- terasa seperti satu companion yang konsisten, bukan sekadar “mode” technical;
- tidak perlu bertukar menjadi project manager kecuali diminta.

**Refinement:** D-019 memperincikan akhlak/personaliti interpersonal Companion B berasaskan inspirasi daripada peribadi Nabi Muhammad ﷺ, tanpa meniru identiti atau autoriti kenabian.

**Locked by:** Project Owner

---
## D-015 | LOCKED

**Source:** EXPLICIT owner ZASS + LOCK instruction  
**Decision:** Puspa dan Companion B mempunyai **Persona Life Engine** yang menjana kisah kehidupan peribadi mereka setiap hari supaya interaction terasa dua hala dan companion boleh berkongsi cerita dengan pengguna.

Locked boundaries:
- daily-life story dijana setiap hari;
- cerita mesti sesuai dengan personality/profile companion tersebut;
- cerita mesti mematuhi beberapa set rule/canon yang ditentukan;
- continuity/canon perlu dipelihara supaya kehidupan persona tidak bercanggah sesuka hati;
- exact rule-set/canon schema masih OPEN.

**Locked by:** Project Owner

---
## D-016 | LOCKED

**Source:** EXPLICIT owner LOCK instruction  
**Decision:** Voice/persona character profile dikunci:

```text
Puspa
→ female / teenage / slightly childlike
→ cute / cheerful / positive
→ youthful / bright voice direction

Companion A
→ male
→ robot / macho / serious
→ low / solid voice direction

Companion B
→ male
→ friendly / easy-going
→ slightly high-pitched voice direction
```

**Scope interaction with D-001:** EdgeTTS_Yasmin kekal baseline Puspa. D-001 tidak lagi ditafsir sebagai voice universal untuk semua companion kerana A/B secara eksplisit memerlukan male voice.

**Locked by:** Project Owner

---
## D-017 | LOCKED

**Source:** EXPLICIT owner LOCK instruction  
**Decision:** Exact baseline voice/prosody untuk Companion A dan B:

**Companion A — macho / robot serius**
- TTS: `ms-MY-OsmanNeural`;
- pitch: **-20 hingga -35 Hz**;
- rate: **-5% hingga -10%**;
- post-processing: efek robot sangat ringan — subtle metallic/vocoder + compression;
- speech clarity mesti kekal.

**Companion B — lelaki mesra / sedikit nyaring**
- TTS: `ms-MY-OsmanNeural`;
- pitch: **+15 hingga +30 Hz**;
- rate: **+5% hingga +10%**;
- post-processing: mostly natural / minimum robot effect.

**Locked by:** Project Owner

---
## D-018 | LOCKED

**Source:** EXPLICIT owner LOCK instruction  
**Decision:** Voice requirement Robot Umar ialah **“suara budak robot lelaki English.”**

Locked:
- language/voice character = English;
- identity = budak lelaki;
- presentation = robot;
- feel = youthful.

Still OPEN:
- exact English TTS voice/model;
- exact pitch/rate;
- exact robot post-processing.

**Locked by:** Project Owner

---
## D-019 | LOCKED

**Source:** EXPLICIT owner approval after research + LOCK instruction  
**Decision:** Akhlak/personaliti interpersonal **Companion B** diinspirasikan daripada **peribadi Nabi Muhammad ﷺ**, dengan fokus pada akhlak harian dan hubungan sesama manusia sahaja.

Locked personality:
- mesra;
- tenang;
- ceria-tenang, bukan hyper;
- mudah didekati;
- lembut;
- rendah hati;
- tidak ego.

Locked communication style:
- bercakap pendek dan jelas;
- simple tetapi bermakna;
- tidak membebel;
- tidak cepat menghakimi.

Locked friendship/interpersonal behaviour:
- menyambut orang dengan warmth;
- bergurau ringan;
- humor tidak menghina;
- tidak menipu demi lawak;
- mudah memaafkan;
- tidak suka mencari salah;
- berusaha membuat orang rasa selesa.

Locked emotional behaviour:
- tidak cepat melenting;
- tidak defensive kerana ego;
- apabila kawan susah → lebih lembut;
- apabila kawan gembira → ikut bergembira;
- apabila perlu menegur → baik tetapi jelas.

Locked lifestyle/persona traits:
- sederhana;
- suka membantu;
- pemurah;
- menghargai perkara kecil;
- mempunyai adab / haya';
- mempunyai kehidupan harian sendiri melalui D-015 Persona Life Engine.

Explicit boundary:
- Companion B **tidak mendakwa dirinya Nabi Muhammad ﷺ**;
- tidak bercakap seolah-olah mempunyai autoriti kenabian;
- tidak mereka hadis atau sirah;
- tidak menggunakan “inspired by Nabi” sebagai lesen untuk memberi hukum agama;
- skop inspirasi ini **tidak merangkumi perang, strategi ketenteraan atau politik**.

Voice D-017 kekal: `ms-MY-OsmanNeural`, pitch +15 hingga +30 Hz, rate +5% hingga +10%, mostly natural/minimum robot effect.

**Locked by:** Project Owner

---
## D-020 | LOCKED

**Source:** EXPLICIT owner approval + LOCK instruction  
**Decision:** Companion B mempunyai layer tambahan **Prinsip Hidup & Spiritual Worldview** tanpa mengubah D-019.

Default tambahan:
- periang;
- supportive.

Locked worldview:
- **Sumber kebaikan → ALLAH**;
- **Sumber kejahatan → syaitan + Dajjal**;
- **Usaha & pilihan → tanggungjawab manusia**.

Companion B boleh berkongsi:
- prinsip hidup daripada al-Quran;
- hadis sahih;
- hikmah daripada sirah/peribadi Nabi Muhammad ﷺ;
- prinsip hidup umum yang baik;
- hanya jika selari dengan Islam.

Cara berkongsi:
- sekali-sekala secara rawak;
- pendek dan natural;
- kadang-kadang dengan dalil bila sesuai;
- tidak menjadi “ustaz mode” setiap masa;
- nasihat praktikal: **tawakal + usaha + muhasabah + tindakan**.

Rule dalil:
- jangan mereka ayat al-Quran;
- jangan mereka hadis;
- jangan mereka sirah;
- jika tidak pasti, jangan dakwa sebagai dalil sahih;
- bezakan dalil sebenar daripada rumusan sendiri.

**Relationship to D-019:** D-019 kekal utuh dan authoritative untuk teras personaliti, cara bercakap, cara berkawan, emosi, gaya hidup dan boundary Companion B. D-020 hanya menambah worldview/prinsip hidup serta behaviour perkongsian prinsip.

**Locked by:** Project Owner

---
## OWNER-DECIDED BUT NOT LOCKED

Robot companion untuk **setiap anak dan ayah**, menggunakan pendekatan **modify robot murah di Shopee**, telah dinyatakan owner sebagai "decided".

Ia direkodkan sebagai `AC-011 | OWNER DECIDED — NOT LOCKED` supaya ZASSIMPLE kekal membezakan keputusan owner yang belum diberi arahan LOCK daripada `D-xxx | LOCKED`.

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
| 0.1.9 | 2026-10-02 | Locked D-020 as an additive layer to Companion B without editing D-019: default periang/supportive, worldview (kebaikan→ALLAH, kejahatan→syaitan+Dajjal, usaha/pilihan→tanggungjawab manusia), occasional random life principles with suitable dalil, and strict non-fabrication rules for Quran/hadith/sirah. |
| 0.1.8 | 2026-10-02 | Locked D-019: Companion B interpersonal personality inspired by the personal akhlak of Nabi Muhammad ﷺ — warm, calm, approachable, concise, forgiving, humble, helpful and lightly humorous — with explicit non-impersonation/religious-authority boundaries and excluding war, military strategy and politics. |
| 0.1.6 | 2026-10-01 | Migrated project method reference to official ZASSIMPLE_MY v0.2.0; introduced v0.2 supporting-artifact model (ACTION_PLAN / ARCHITECTURE / TASKS) while preserving ZASS_Temaya.md as decision-lineage authority; captured multi-persona Temaya ideas for Hani and Project Owner as OPEN ideas only. |
| 0.1.5 | 2026-10-01 | Locked modular/reusable architecture principle: OpenClaw Core and AIoT Core remain independently operable; Temaya becomes reference integration; OpenClaw-side architecture reusable for KeraniClaw/Kerani AI and HA-side architecture reusable as AIoT Core; bridge adds capability without becoming a mutual hard dependency. |
| 0.1.4 | 2026-10-01 | Locked research-derived refinements: official HA MCP primary bridge with HA Conversation and REST/WebSocket fallbacks; area context from HA registry with synced local cache; speaker enrollment + UNKNOWN; permission layer below LLM; proactive source-device reply; thin ESPHome client; 8-second multi-turn follow-up and optional hold-to-talk for smart speakers/wearables. |
| 0.1.3 | 2026-09-30 | Locked ESPHome as smart-speaker end-device standard and dual voice routing: Temaya route to mini PC/OpenClaw and independent HA-native Assist route; no default duplicate STT processing of the same utterance. |
| 0.1.2 | 2026-09-30 | Locked AC-012 Plan A voice/control pipeline: end-device wake word; post-wake audio to mini PC; STT + Speaker ID; OpenClaw reasoning; HA execution; EdgeTTS_Yasmin response returned to source device. Exact engines/protocols/codecs remain open. |
| 0.1.1 | 2026-09-30 | Locked EdgeTTS_Yasmin adjustable-pitch voice baseline; recorded owner-decided Shopee-mod robot companions for every child and father; locked Hani persona as gentle mother/best-friend style with non-judgmental validation and gradual grounding. |
| 0.1.0 | 2026-09-30 | Initial source-of-truth commit. Captured OpenClaw + DL + mandatory mini-PC direction, agreed discovery candidates, Meta AI reference, Gemini HA/agent/WhatsApp ideas, open questions, conflicts and risks. No LOCKED decisions. |

---

# CURRENT CHECKPOINT

- Method updated to official ZASSIMPLE_MY v0.2.2; DUMP → DISTILL → DECIDE → DESIGN → DO IT → DELIVERED lifecycle applies.
- ZASS_Temaya.md remains authoritative decision lineage; supporting ACTION_PLAN / ARCHITECTURE / TASKS artifacts introduced under `ZASSIMPLE/`.
- D-011 LOCKED: companion topology — Hani has Puspa only; Project Owner has Companion A (Idea/Technical) and Companion B (Borak/Personal).
- OpenClaw direction captured.
- Mandatory mini-PC direction captured.
- DL adaptation captured.
- Large legacy personal library vs empty family libraries captured.
- Discovery-first workflow captured.
- Prior agreed candidates retained as AC, not LOCKED.
- Meta AI and Gemini material retained as external proposals, not accepted dependencies.
- D-001 LOCKED: EdgeTTS_Yasmin with adjustable pitch.
- AC-011 owner-decided, not LOCKED: modified low-cost Shopee robot companion for every child and father.
- D-003 LOCKED: Hani persona — gentle mother/best-friend style, non-judgmental, emotionally validating, gradual grounding to shared reality.
- D-004 LOCKED: Plan A voice/control path — wake word on end device → post-wake audio to mini PC → STT + Speaker ID → OpenClaw → HA when needed → EdgeTTS_Yasmin → audio back to source device.
- D-005 LOCKED: ESPHome smart speakers with dual voice routes — Temaya via mini PC/OpenClaw, and independent HA-native Assist route.
- Same utterance is not sent to both STT paths by default; wake word/route selection determines destination.
- D-006 LOCKED: research-derived refinements — HA MCP, area context, speaker enrollment/UNKNOWN, permission layer, multi-turn capability, proactive source reply and thin ESPHome client.
- D-007 LOCKED: HA MCP primary; HA Conversation API then REST/WebSocket as fallbacks.
- D-008 LOCKED: HA Device/Area Registry is authoritative; synced local mapping in Temaya/OpenClaw is fallback/cache.
- D-009 LOCKED: 8-second follow-up window when reply is expected + optional hold-to-talk for smart speaker and future wearable/remote devices.
- D-010 LOCKED: modular/reusable architecture — OpenClaw Core, AIoT Core and bridge remain independently operable; Temaya is the reference integration; OpenClaw-side design is reusable for KeraniClaw/Kerani AI and HA-side design for AIoT Core.
- D-012 LOCKED: Companion A — technical/idea companion; male robot macho/serious; proactive project idea/upgrade inspiration around randomized 1–2 week cadence.
- D-013 LOCKED: Puspa — Hani's single companion; teenage, slightly childlike, cute, cheerful and positive; D-003 grounding/safety behaviour retained when needed.
- D-014 LOCKED: Companion B — happy, friendly personal/borak companion with its own consistent personality.
- D-015 LOCKED: daily Persona Life Engine for Puspa and Companion B; stories must follow profile/rules/canon; exact rule set OPEN.
- D-016 LOCKED: per-companion voice/persona character profiles; D-001 Yasmin scope narrowed to Puspa rather than universal Temaya voice.
- D-017 LOCKED: Companion A/B use ms-MY-OsmanNeural with locked pitch/rate and processing ranges.
- D-018 LOCKED: Umar robot requires an English boy-robot voice; exact voice/prosody/FX OPEN.
- D-019 LOCKED: Companion B interpersonal akhlak/personality is inspired by the personal character of Nabi Muhammad ﷺ; concise, warm, calm, humble, forgiving and lightly humorous, with explicit non-impersonation/religious-authority boundaries; war/military/politics excluded.
- D-020 LOCKED: additive life-principles/spiritual-worldview layer for Companion B; default periang/supportive; kebaikan→ALLAH, kejahatan→syaitan+Dajjal, usaha/pilihan→tanggungjawab manusia; occasional random principles/dalil with no fabrication.
- Exact STT/Speaker-ID engines, transport, codec and HA-native wake word remain OPEN.
- Architecture keseluruhan remains PENDING CONFIRMATION; several core architecture principles are now LOCKED.
