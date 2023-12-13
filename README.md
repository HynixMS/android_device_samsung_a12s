TWRP configuration for Samsung Galaxy A12 Nacho (a12snxx)
================================================================
 
Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa Core Cortex-A53
Chipset | Exynos 850
GPU     | Mali-G52
Memory  | 4 GB
Shipped Android Version | 11 Red Velvet Cake with One UI 3.1
Storage | 32/64/128 GB
MicroSD | Up to 256 GB
Battery | 5000 mAh (non-removable)
Dimensions | 164 x 75.8 x 8.9 mm (6.46 x 2.98 x 0.35 in)
Display | 720 x 1600 pixels, 20:9 ratio (~270 ppi density)
Rear Camera  | 48 MP, f/2.0, 26mm (wide), AF 5 MP, f/2.2, 123˚ (ultrawide) 2 MP, f/2.4, (macro) 2 MP, f/2.4, (depth) LED flash, panorama, HDR
Front Camera | 8.0 MP
Release Month | 2021, August 09

## How To Compile

# Create dirs
```
mkdir twrp; cd twrp
```

## Init repo
```
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
```

## Clone repo
```
git clone https://github.com/HynixMS/android_device_samsung_a12s -b android-12.1 device/samsung/a12s
```
## Sync recovery repo
```
repo sync
```

## Run This Command For Fix Permission denied
```
chmod +x device/samsung/a12s/mkbootimg
```

## Build
```
source build/envsetup.sh; export ALLOW_MISSING_DEPENDENCIES=true; lunch twrp_a12s-eng; mka recoveryimage
```