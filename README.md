# TesseraOS Manifest (`t-16`)

**TesseraOS** is a clean-room Android 16 Custom ROM for **Nothing Phone (1) (`Spacewar`)** built on top of **LineageOS 23.2**, faithfully bringing Windows Phone 8.1 / Metro UI geometry, typography (**Selawik** MIT), 120Hz motion physics, and Live Tiles to modern Android.

## Quick Sync & Build

```bash
mkdir -p ~/tessera && cd ~/tessera
repo init -u https://github.com/LineageOS/android.git -b lineage-23.2 --git-lfs --depth=1
mkdir -p .repo/local_manifests
curl -sSL https://raw.githubusercontent.com/BruxinCore/TesseraOS_manifest/t-16/local_manifests/tessera_spacewar.xml -o .repo/local_manifests/tessera_spacewar.xml
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune
source build/envsetup.sh
breakfast Spacewar
mka bacon
```

## Repositories
- `BruxinCore/TesseraOS_manifest` (`t-16`): Local manifests and build documentation.
- `BruxinCore/TesseraOS_vendor_tessera` (`t-16`): Global Selawik font, `0dp` Metro RRO overlays, and TesseraOS product configuration.
- `BruxinCore/TesseraOS_packages_apps_TesseraHome` (`t-16`): Privileged 120Hz WP 8.1 Metro Launcher (`com.tesseraos.home`).
- `BruxinCore/CalamityKernel-spacewar` (`CALY-Daitaku`): Linux 6.12.81 LTS kernel with `backslashxx/KernelSU`.

## Credits & Upstream Attribution
All upstream commit authorship and licenses are strictly preserved:
- **Android Open Source Project (AOSP)** - Core Android 16 platform.
- **LineageOS Project** - Base ROM (`lineage-23.2`), `device/nothing/Spacewar`, `hardware/nothing`, and `kernel/nothing/sm7325`.
- **TheMuppets** - Proprietary vendor blobs (`vendor/nothing/Spacewar`).
- **Microsoft** - Selawik Open Source Typeface (MIT License).
- **backslashxx** - KernelSU root solution.
- **NerokiStyle (`BruxinCore`)** - TesseraOS architecture, `TesseraHome`, Metro overlays, and `CALY-Daitaku` kernel.
