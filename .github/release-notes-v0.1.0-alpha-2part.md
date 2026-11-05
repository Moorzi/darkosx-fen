## dArkOSX Fen v0.1.0-alpha (R36S / R36XX)

Pre-release public image. Custom firmware for R36S / R36XX built on dArkOS — not stock upstream dArkOS. Codename **Fen**.

NDS retail BIOS/firmware stripped. Free MSX C-BIOS included where applicable. No ROMs or copyrighted console BIOS are packaged; bring your own dumps from hardware you own.

The [project website](https://moorzi.github.io/darkosx-fen/) download button stays **Coming Soon**. Both zip parts below are live and checksum-verified.

### Download (2 parts)

Download **both** files:

1. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.001`
2. `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.002`

Also grab `PARTS.sha256`, `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.zip.sha256`, `dArkOSX-Fen_R36S_v0.1.0-alpha.img.xz.sha256`, and `SHA256SUMS`.

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

**SHA256 (joined zip):** `a33669acf574397fd61fef80510ecfa26e3376ecbf8b5d0d36c56e36bc5820f0`

**SHA256 (xz):** `f6b2d88577405e0e880d542b22df9db55f7b50850394e5f0b07cdb439a3fc6d5`

**SHA256 (parts):** see `PARTS.sha256` on this release.

### Notes

- The previous seven `.img.xz.part0N` assets are gone — use this 2-part zip set only.
- Optional lock screen uses a **device PIN**.
- Change default Wi-Fi credentials (`ark` / `ark`) before sharing a network.
- Public status stays qualitative; detailed benches stay private.
