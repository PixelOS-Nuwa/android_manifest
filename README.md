# PixelOS

## Getting Started

To get started with the PixelOS source code, you'll need to be
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

To initialize your local repository, run:

```bash
repo init -u git@github.com:PixelOS-Nuwa/android_manifest.git -b seventeen --git-lfs
```
 or
```bash
repo init -u git@github.com:PixelOS-Nuwa/android_manifest.git -b seventeen --git-lfs --depth=1
```
Then, sync the repository:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## Building the System

Initialize the ROM build environment by sourcing the envsetup.sh script:

```bash
. build/envsetup.sh
```
 or
```bash
source build/envsetup.sh
```

After cloning the device-specific sources, use breakfast to configure the build for your device:

```bash
breakfast devicecodename
```
 eg:
```bash
lunch custom_nuwa-cp2a-userdebug
```

Start the compilation:

```bash
mka pixelos -j$(nproc --all)
```
 or
```bash
m pixelos
```

## Submitting Patches
Patches are always welcome! Feel free to submit your patches via [PixelOS Gerrit](https://review.pixelos.net/).
