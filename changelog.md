## ReelRig AI [v0.1.1] - 2026-11-23 minor update

### 🎬 Three.js 3D Diorama Engine Overhaul
- **Cinematic Rendering & Lighting:** Upgraded WebGL pipeline with `ACESFilmicToneMapping`, `PCFSoftShadowMap`, procedural PBR surface textures (walls, scuffed floors, brushed metal), procedural IBL reflections, volumetric light cones, `FogExp2`, and export-safe post-processing (`UnrealBloomPass`, subtle vignette & grain).
- **Expanded Multi-Zone 3D Map:** Upgraded from a single hallway to a 5-zone interconnected interior (`basement_corridor`, `locker_bay`, `security_office`, `elevator_lobby`, `stairwell_landing`) optimized with `THREE.InstancedMesh` for 60 FPS preview and export.
- **Reactive Environmental Cues:** Added deterministic, timeline-synced world events (hinged/sliding doors, locked-door rattles, light flickers, emergency red power drops, live countdown timers, and dynamic flashlight beam tracking).
- **Diverse Characters & Expressive Animation:** Replaced uniform character models with distinct procedural archetypes/outfits and a blended animation state machine (`idle_tense`, `walk_cautious`, `run_panic`, `look_around`, `startled_recoil`, `reach_interact`, `check_item`, `crouch_hide`) with clamped head/flashlight `lookAt` tracking.

### 🖋️ 16:9 Survival Chronicle (2D Ink) Upgrade
- **Visual Consistency & Reference Lock:** Added Episode Visual Bible, Character Reference sheets (with optional custom stickman PNG upload), Location Master Anchors (`locationId`) to prevent mutating rooms/furniture, strict anatomy guardrails, and one-click per-shot glitch regeneration.
- **Dynamic 16:9 Pacing & Framing:** Enforced varied shot compositions (`wide_scene`, `tight_closeup`, `top_down_diagram`, `split_panel`, `impact_text_card`), snappy deterministic pop-cuts, subtle paper grain, and optional living-ink / callout controls.
- **Snappy 1–2s Insert Shots:** Added matching 2D Ink cutaways (`inventory_checklist` synced with Continuity Snapshot, `resource_gauge`, `danger_clock`, `beat_stamp`) to break monotony in longer 2–10m episodes.
- **Sharper Retention Script Engine:** Rewrote 16:9 storytelling prompts to eliminate generic AI clichés, enforce "BUT / THEREFORE" escalation loops, plant open loops, and prioritize concrete survival details.

### 🎙️ Audio, Voiceover & Creator Workflow
- **Custom Voiceover per Shot:** Added direct microphone recording and `.mp3`/`.wav`/`.m4a` upload per shot, automatic shot-duration fitting with silence trimming, and automatic skipping during batch AI TTS generation.
- **Hybrid Music, AI Auto-Score & SFX:** Added background audio controls supporting custom track uploads (including Act 2 tension crossfades) as well as AI-directed procedural dark-ambient scores and synced foley SFX with automatic voiceover ducking — fully muxed into `Export Video`.
- **Ending A/B Choice Toggle:** Added an On/Off switch (`includeEndingChoice`) to generate linear stories or standalone cliffhangers without forced viewer A/B choice cards, while keeping linear episode continuation intact.
- **Pre-Flight API Cost Estimator:** Added transparent approximate BYOK cost estimates before triggering generation (explicitly reflecting `$0.00` visual cost in real-time Three.js 3D mode).

### 🛡️ Compliance, Legal & Stability
- **Legal & OAuth Readiness:** Audited and updated bilingual (PL/EN) Privacy Policy, Terms of Service (Beta "As-Is", BYOK disclaimer, user content responsibility), Google API Limited Use & YouTube API disclosures, honest cookie/storage notices, and EU AI Act transparency notes — accessible before login without losing Studio state.


## ReelRig AI v0.1.0 - BETA 2026-11-22 First beta realease

First public release of **ReelRig AI** — a browser-based AI video studio powered by **Three.js 3D** and **2D Ink** engines for creating 9:16 Shorts/TikToks and 16:9 story videos.

**Live App:** [viral-ai-videos.ai.studio](https://viral-ai-videos.ai.studio)

### Added
- **Dual Rendering Engines** – Interactive Three.js WebGL 3D engine alongside stylized 2D Ink presets.
- **Multi-Format Video Export** – Native `9:16` (Shorts, Reels, TikTok) and `16:9` (YouTube) export pipelines directly in the browser.
- **New Navigation & Pages** – Dedicated **Studio**, **Showcase** (preset demos with one-click load), and **FAQ** views with persistent Studio state across tabs.
- **Notifications & Privacy Controls** – Dual-layer notification system (in-app toasts + native browser completion alerts) and GDPR-compliant cookie consent settings.
- **Local-First Workflow (BYOK)** – Projects and custom API keys stay locally in the browser.

### Improved & Fixed (Three.js 3D Engine)
- Added floor-grounded walking locomotion and strict joint clamps to prevent erratic arm/limb rotations.
- Enforced minimum scene lighting floor to prevent dark shots from crushing to pitch black.
- Improved 9:16 portrait camera framing, HUD title safe-zone placement, and door interaction physics.
- Toned down floating dust particles and synced shot transitions more tightly with audio cues.

### Known Issues
- Minor shot-pacing edge cases and transition polish are still actively being refined in the Three.js 3D engine.
