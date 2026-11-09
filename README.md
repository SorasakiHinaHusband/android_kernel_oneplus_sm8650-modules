# 一加 SM8650 外部内核模块 🧱

高通 SM8650（pineapple）平台一加机型的树外内核模块，
一加 12（`waffle`）的 MikuUI 构建负责把它们一个个拼进去。

## 谁在管这棵树

**SorasakiHinaHusband** —— 模块加载失败的话，dmesg 里见 🙏

## 分支

`Cinderella` —— MikuUI（Android 17 / BP2A）。

## 怎么用

设备树把 `TARGET_KERNEL_EXT_MODULE_ROOT` 指向这里，并在
`device/oneplus/sm8650-common/BoardConfigCommon.mk` 的
`TARGET_KERNEL_EXT_MODULES` 里点名每个模块。
内核构建会顺手编掉它们，然后照内核树里的
`modules.*.list.msm.pineapple` 分别塞进 vendor / vendor_dlkm / system_dlkm 分区。

## 许可证

除非文件里另有说明，否则按 GNU General Public License v2 授权。
