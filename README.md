# dArkOSX-Fen (dark OS) for R36S / R36XX

**dArkOSX-Fen** (also searched as **dark OS** / **darkosx**) is a community build of custom firmware for **genuine R36S** handhelds (**RK3326**), based on [dArkOS](https://github.com/christianhaitian/dArkOS). Built and tested on a genuine R36S. R36XX owners can try it, but it is not separately validated yet.

It is meant to feel finished the second it wakes: dynamic boot, a redesigned EmulationStation theme, guided first-boot setup, optional lock screen with a **device PIN**, free MSX C-BIOS, RAM Plus, and Wi-Fi file transfer.

- **Site:** https://moorzi.github.io/darkosx-fen/
- **Download / release:** https://github.com/Moorzi/darkosx-fen/releases/tag/v0.1.0-alpha
- **Feedback:** https://github.com/Moorzi/darkosx-fen/issues

Genuine R36S, typically V21 / V22-ish. Clones usually want RE or a clone-specific build. Independent community project. Not an official dArkOS release.

## What's in it

- Dynamic boot logo and background instead of the plain stock path
- Redesigned EmulationStation theme and tiled Control Centre
- Guided first-boot setup: welcome, name, Wi-Fi, PIN, lock and BIOS help. Board and panel are chosen in the image boot selector, not this wizard
- Optional lock screen with a device PIN and ten backgrounds
- MSX ready out of the box. Free **C-BIOS** ships in the image
- Heavier systems get real attention (Dreamcast especially; PlayStation and N64 in good shape). Lighter classics stay silky
- **RAM Plus** when the built-in 1 GB fills up on demanding titles
- Wi-Fi file transfer and the web file browser stay. Change the default `ark` / `ark` credentials before sharing a network

## Download

**Required:** only the two zip parts from the [v0.1.0-alpha release](https://github.com/Moorzi/darkosx-fen/releases/tag/v0.1.0-alpha):

1. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001`
2. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002`

**Optional, recommended:** `PARTS.sha256`, `SHA256SUMS`, `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256`, and `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256`. You can skip the hash files and still join and flash. Verifying is the safer path.

**Back up your microSD first. Flashing wipes the card.**

## Install

### 1. Join the two parts

Linux / macOS:

```bash
cat dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001 \
    dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002 \
  > dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip
```

Windows (Command Prompt):

```bat
copy /b dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001+dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002 dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip
```

### 2. Verify (optional, recommended)

Linux:

```bash
sha256sum -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256
```

macOS:

```bash
shasum -a 256 -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256
```

Windows (PowerShell). Compare the output to the hash in the `.sha256` file:

```powershell
Get-FileHash .\dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip -Algorithm SHA256
```

### 3. Unzip, decompress, flash

Linux / macOS:

```bash
unzip dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip
# optional: sha256sum -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256
# macOS:   shasum -a 256 -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256
xz -dk dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz

# Flash with balenaEtcher, or:
sudo dd if=dArkOSX-Fen_R36S_v0.1.0-alpha.img of=/dev/sdX bs=4M status=progress conv=fsync
# Double-check /dev/sdX. Wrong device wipes the wrong disk.
```

Windows: unzip with 7-Zip or File Explorer, decompress the `.xz` with 7-Zip, then flash the `.img` with [balenaEtcher](https://etcher.balena.io/).

### 4. Boot selector, then first-boot wizard

These are two different steps:

1. **Image boot selector:** match your board and panel here so you do not black-screen. This is not part of the guided wizard.
2. **Guided first-boot wizard:** welcome, name, Wi-Fi, PIN, lock and BIOS help.
3. Change the default Wi-Fi login (`ark` / `ark`) before sharing a network.
4. Optional lock screen: set a **device PIN** and pick a lock background under Display & Sound.

## Checksums

| What | SHA256 |
| --- | --- |
| Joined zip | `a33669acf574397fd61fef80510ecfa26e3376ecbf8b5d0d36c56e36bc5820f0` |
| `.img.xz` | `f6b2d88577405e0e880d542b22df9db55f7b50850394e5f0b07cdb439a3fc6d5` |
| Each part | see `PARTS.sha256` |

## BIOS honesty

- **No ROMs** are included
- Free **MSX C-BIOS** is included, so MSX works out of the box
- Copyrighted BIOS for other systems (GB / GBC / GBA / PSX / NDS and similar) is **not** included. Supply your own where needed. First-boot help lists what is still missing

## Hardware note

Built and tested on a **genuine R36S**. R36XX is not separately validated yet. Clones usually want RE or a clone-specific build.

## Interface previews

[![dArkOSX-Fen Control Centre on R36S](docs/assets/screens/control-centre.webp)](docs/assets/screens/control-centre.png)

[![dArkOSX-Fen EmulationStation system views](docs/assets/screens/systems-grid.webp)](docs/assets/screens/systems-grid.jpg)

More on the [website gallery](https://moorzi.github.io/darkosx-fen/#look), including lock-background previews.

## Names that sound similar

- **dArkOSX-Fen** / **dArkOSX** / **dark OS** (this project): independent custom firmware built and tested on genuine R36S, published as [Moorzi/darkosx-fen](https://github.com/Moorzi/darkosx-fen)
- **dArkOS**: the upstream handheld firmware this build is based on ([christianhaitian/dArkOS](https://github.com/christianhaitian/dArkOS))
- **darkos** (Android): a different Wine-on-Android project; not this handheld firmware

## Legal and credits

No games, ROMs, or copyrighted console BIOS are included. Use only material you are legally entitled to use. dArkOSX-Fen is a community build on dArkOS and is not affiliated with or endorsed by upstream dArkOS maintainers, the Android darkos project, or any console manufacturer.

Thanks to the dArkOS project for the upstream base this build stands on.

VT323 and Share Tech Mono are under the SIL Open Font License; see `docs/assets/fonts/`.
