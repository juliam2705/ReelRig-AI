## [v0.6.0-beta] - 2026-11-27 - BIG UPDATE

### 🎨 New Viral Visual Styles & Overhauled 2D/3D Animation
- **2D Vector Cartoon Overhaul (`vectorPuppetRig2D.ts`, `stylizedSceneBackdrop2D.ts`):** Replaced primitive 2D shapes with a crisp, zero-API vector ink & 2-tone cel-shaded puppet engine featuring 12 dynamic poses, 12 cartoon expressions, audio-driven lip-sync, squash-and-stretch transitions, animated comic FX (`💧`, `💢`, `💡`, `?!`), 2-character staging, and multi-layered parallax backdrops.
- **2 New Viral 9:16 3D Styles (`stylizedToonAndBlockyRigs.ts`):** Added **`2.5D Toon-Stickman in 3D`** (vibrant daylight cel-shading, dark ink outlines, hybrid stickman-capsule rigs, and **Cross-Section Underground Cutaway** support) and **`Blocky 3D Story`** (daylight R6-style blocky avatars + high-contrast slender shadow monster archetype).
- **Realistic 3D Locomotion & Zero-Clipping Physics (`characterLocomotionSolver.ts`, `collisionAndCameraGuard.ts`):** Eliminated superhuman "Flash" movement and moonwalking via capped human speeds (`0.85–3.8 m/s`), smooth acceleration/deceleration to full stops, arc-length-driven strides, post-build world-space `Box3` Minkowski collider baking (`0.25m` A* grid), hard circle-vs-AABB push-out, and strict shot-boundary hard camera cuts with multi-ray anti-clipping.
- **3D Expressiveness & Viral Storytelling Props (`characterGestureLibrary3D.ts`, `viralShortsPropsAndFx.ts`):** Expanded 3D characters to 12+ facial expressions (with Horror anti-smile lock and saccadic eye darts), 14 body gestures with upper/lower-body layering, **Story Insert Close-Up Props** (handwritten diary with falling teardrop, carved stone rule tablet, notice card), **3D Comic Speech Bubbles**, **Diegetic Torso/Belt Counter Dials**, and **Action FX** (`Speed Trails`, `Shoe Fire`, `Time Freeze`).

### 💡 Smart Lighting, 16:9 Smooth Motion & Visual Polish
- **Smart Lighting Director (`smartLightingDirector.ts`):** Built a deterministic master lighting controller that drops room lights, ambient/hemisphere fill, and PMREM `scene.environmentIntensity` cleanly on blackout, auto-detects EN/PL power-kill cues from narration at exact word timestamps, persists darkness across shots, triggers synced circuit-breaker SFX, and engages readable **CCTV Infrared (IR) boost** during pitch-black frames.
- **3D Rendering Fixes:** Fixed volumetric flashlight cone alignment (`+Z` forward with soft shader alpha falloff), eliminated white glasses bloom blowout, restricted neon urban horizon lights strictly to city biomes, and added evidence-driven close-up inserts for window shadows and rattling door handles.
- **16:9 Smooth 60 FPS Compositor (`smoothMotionCompositor16x9.ts`):** Upgraded 16:9 Chronicles with eased sub-pixel 2D camera moves, deterministic transitions (`crossfade`, `dip_to_black`, `whip_pan_blur`, `hard_cut`), 2.5D parallax fog/weather overlays, optional 8 FPS hand-drawn boil, and animated chapter cards.

