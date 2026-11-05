## dArkOSX Fen v0.1.0-alpha (R36S / R36XX)

Pre-release public image. Custom firmware for R36S / R36XX built on dArkOS — not stock upstream dArkOS.

NDS retail BIOS/firmware stripped. Free MSX C-BIOS included where applicable. No ROMs or copyrighted console BIOS are packaged; bring your own dumps from hardware you own.

### Download (2 parts)

Download **both** files:

1. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001`
2. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002`

Also grab `PARTS.sha256`, `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256`, `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256` and `SHA256SUMS`.

#### Linux / macOS

```bash
# 1. Join
cat dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001 \
    dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002 \
  > dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip

# 2. Verify the zip
sha256sum -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256

# 3. Unzip → .img.xz
unzip dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip

# 4. Verify the xz
sha256sum -c dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256
# expected: f6b2d88577405e0e880d542b22df9db55f7b50850394e5f0b07cdb439a3fc6d5

# 5. Decompress
xz -dk dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz

# 6. Flash (replace /dev/sdX — double-check the device)
sudo dd if=dArkOSX-Fen_R36S_v0.1.0-alpha.img of=/dev/sdX bs=4M status=progress conv=fsync
```

Or flash the `.img` with [balenaEtcher](https://etcher.balena.io/).

#### Windows

```bat
copy /b dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001+dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002 dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip
```

1. Unzip with 7-Zip or Explorer.
2. Decompress the `.xz` with 7-Zip to get the `.img`.
3. Flash with balenaEtcher.

**SHA256 (zip):** `__ZIP_SHA__`

**SHA256 (xz):** `f6b2d88577405e0e880d542b22df9db55f7b50850394e5f0b07cdb439a3fc6d5`

### Notes

- The previous seven `.img.xz.part0N` assets are superseded — use this 2-part zip set only.
- Stock-vs-build FPS tables are still being measured on device and will be added as they land.
