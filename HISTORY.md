# mist kernel repository provenance and scope

Migrated the original `kernel/xiaomi/mist/README.md` exactly from
[nAa-mist/mist-bringup](https://github.com/nAa-mist/mist-bringup)
historical source commit
[2b6d0953](https://github.com/nAa-mist/mist-bringup/commit/2b6d0953fc8d59d4218fdaafbd8b25d19c318918).

This repository is a **mist-device-specific kernel reference/scaffold**.
It does **not** yet contain a fully imported, tested Xiaomi kernel.

The verified SM4450/Parrot common build integration currently uses upstream
xiaomi-ravelin repositories for kernel, kernel modules and device trees. They
should be mirrored or developed in **separate** owner repositories after
those repositories are created. Those common sources should not be pasted into
this mist-specific repository without a clear integration plan.

The original research, module/fstab/AVB inspection data and all original
commit history remain in `nAa-mist/mist-bringup`. The kernel build has
not been compiled or boot-tested as part of this migration.