### 🎬 Longform Survival (10–40 min), Full Movie Compiler & Viral Shorts
- **Longform Survival Architect (`longformSurvivalArchitect.ts`, `survivalSupplyBoard2D.ts`):** Added `10m / 15m / 25m / 35–40m` presets, 6 everyday claustrophobic survival starters, `2 → 1 → 3` escalation structure, mid-roll curiosity bridges (anti-*Payoff Void*), realistic survival logistics, and TV-readable **Survival Supply & Tactics Boards** every 60–90s.
- **Full Movie Mode & `Test & Compare` 3-Pack (`seasonOmnibusCompiler.ts`):** Upgraded the Season Omnibus Compiler with **Full Movie Mode (35–75 min)** featuring minimalist `DAY X` chapter dividers, auto-trimmed middle A/B outros, and exact copy-ready `00:00` YouTube chapters, plus a zero-API **HD/4K 3-Variant Thumbnail & Title Pack** optimized for Connected TV and YouTube *Test & Compare*.
- **Viral Shorts Twist & Seamless Loop Engines (`viralShortsTwistDirector.ts`, `shortsParadoxAndLoopEngine.ts`):** Switched Shorts defaults to **Standalone Complete Stories** (with optional serial mode), added **`60s Dramatized Real Fact / Paradox`** (with auto `"The real story:"` description block), **`75s Tight Twist`** and **`150s Viral Mini-Movie`** (5-act structure + Rule of 3 examples), **1-Word Punch Captions**, **Zero-Fade Frame `0.0s` Scroll-Stop Guard**, and a **True Seamless Loop Builder** with live end-to-start loop preview.

### 🗳️ Interactive A/B Serial Mode & Verified Season Math
- **Interactive A/B Serial & `Season Ledger` (`seasonLedgerEngine.ts`, `serialRollUpHud.ts`):** Added the `Interactive A/B Serial` genre with AI concept generation, TypeScript-verified numeric tracking (optional in Horror/Survival, default in Serial), and an exclusive animated **Serial Roll-Up HUD** with floating `+ / -` delta popups and synced SFX.
- **Season Arc & Community Vote Flow (`seasonArcAndVotingEngine.ts`):** Added an 8–10 episode **Season Arc Planner**, `"Viewers Chose A / B"` vote input for `Episode N+1` continuity, and a deterministic 3-second animated **A vs B Voting Outro Card** inside safe zones.

### 🎙️ Pro Audio, Own-Voice Studio & Documentary Narration
- **In-Browser Voiceover Studio (`ownVoiceStudioEngine.ts`):** Added per-shot and teleprompter microphone recording directly in the browser with live VU meter, `IndexedDB` persistence, local WAV/MP3 import, and a live/export-identical **Broadcast Vocal DSP Chain** wired into 3D/2D Lip-Sync, 1:1 captions, and `-8 dB` auto-ducking.
- **Deadpan Tactical Documentary Mode (`documentaryNarrationMode.ts`):** Added a calm, minimalist 2nd-person survival narration preset with staccato short-sentence rules, warm de-essed TTS EQ, deterministic `[pause]` / `[beat]` / `[day_break]` breathing gaps (lifting room ambience during silence), a live **Pause Rhythm** slider, and a **15-Second Hook Audition** player.
- **1:1 TTS-to-Caption & Voice Identity Lock:** Unified `spokenText` as the single source of truth for TTS and captions, locked episode protagonist voices to prevent accidental mid-episode gender flips, and added a hook title sanitizer preventing truncated banners.

### 🛡️ Pre-Render QA Gate & YouTube 2026 Compliance
- **Pre-Render QA Gate & YPP Guard (`preRenderQaGate.ts`, `youtubePackagingAndYppGuard.ts`):** Added a zero-API pre-export quality gate with 1-click **Auto-Fix** covering Ledger math, 1:1 captions, voice locks, 3D physics/blackout safety, anti-AI-slop clichés, **YPP 2026 Inauthentic Content** repetitiveness checks, **Shorts >60s Content ID** safety, Frame `0.0s` brightness checks, platform-split **YouTube vs. TikTok Publish Packs** (auto-stripping raw filenames/hashtags from YouTube titles), and **Channel Identity Lock** with niche-drift warnings.

### ✨ Creator Workspace, Showcase & Onboarding UX
- **Decluttered Studio Workspace (`CollapsibleSection.tsx`):** Redesigned the Studio with Progressive Disclosure — video-first viewport layout, collapsible accordions with live status pills, collapsible Left/Right sidebars, deduplicated controls, and an accordion Shot List persisted in `localStorage`.
- **Showcase Gallery & Creator Power Tools (`ShowcaseGalleryModal.tsx`, `brandKitAndLocker.ts`, `byokCostTracker.ts`, `sessionAutoSaveAndHistory.ts`):** Added 5 zero-API playable Showcase templates with 1-click **"Open & Remix in Sandbox"**, **Creator Brand Kit** (baked MP4 watermarks & caption themes), **Character Locker**, live **BYOK Cost Meter & Spend Guard**, and silent **IndexedDB Auto-Save + 30-step `Ctrl+Z` / `Ctrl+Y` Undo/Redo**.
- **Landing Tutorial & Interactive Studio Tour (`LandingTutorialSection.tsx`, `StudioOnboardingTour.tsx`):** Added a bilingual (`EN` / `PL`) searchable 5-tab Feature Encyclopedia + 4-step Quick Start below the hero preview card and a 9-step zero-dependency Spotlight Onboarding Tour inside the Studio.

