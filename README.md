# dArkOSX — custom firmware for R36S and R36XX

[Project website](https://moorzi.github.io/darkosx-fen/) · [Release status](https://github.com/Moorzi/darkosx-fen/releases) · [Upstream dArkOS](https://github.com/christianhaitian/dArkOS)

dArkOSX is an independent Linux **custom firmware** build for **R36S** and **R36XX** handhelds, built **on dArkOS**. It is a **ground-up rebuild, not a skin on stock firmware** — kernel work, bug fixes, hardware communication paths and audio, plus a revised EmulationStation experience. **MSX works out of the box** with free **C-BIOS** (stock typically does not ship that BIOS). On demanding titles — especially **Dreamcast** — Fen is **faster** than stock; PlayStation and N64 run ahead; classics stay full speed (not a blanket faster-than-stock claim). An **optional lock screen** with a cycle of ten backgrounds and a button-combo PIN is unique among handheld OSes we know of (convenience lock — not encryption). Fen is this build’s codename. Independent community project — not stock dArkOS or an official upstream release.

**Site:** [moorzi.github.io/darkosx-fen](https://moorzi.github.io/darkosx-fen/) · Feedback: [site #feedback](https://moorzi.github.io/darkosx-fen/#feedback)

## Image availability

**Coming soon on the [project website](https://moorzi.github.io/darkosx-fen/).** A public alpha exists at [v0.1.0-alpha](https://github.com/Moorzi/darkosx-fen/releases/tag/v0.1.0-alpha). The site download button stays Coming Soon until the easy **≤2-part** package is fully published and verified. Do not treat partial uploads as the final install path.

NDS retail BIOS are stripped; free MSX C-BIOS is included. No ROMs or copyrighted BIOS are supplied. Back up your card before flashing anything.

## What changes

- **Core rebuild:** kernel work, bug fixes and hardware communication paths form the ground-up, performance-focused rebuild programme.
- **Systems performance:** faster on demanding titles — especially Dreamcast; PlayStation and N64 ahead; classics full speed. Not a blanket faster-than-stock claim. Public site stays qualitative (no stopwatch / FPS tables).
- **RAM Plus:** 2 GB of extended / virtual memory when onboard RAM runs out — extra headroom for demanding games (N64, Dreamcast) on a 1 GB handheld.
- **MSX out of the box:** free C-BIOS ships in the image so MSX loads without adding BIOS. Copyrighted GB/GBC/GBA/PSX/NDS BIOS stay user-supplied.
- **Audio work:** part of the same rebuild programme.
- **Verified image details:** NDS retail BIOS stripped; free `drastic_bios` retained; A/B swap off by default; lock-background selection-save fix included. Mowgli is excluded from v1.

- **EmulationStation:** a terminal-style theme, tiled Control Centre and revised system panel.
- **First boot:** guided settings, confirmed with A.
- **Lock screen (unique among handheld OSes we know of):** cycle of ten backgrounds under **Display & Sound → Lock Background**, saved across sleep and restart. Unlock is an optional **button-combo PIN** — a convenience lock for the front end, **not encryption** and **not** the Linux account password.
- **Frequency policy:** settings within the published hardware clock range, without overvolting.
- **File transfer:** Samba sharing and the web file browser are retained. Change default SSH/Samba credentials (`ark` / `ark`) before sharing a network.
- **Public package:** no ROMs or copyrighted console BIOS. Supply only files you are legally entitled to use.

These describe the current build. The first release targets R36S and R36XX; the recorded device readings below are specifically from an R36S, not a separate R36XX validation.

## Interface previews

[![dArkOSX Control Centre captured on R36S](docs/assets/screens/control-centre.webp)](docs/assets/screens/control-centre.png)

[![dArkOSX EmulationStation system views](docs/assets/screens/systems-grid.webp)](docs/assets/screens/systems-grid.jpg)

The [website gallery](https://moorzi.github.io/darkosx-fen/#look) adapts to phone and desktop screens. Its lock-background selector previews Signal Fall, Emerald Nebula, Orbital Ghost, Deep Field, Event Horizon, Circuit Noir, Aurora Drift, Vector Grid, Obsidian Signal and Ghost Wave.

## Instrument readings

Recorded on one R36S on **5 November 2026 (Europe/London)**. The battery was charging at roughly 48–53% capacity. Read-only probes sampled `/proc` and `/sys`; idle figures exclude the first minute of each sample. These readings document the current build on an **R36S** (not a separate R36XX validation). Boot and systems comparisons on the [site](https://moorzi.github.io/darkosx-fen/#status) are qualitative only — detailed stopwatch and frame-rate tables are not published.

| Metric | Method | Result |
|---|---|---|
| Boot to EmulationStation | menu ready, side-by-side | Fen is **faster**, with **dynamic boot logo + dynamic background**; stock uses the plain boot path |
| EmulationStation RSS (menu) | `/proc` VmRSS | **183 MB** |
| CPU policy | sysfs | ondemand · 1008–1512 MHz |
| Idle SoC temperature | idle sample while charging | **~66 °C** median (charging) |
| Idle ES CPU share | % of one core | **~22%** median |
| System RAM | MemTotal | 895 MB |
| Systems performance | paired same ROMs | **Faster** on demanding titles — especially Dreamcast; PS1 and N64 ahead; classics full speed (not a blanket win) |

## dArkOSX vs dArkOS vs darkos

“Dark OS”, “darkos” and “dArkOS” can lead to different projects:

| Project | Purpose and relationship |
|---|---|
| [christianhaitian/dArkOS](https://github.com/christianhaitian/dArkOS) | Upstream Linux handheld firmware; use it for stock dArkOS downloads and documentation. |
| [Moorzi/darkosx-fen](https://github.com/Moorzi/darkosx-fen) | This repository: dArkOSX, an independent R36S / R36XX custom firmware build based on dArkOS. |
| [ahmad1abbadi/darkos](https://github.com/ahmad1abbadi/darkos) | A separate Wine-on-Android project, not this Linux handheld firmware. |

## Outstanding validation

- Systems vs stock verified on device (public copy stays qualitative). Battery-drain testing remains pending.

## Website

GitHub Pages serves `docs/` on `main`; `docs/.nojekyll` must remain. The page uses local fonts and responsive WebP previews, with full-size capture links. Sparse background glyphs move at 2–4 pixels per second on desktop; animation is disabled on phones and for reduced-motion preferences. Metadata, canonical URL, structured data, robots and sitemap describe this project without implying upstream affiliation. Search rankings are not guaranteed.

## Legal and credits

No games, ROMs or copyrighted console BIOS are included. Use only material you are legally entitled to use. dArkOSX is not affiliated with or endorsed by Christian Haitian, upstream dArkOS maintainers, the Android darkos project or any console manufacturer.

VT323 and Share Tech Mono are distributed under the SIL Open Font License; see `docs/assets/fonts/`.
