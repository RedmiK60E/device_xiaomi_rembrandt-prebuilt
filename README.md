Copyright (C) 2022 The LineageOS Project
# Device tree for Redmi K60E (rembrandt) - Prebuilt

The Redmi K60E (codenamed _"rembrandt"_) is a high-end, mid-range smartphone from Xiaomi.

It was released in December 2022.

## Device Specifications

|                   Basic | Spec Sheet                                              |
| ----------------------: | :------------------------------------------------------ |
|                     CPU | Octa-core CPU with 4x Arm Cortex-A78 up to 3.10GHz      |
|                 Chipset | Mediatek Dimensity 8200                                 |
|                     GPU | Mali-G610 MC6                                           |
|                  Memory | 8/12 GB RAM (LPDDR5 6400Mbps)                           |
| Shipped Android Version | 12 with MIUI 13                                         |
|                 Storage | 128/256/512 GB (UFS 3.1)                                |
|                 Battery | Non-removablem, Li-Po 5500 mAh                          |
|                 Display | 1440 x 3200 pixels, 6.67 inches, 120 Hz, AMOLED, HDR10+ |
|                  Camere | 48MP(Primary) 8MP(Ultra-wide) 2MP(Telephoto-macro)      |

## Device Picture
![Redmi K60E](https://cdn.cnbj0.fds.api.mi-img.com/b2c-shopapi-pms/pms_1672036696.35998614.png)

## Patches

## GPU:
> https://github.com/RedmiK60E/android_frameworks_native/commit/fceefdd9aec0e18309f909155794a406b240062e

### Telephony
> https://github.com/PixelExperience/frameworks_opt_telephony/commit/538afb21007e0497bde131b1ef327fb93ee37031

### Ims
> https://github.com/PixelExperience/frameworks_opt_net_ims/commit/ddacb4ba5ec943a410bb74ea31ea7b32003ce708

> https://github.com/PixelExperience/frameworks_opt_net_ims/commit/9de68f4da30fc61d95bdbdfbd400f8080ea00cec

## Building

### Complete zip
> Needed: [device/xiaomi/rembrandt](https://github.com/RedmiK60E/device_xiaomi_rembrandt-prebuilt); [vendor/xiaomi/rembrandt](https://github.com/RedmiK60E/vendor_xiaomi_rembrandt-prebuilt); [kernel/xiaomi/rembrandt](https://github.com/RedmiK60E/kernel_xiaomi_rembrandt)

> Added by yourself: device/xiaomi/rembrandt/prebuilts/<b>vendor.img</b>; device/xiaomi/rembrandt/prebuilts/<b>odm.img</b>; vendor/xiaomi/rembrandt/proprietary/priv-app/MiuiCamera/<b>MiuiCamera.apk</b>(This file is larger than 100 MB, or you can clone it with Git LFS)

> Patch: [Patches Needed](#Patches)

> lunch lineage_rembrandt-userdebug

> mka bacon

### DSU sideloader
> Needed: [device/xiaomi/rembrandt](https://github.com/RedmiK60E/device_xiaomi_rembrandt-prebuilt); [vendor/xiaomi/rembrandt](https://github.com/RedmiK60E/vendor_xiaomi_rembrandt-prebuilt); [kernel/xiaomi/rembrandt](https://github.com/RedmiK60E/kernel_xiaomi_rembrandt)

> Added by yourself: vendor/xiaomi/rembrandt/proprietary/priv-app/MiuiCamera/<b>MiuiCamera.apk</b>(This file is larger than 100 MB, or you can clone it with Git LFS)

> Patch: [Patches Needed](#Patches), [Drop import prebuilt vendor/odm image](https://github.com/RedmiK60E/device_xiaomi_rembrandt-prebuilt/commit/96060cfb8e85fa1a1e6728c68d08b36db233fa5d)

> lunch lineage_rembrandt-userdebug

> mka systemimage && mka productimage && cd $OUT && zip dsu.zip system.img product.img

## Credits
This tree based on Redmi Note 11T Pro+(xaga) of @wbs306
