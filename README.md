# dArkOSX — a fresher experience for R36S and R36XX

[Project website](https://moorzi.github.io/darkosx-fen/) · [Release](https://github.com/Moorzi/darkosx-fen/releases/tag/v0.1.0-alpha) · [Built on dArkOS](https://github.com/christianhaitian/dArkOS)

dArkOSX turns your **R36S or R36XX** into something that feels finished the moment it wakes — a refreshed look, smoother everyday use, and stronger play on demanding games. Built on **dArkOS**, Fen brings a redesigned menu, a tiled Control Centre, **dynamic boot** visuals, **RAM Plus**, **MSX out of the box**, and an optional lock screen with a **device PIN** you will not find on other handheld OSes. The polish on the surface is backed by real system work underneath.

**Fen** is this build’s codename. Independent community project — not an official dArkOS release.

Feedback: [site comments](https://moorzi.github.io/darkosx-fen/#feedback)

## Get dArkOSX

The finished Fen image is a verified **two-part** download on GitHub: [v0.1.0-alpha](https://github.com/Moorzi/darkosx-fen/releases/tag/v0.1.0-alpha). The website download button opens when we promote it. Read the release notes and **back up your memory card** before installing.

### Install from GitHub

1. Download both `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001` and `.002`, plus `PARTS.sha256`, `SHA256SUMS`, and the zip / xz `.sha256` files.
2. **Join** the parts (`cat …001 …002 > …img.xz.zip` on Linux/macOS, or `copy /b …001+…002 …img.xz.zip` on Windows).
3. **Verify** the joined zip hash, unzip to `.img.xz`, verify that hash, then decompress to `.img`.
4. **Flash** with [balenaEtcher](https://etcher.balena.io/) or `dd` (double-check the target device).
5. Change the default `ark` / `ark` Wi-Fi credentials before sharing a network. Optional lock uses a **device PIN**.

Full join / verify / flash wording also lives on the [website status section](https://moorzi.github.io/darkosx-fen/#install).

**No games, ROMs, or copyrighted console BIOS are included.** Retail Nintendo DS BIOS files have been removed. **MSX** includes free **C-BIOS**, so it works out of the box. Other systems that need copyrighted BIOS stay user-supplied.

## What’s different?

### Looks and everyday use

A dynamic boot logo and background lead into a refreshed EmulationStation menu, with a terminal-inspired theme, a tiled Control Centre, and a redesigned system panel. A guided first-boot setup walks you through the basics.

Fen reaches the games menu **faster** than stock while showing those dynamic visuals — stock stays on the plain boot path.

### Demanding games

Fen is **faster** on demanding titles — especially **Dreamcast** — with **PlayStation** and **Nintendo 64** ahead too. Lighter classics stay silky; the heavy games are where Fen shines.

**RAM Plus** adds extra working memory when the handheld’s built-in 1 GB fills up — useful for heavy games like N64 and Dreamcast. It is not extra physical RAM.

### Lock screen and device PIN

No other handheld OS we know of ships a lock screen like this. Turn on the optional lock screen, pick from **ten backgrounds** under **Display & Sound → Lock Background**, and set a **device PIN** with a button combo when you want to keep casual eyes off the menu. Your background choice stays across sleep and restart.

### Wi-Fi file transfer

Wi-Fi file sharing and the web file browser stay available, same as the community expects. Change the default `ark` / `ark` credentials before sharing a network.

## Interface previews

[![dArkOSX Control Centre captured on R36S](docs/assets/screens/control-centre.webp)](docs/assets/screens/control-centre.png)

[![dArkOSX EmulationStation system views](docs/assets/screens/systems-grid.webp)](docs/assets/screens/systems-grid.jpg)

More on the [website gallery](https://moorzi.github.io/darkosx-fen/#look), including lock-background previews.

## Names that sound similar

- **dArkOSX** (this project) — independent custom firmware for R36S / R36XX, published as [Moorzi/darkosx-fen](https://github.com/Moorzi/darkosx-fen).
- **dArkOS** — the upstream handheld firmware this build is based on ([christianhaitian/dArkOS](https://github.com/christianhaitian/dArkOS)).
- **darkos** (Android) — a different Wine-on-Android project; not this handheld firmware.

## Notes

Recorded checks so far are on an **R36S** (not a separate R36XX validation). Battery-life testing is still pending. Detailed stopwatch and frame-rate tables stay private; public copy stays qualitative.

## Legal and credits

No games, ROMs, or copyrighted console BIOS are included. Use only material you are legally entitled to use. dArkOSX is not affiliated with or endorsed by Christian Haitian, upstream dArkOS maintainers, the Android darkos project, or any console manufacturer.

VT323 and Share Tech Mono are under the SIL Open Font License; see `docs/assets/fonts/`.
