# Project

This projects aims to create a manifest used for building ArrowOS for the Nokia 8 (NB1).
All the changes are provided in separate repositories: this allows to upgrade Android with minimal effort, potentially also for future major versions.
Most of the added repositories is provided by LineageOS or CAF, so thanks to them for those repos.

# Build instructions

Follow the instructions from ArrowOS to setup a machine to build Android 12.

```
mkdir arrow && cd arrow
repo init -u https://github.com/ArrowOS/android_manifest.git -b arrow-12.0
repo sync
```

Then initialize the ROM environment and build.

```
source build/envsetup.sh
lunch arrow_NB1-userdebug
m otapackage
```