## [v0.5.0-beta] - 2026-11-25

### 🌍 True Open-World Terrain, Foliage & Elevated Structures (3D Mode)
- **Procedural Heightfield & Road Network (`openTerrainEngine.ts`):** Added continuous seeded terrain elevation with automatic smooth flattening under standalone buildings and road corridors, plus procedural asphalt highways, country roads, dirt trails, and roadside guardrails.
- **Instanced Wind-Swaying Foliage & Open Props (`openFoliageAndProps.ts`):** Added batched `THREE.InstancedMesh` grass (2,500–5,000 tufts) with deterministic `uTime` wind shaders, plus outdoor landmarks (abandoned cars with hazard lights, utility poles, fences, boulders, road signs) registered cleanly into A* navigation.
- **Elevated Vertical Structures (`elevatedStructureBuilder.ts`):** Fixed open-world room spam and added full `elevationY` verticality with anchored support frames, railings, and unified `getWalkableSurfaceY()` height snapping — including 1-click **Fire Watchtower (11m)**, **Rooftop (14m)**, **Cliff Station (10m)**, and **Elevated Bridge** presets.

### 🎬 3D Lookdev, Cinematography, Characters & Micro-FX
- **Cinematic Lookdev Pipeline (`cinematicLookdevPipeline.ts`):** Upgraded rendering to `ACESFilmicToneMapping`, procedural `PMREM` environment reflections, canvas-generated PBR `bumpMap`/`roughnessMap` + wall-bottom AO, zero-cost grounded contact shadows, and deterministic `EffectComposer` post-processing (`UnrealBloomPass`, vignette, grading, micro film grain) tuned to prevent face blowout.
- **Expressive Characters & Audio Lip-Sync (`characterFaceAnimator.ts`):** Upgraded character rigs with sculpted `CapsuleGeometry` silhouettes and layered outfit details, dynamic Canvas facial expressions with deterministic blinking and gaze tracking, secondary motion (breathing, head-lead turns, backpack bob, flashlight tremor), and deterministic 60 Hz RMS audio-driven lip-sync.
- **Interactive Horror Cinematography (`cinematicCameraAndFx.ts`):** Added proximity-swinging & SFX-rattling hinged 3D doors, per-shot lens modes (**CCTV**, **Bodycam**, **Night Vision**), **Crash Zoom**, **Dolly Zoom (Vertigo)**, SFX-synced **Impact Shake**, controlled **Blackout** windows with volumetric flashlight cones, hard camera line-of-sight wall raycasting, and manual **A → B** camera waypoints on the 2D Mini-Map.
- **Interior Polish, Horde & Micro-FX (`interiorPolishAndClutter.ts`, `hordeAndMicroFx.ts`):** Added batched baseboards, doorframes, ceiling beams, utility pipes, animated Canvas monitor screens, instanced micro-clutter, floating dust motes, instanced silhouette hordes (`InstancedMesh`), cold breath vapor, sparks/engine smoke, and deterministic prop pickups.

### ⚡ Dopamine Hook & Retention Engine (9:16 Shorts)
- **Automated Viral Hooks (`dopamineHookEngine.ts`):** Added toggleable **Cold Open + VHS Tape Rewind** (`0.0s–2.2s`), **Hidden Background Anomaly** comment-bait spawns, **Live Tension Telemetry HUD** (`Heart Rate BPM`, `Oxygen %`, `Battery %`, `Distance`, `Countdown`), and 4 one-click Story Director hook archetypes (`Broken Logic`, `Rule Horror`, `Countdown`, `Seamless Loop`).
- **Hyper-Dopamine Pacing & Kinetic Typography:** Upgraded `Retention X-Ray` and Auto-Fix with a `≤2.5s` impulse pacing audit, added elastic **Pop + Shake** kinetic word-by-word captions inside safe zones, and introduced world-space **3D Spatial Typography** with true camera parallax.

