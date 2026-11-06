# Required mist kernel source upload

**Destination:** [nAa-mist/kernel_xiaomi_mist](https://github.com/nAa-mist/kernel_xiaomi_mist).

The project is ready for the user's full `mist` kernel source upload. This
repository currently contains documentation only, not a validated bootable
kernel.

## Source content needed

- Complete `mist-w-oss` kernel source checkout as published/modified, including its original directory structure.
- Its exact source revision / base branch and any local patches.
- Device `build.config`, defconfig, Clang/LLVM configuration and build scripts.
- Relevant modules and board DTS/DTBO integration files, or exact pinned references
  to the dedicated `kernel_xiaomi_sm4450-modules` and
  `kernel_xiaomi_sm4450-devicetrees` repositories.
- References to the matching stock `boot.img`, `vendor_boot.img`, `dtbo.img`
  and kernel version for verification. Keep binary stock images outside public
  source repositories.

Known OSS references:
- [MiCode Xiaomi_Kernel_OpenSource mist-w-oss](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/tree/mist-w-oss)
- [MiCode kernel_build mist-w-oss](https://github.com/MiCode/kernel_build/tree/mist-w-oss)
- [MiCode kernel_devicetree mist-w-oss](https://github.com/MiCode/kernel_devicetree/tree/mist-w-oss)

## What follows the upload

1. Compare the uploaded source against the public MiCode reference and
   document any differences.
2. Check whether the common kernel source at
   `kernel/xiaomi/sm4450` is still needed, or whether the complete mist
   source should replace it in the LineageOS build manifest.
3. Resolve kernel module compatibility and build configuration.
4. Update the canonical build dependency pin in
   `nAa-mist/device_xiaomi_mist/manifests/mist-sm4450.xml`.
5. Compile, diagnose errors, and validate boot compatibility only on a
   confirmed matching test device.

**No kernel compilation or device boot success is claimed yet.**
