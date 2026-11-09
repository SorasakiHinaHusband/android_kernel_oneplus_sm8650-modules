# OnePlus SM8650 out-of-tree kernel modules

Out-of-tree kernel modules for OnePlus devices based on Qualcomm SM8650
(pineapple), used by the OnePlus 12 (`waffle`) MikuUI build.

## Maintainer

- **SorasakiHinaHusband** — <https://github.com/SorasakiHinaHusband>

## Branch

- `Cinderella` — MikuUI (Android 17 / BP2A)

## Usage

The device tree points `TARGET_KERNEL_EXT_MODULE_ROOT` at this directory and
lists every module in `TARGET_KERNEL_EXT_MODULES` (see
`device/oneplus/sm8650-common/BoardConfigCommon.mk`). Modules are built in-tree
by the kernel build and installed into the vendor / vendor_dlkm / system_dlkm
partitions according to the `modules.*.list.msm.pineapple` files in the kernel
tree.

## License

Licensed under the GNU General Public License, version 2, unless stated
otherwise in the individual source files.
