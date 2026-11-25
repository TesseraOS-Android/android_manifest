TesseraOS
=========

Getting started
---------------

To get started with Android/TesseraOS, you will need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

### 1. Initializing the repository

Initialize the LineageOS 23.2 base tree and pull the TesseraOS local manifest:

```bash
mkdir -p ~/tessera && cd ~/tessera
repo init -u https://github.com/LineageOS/android.git -b lineage-23.2 --git-lfs --no-clone-bundle
mkdir -p .repo/local_manifests
curl -sSL https://raw.githubusercontent.com/BruxinCore/android_manifest/16.0/local_manifests/tessera_spacewar.xml -o .repo/local_manifests/tessera_spacewar.xml
```

### 2. Syncing the source

```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune
```

### 3. Building for Nothing Phone (1) (`Spacewar`)

```bash
source build/envsetup.sh
breakfast Spacewar
mka bacon
```

Repositories
------------

- `android_manifest` - Local manifests and sync instructions
- `android_vendor_tessera` - Product configuration, Selawik font family, and Metro RRO overlays
- `android_packages_apps_TesseraHome` - Default home launcher (`com.tesseraos.home`)
- `CalamityKernel-spacewar` - Linux 6.12.81 LTS kernel (`CALY-Daitaku`)

Credits
-------

All upstream authorship, commit history, and licenses are preserved:

- **Android Open Source Project (AOSP)**
- **LineageOS** (`lineage-23.2`, `android_device_nothing_Spacewar`, `android_hardware_nothing`, `android_kernel_nothing_sm7325`)
- **TheMuppets** (`proprietary_vendor_nothing_Spacewar`)
- **Microsoft** (Selawik Open Source Typeface, MIT License)
- **backslashxx** (KernelSU)
- **BruxinCore (NerokiStyle)** (TesseraOS)