### 🎙️ Multi-Voice Audio, Radio DSP & Cross-Engine Story Systems (16:9 & 3D)
- **Multi-Voice Casting & Radio DSP (`multiVoiceAudioEngine.ts`):** Added per-character Gemini TTS casting, deterministic **Radio / Intercom / Phone** bandpass + soft-clip + squelch-click DSP chains, and smooth **`-8 dB` Music Auto-Ducking** mirrored identically between live preview and `OfflineAudioContext` WebCodecs MP4 export.
- **World & Inventory Bible (`seasonBibleEngine.ts`):** Added persistent cross-episode continuity tracking protagonist health/injuries, gear condition (`intact` / `low` / `broken` / `lost`), character survival status, and active mysteries — auto-synced after each episode and injected into `Episode N+1`.
- **1-Click Trailer / Short Extractor (`shortExtractorEngine.ts`):** Convert any 16:9 episode into a vertical `1080×1920` 9:16 Short via **Instant Zero-API Smart-Crop Trailer** or **Native 3D Teaser** generation.

### 🔐 Strict BYOK Security & Firestore Admin Panel
- **Bulletproof BYOK Persistence & Billing Guard (`apiKeyStorage.ts`):** Added synchronous `localStorage` key hydration, opt-in private Google Account Cloud Sync (`users/{uid}/secrets/api`), and a strict centralized `requireUserByokKey()` audit removing all developer/env API key fallbacks for safe Public Beta.
- **Firestore Access Control & Telemetry (`accessControlFirestore.ts`, `adminTelemetryService.ts`):** Migrated **Request Access** and **Allowlist** from Drive to Firestore, added **Studio Access Mode** (`Closed Beta` / `Open Sandbox + Cloud Beta` / `Public Beta` + `Maintenance Mode`), **Invite Codes** with usage caps, **Activity Funnel KPIs** + 7-day chart, **Live Client Error Log** (WebCodecs/WebGL crash tracker), **Global Broadcast Banner**, **Remote Feature Flags**, and a clean 3-tab Admin Panel layout.

## [v0.4.0] BETA - 2026-11-24 BIG UPDATE/FIX 3D THREE.JS

### 🌤️ Outdoor Sky, Weather & Horizon Engine (3D Mode)
- **Procedural Sky Dome & Celestial Lighting:** Added `skyAtmosphereEngine.ts` with a custom gradient sky shader synced to `FogExp2`, sun and moon discs aligned to the shadow-casting `DirectionalLight`, seeded twinkling starfields, and drifting `InstancedMesh` cloud layers.
- **Deterministic 3D Weather & Wind:** Added `weatherAndHorizonEngine.ts` featuring camera-centered 3D rain streaks and falling snow (automatically masked out of interior rooms), deterministic storm lightning flashes, and wind-swaying exterior trees — fully synced frame-for-frame with 30 FPS WebCodecs MP4 export.
- **Distant Horizon Ring:** Eliminated map-edge void drop-offs by generating an extended ground skirt and batched distant silhouettes (`mountains`, `forest`, `city_skyline`) matched to the world theme.
- **Exterior Windows & Atmospheric Details:** Upgraded `proceduralWorldBuilder.ts`, `modularPropKit.ts`, and `proceduralMaterialLibrary.ts` to carve real framed windows on exterior-facing interior walls (keeping sky, weather, and horizon visible from indoors), add fake volumetric light cones under streetlamps, and enable wet reflective asphalt/puddles in rain and storm modes.
- **Atmosphere & Sky Studio Controls:** Added prompt-based weather/time auto-inference plus a collapsible real-time **Atmosphere & Sky** override bar (`Time of Day`, `Weather`, `Horizon`) in 3D Studio — fully usable in **Zero-API Sandbox Mode** and persisted in `My Stories` / `.reelrig.json`.

