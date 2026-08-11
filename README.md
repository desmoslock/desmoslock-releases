# DesmosLock releases

This public repository contains DesmosLock installer releases and their provenance.
The proprietary application source remains in its private repository.

No replacement macOS release has been published yet. The defective v1.0.0 macOS
DMGs will not be mirrored here.

Every stable release must contain exactly these assets:

- `DesmosLock-mac.dmg`
- `DesmosLock-mac-intel.dmg`
- `DesmosLock-setup.exe`
- `DesmosLock.AppImage`
- `SHA256SUMS.txt`
- `RELEASE-PROVENANCE.json`

Verify a downloaded release from the directory containing all six files:

```bash
shasum -a 256 --check SHA256SUMS.txt
```

The v1.0.1 macOS builds use a valid ad-hoc code signature and hardened runtime, but
they are not Apple-notarized. On first launch, macOS may identify the developer as
unknown. Open **System Settings → Privacy & Security**, find the blocked DesmosLock
message, and choose **Open Anyway** once. Subsequent launches work normally.

GitHub release immutability is enabled. Published release assets and release tags
must never be replaced; a correction requires a newer version.
