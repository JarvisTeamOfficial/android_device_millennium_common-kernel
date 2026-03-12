# Common Millennium Prebuilt Kernel

1. HayaseYuuka Kernel(yuuka/Image.gz)
   - Built from [Yuuka source](https://github.com/MillenniumOSS/android_kernel_common_android12-5.10/tree/yuuka-rebase)
   - with MGLRU backports
   - Used by LG8n

2. KagamiChihiro Kernel(chihiro/Image.gz)
   - Built from [Chihiro source](https://github.com/MillenniumOSS/android_kernel_common_android12-5.10/tree/chihiro-rebase)
   - For devices that can't handle MGLRU(LH7n, LG7n, X678B, and CK7n)

---
# How to use

1. Use [this](https://github.com/MillenniumOSS/android_device_tecno_LH7n/commit/fb2acc585b56ff5c25ebe8ba5400755b8fa63629) commit as reference

2. then change LOCAL_KERNEL to:
```
LOCAL_KERNEL := $(COMMON_GKI_PATH)/chihiro/Image.gz
```


---
## A notice to builders if you plan to use this on your devices

- `Yuuka` is known to be picky on which devices it can run on and is only confirmed to be stable in LG8n
- If you don't know if your device can handle Yuuka, point your LOCAL_KERNEL to chihiro/Image.gz