### 🧭 3D Character Navigation & Prop Collision Fix
- **Sub-Tile Deterministic A* Pathfinding:** Added `obstacleNavigationGrid.ts` with a 0.5m walkability grid and exact prop XZ footprint colliders (`CHARACTER_RADIUS = 0.48m`) so characters cleanly navigate around tables, beds, desks, crates, and shelves instead of clipping through furniture.
- **Path Smoothing & Doorway Guarantees:** Implemented ray-vs-AABB string-pulling smoothing for natural turns, enforced a `1.4m` doorway clearance zone during prop placement, and added `resolveSafeStandingPoint()` snapping so stationary spawns never clip into props or walls while staying 100% deterministic for MP4 export.

## [v0.3.0] - 2026-11-24 BIG UPDATE

### 🗺️ Procedural 3D World Engine (Prompt-to-Map)
- **Dynamic Multi-Location Grid Blueprints:** Added `mapBlueprintSchema.ts` and `proceduralWorldBuilder.ts` so prompts can automatically generate connected 4–16+ zone 3D worlds mixing interiors and exteriors, with automatic shared-wall doorway carving, safe prop slots, and overlap/connectivity validation.
- **Procedural PBR Themes & Modular Prop Kit:** Built `proceduralMaterialLibrary.ts` (8 canvas-generated PBR themes: `hospital`, `school`, `bunker`, `supermarket`, `forest`, `street`, `spaceship`, `office`) and `modularPropKit.ts` (~24 stylized interior/exterior props with zero external `.glb` dependencies).
- **60 FPS Large-Map Optimizations:** Implemented `THREE.InstancedMesh` batching, dynamic shadow Light Pooling (capped at 2–3 active shadow lights), graph-based Zone Culling, and deterministic cross-room BFS pathfinding (`findWorldPath`) with doorway swings and interior camera wall clamping.
- **2D Floorplan Mini-Map:** Added a collapsible interactive 2D Mini-Map and **Regenerate World Layout** (`Compact` / `Medium` / `Large`) controls inside the 3D Studio.

### 🎨 16:9 Survival Chronicle Engine (Editorial & Continuity Upgrade)
- **Zero-Cost Programmatic Editorial Cards:** Added `editorialCardRenderer.ts` to render crisp, deterministic Canvas data cards (`day_intertitle`, `supplies_tracker`, `threat_counter`, `rule_card`, `fact_chart`) with zero image-API cost.
- **Optical Masks & Clean Cinema Mode:** Added `peephole` and `binoculars` framing masks, a snappy hard cut-in pacing preset (`Beanie Cut-In Rhythm`), and **Clean Cinema Mode** (on-screen captions OFF by default for 16:9 while keeping `.srt` bundle export intact).
- **Persistent Room State & Cast Signatures:** Added `roomStateContinuity.ts` so permanent plot changes (barricades, candles, damage) persist across days in the same location, paired with recurring `castSignatures` and grounded survival + mystery story direction.
- **Full Movie Compilation Builder:** Added **Combine Episodes (Full Movie)** in `My Stories` to merge multiple 16:9 episodes into one unified long-form timeline with recalculated YouTube chapter timestamps.

### 📺 Season Continuity ("Continue to Next Episode")
- **Episode Carryover Engine:** Added `seasonContinuityEngine.ts` to extract and inherit ending day counts, remaining water/food supplies, surviving cast + pinned visual references, active room states, established rules, and open cliffhangers across `S1E1 → S1E2 → S1E3`.
- **Series Management:** Added the editable **Next Episode Continuity Brief** modal (with optional 15s *"Previously On"* cold open), series grouping badges in `My Stories`, and 1-click **Stitch Season (Full Movie)**.

### ⚡ Retention X-Ray Auto-Fix, Waveform & Pinpoint SFX
- **1-Click Retention Auto-Fixer:** Extended Retention X-Ray with `retentionAutoFixer.ts` — automatically splits monotonous dead zones, injects zero-cost pattern interrupts/masks, trims weak hooks with 1-click Undo, and offers an optional BYOK-only AI hook rewrite.
- **Mini-Timeline Waveform & Pinpoint SFX:** Added `waveformPeakExtractor.ts` (audio peak strip + silence gap indicators) and `proceduralSfxSynth.ts` (8 zero-404 Web Audio thriller cues including `three_slow_knocks`, `radio_static_burst`, and `music_cut_drop`), allowing click-to-place draggable SFX markers baked cleanly into both live playback and deterministic 30 FPS MP4 export.

