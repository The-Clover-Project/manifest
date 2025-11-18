![banner](https://github.com/The-Clover-Project/.github/raw/main/banner8.png)
# The Clover Project | Android Open Source Software
An Android Operating System Based On AOSP.

### Requirements
- Around 500GB disk space.
- Around 32GB RAM running Linux.

### Sync our source ###
```bash
repo init -u https://github.com/The-Clover-Project/manifest.git -b 16-qpr2 --git-lfs
```
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Optional flags: ###

- **Enable Blur Effects**  
  ```make
  TARGET_ENABLE_BLUR := true
  ```
  (Default value is false.)

- **Build Pixel Launcher**  
  ```make
  TARGET_INCLUDE_PIXEL_LAUNCHER := true
  ```
  (Default value is false.)

### Build our source ###

- Set up the build environment
```bash
source build/envsetup.sh
```

- Lunch a target
```bash
lunch clover_$devicecodename-bp4a-userdebug
```

- To start compiling
```bash
mka clover -j$(nproc --all)
```