# dArkOSX Fen for R36S / R36XX

Custom firmware for the **R36S** and **R36XX**, built on **dArkOS**. Codename **Fen**.

Fresh menu and Control Centre, dynamic boot logo and background, faster play on demanding games (Dreamcast leads; PlayStation and N64 ahead too), **RAM Plus**, **MSX ready out of the box**, and an optional **lock screen with device PIN**.

Site: [moorzi.github.io/darkosx-fen](https://moorzi.github.io/darkosx-fen/) · **Download image** is live there too.

## What’s in the package

- No ROMs
- Free **MSX C-BIOS** included (MSX works without hunting BIOS)
- Retail Nintendo DS BIOS / firmware **not** included — supply your own copyrighted BIOS where needed
- Clean image only — bring dumps from hardware you own

## How to install (two files)

Download **both** parts from this release:

1. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001`
2. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002`

Also download: `PARTS.sha256`, `SHA256SUMS`, `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256`, and `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256`.

**Back up your microSD first — flashing wipes the card.**

### On a Mac or Linux PC

```bash
# Join the two parts into one zip
cat dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001 \
    dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002 \
  > dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip

# Check the zip
sha256sum -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256

# Unzip → .img.xz
unzip dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip

# Check the xz
sha256sum -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256

# Decompress → .img
xz -dk dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz

# Flash (replace /dev/sdX — double-check the device!)
sudo dd if=dArkOSX-Fen_R36S_v0.1.0-alpha.img of=/dev/sdX bs=4M status=progress conv=fsync
```

Or flash the `.img` with [balenaEtcher](https://etcher.balena.io/).

### On Windows

```bat
copy /b dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001+dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002 dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip
```

1. Unzip with 7-Zip or File Explorer  
2. Decompress the `.xz` with 7-Zip to get the `.img`  
3. Flash with [balenaEtcher](https://etcher.balena.io/)

## Checksums

| What | SHA256 |
| --- | --- |
| Joined zip | `a33669acf574397fd61fef80510ecfa26e3376ecbf8b5d0d36c56e36bc5820f0` |
| `.img.xz` | `f6b2d88577405e0e880d542b22df9db55f7b50850394e5f0b07cdb439a3fc6d5` |
| Each part | see `PARTS.sha256` |

## After first boot

- Change the default Wi-Fi login (`ark` / `ark`) before sharing a network
- Optional lock screen: set a **device PIN** and pick a lock background under Display & Sound