### 🛡️ Zero-API Sandbox & UI Polish
- **Try Without API Key (Zero-API Sandbox):** Added `sandboxModeGuard.ts` enforcing a strict zero-outbound-API billing guard when no user BYOK key is present — letting visitors test 3D/2D editing, editorial cards, mic voiceovers, procedural SFX, and local WebCodecs MP4 exports without touching developer quota.
- **UI & Visual Refinements:** Applied layout and styling polish across the Studio interface.

## ReelRig Ai [v0.2.0] - 2026-11-23 usual update

### 🎞️ Deterministic Video Export (WebCodecs + Mediabunny)
- **Frame-by-Frame 30 FPS MP4 Exporter:** Replaced real-time `MediaRecorder` drops with deterministic `1/30s` stepped offline rendering (`deterministicMp4Exporter.ts`) across both Three.js 3D and 2D Ink modes, ensuring smooth MP4 exports even on slower GPUs/laptops.
- **Zero-Drift Audio Muxing:** Added `OfflineAudioContext` rendering to mix TTS, Custom Voiceovers, Music/AI Auto-Score, and SFX cleanly into the MP4 container with exact frame sync, progress counter, cancel support, and automatic `MediaRecorder` fallback on unsupported browsers.

### 👁️ 16:9 2D Ink Vision Director & Consistency
- **Multi-Reference Gemini Anchor Pipeline:** Upgraded `inkAnchorPipeline.ts` to natively pass multiple inline reference images (pinned Canon Character/Style Anchor + Location Master Anchor) on every shot to eliminate style and room drift by Act 3, including a 1-click **"Pin Panel 1 as Style Anchor"** control.
- **AI Glitch Watchdog (Auto-QC):** Added a toggleable, single-call Gemini Flash vision pass (`visionDirectorQc.ts`) that detects extra limbs, garbled text, and broken style — automatically running at most 1 targeted retry to fix glitches while keeping BYOK costs capped.
- **Smart Framing Pop-Cuts:** Used detected `characterFace`, `keyProp`, and `secondaryFocus` bounding boxes to center 16:9 hard cut-ins precisely on subjects with headroom protection and edge clamping instead of blind center crops.

### 🧩 Studio UX, Timeline & Queue Reliability
- **Focus Mode & Mobile View:** Added collapsible left/right sidebars with `ResizeObserver` canvas scaling, replaced blank preview states with interactive demo/action overlays, and built a clean `<768px` mobile preview experience.
- **Showcase "Open & Remix in Studio":** Added 1-click cloning of featured 9:16 3D and 16:9 2D Ink presets directly into an editable Studio workspace.
- **Interactive Proportional Mini-Timeline:** Upgraded the shot strip to proportional duration blocks with Drag & Drop reordering, quick `+` shot insertion, deletion, and per-shot readiness badges.
- **Resilient Generation Queue:** Added centralized batch controls (`resilientGenerationQueue.ts`) with Pause/Resume/Cancel, automatic exponential backoff on `HTTP 429` / `503` rate limits, and subtle background tab completion alerts.

### 🛠️ Pro Creator Workflow & Publishing
- **Channel Brand Kit:** Added reusable channel presets (`brandKitStore.ts`) saving pinned character PNGs, accent color, paper tone, default voice/BGM, captions, and optional corner watermarks for 1-click reuse on new series.
- **Editing Bundle (`.zip`) & Project Backup (`.reelrig.json`):** Added client-side `.zip` export (`projectZipExporter.ts`) with full-res visuals, per-shot audio files, timecoded `.srt` subtitles, and script metadata for DaVinci Resolve/CapCut, plus portable `.reelrig.json` backup/import and a quick Bug Report / Feedback link.
- **Publish Pack & Thumbnail Feed Preview:** Added auto-calculated YouTube chapter timestamps (`0:00`+) with 1-click copy inside `Publish Pack`, plus a live Dark/Light Mobile & Desktop YouTube feed preview inside `Create Thumbnail`.

### 🐛 Bug Fixes
- **Fixed Audio Playback & Export `HTTP 404`:** Implemented a centralized audio asset resolver handling IndexedDB blobs and base64/data URIs directly without blind `fetch()` calls, safely clearing stale `blob:` URLs and dead demo paths so playback and `Export Video` never crash on missing audio.
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
