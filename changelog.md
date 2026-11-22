## ReelRig AI v0.1.0 - BETA

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
