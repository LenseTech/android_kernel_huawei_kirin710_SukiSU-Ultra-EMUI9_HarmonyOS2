# SukiSU-Ultra for Huawei nova 3i based on EMUI9.1/HarmonyOS2.0.

**English** | [简体中文](README_CN.md)
#

# Due to poor compatibility of SukiSU Ultra versions above v3.1.8 with 4.x kernels, maintenance of this project has been discontinued.

## Features
- Provide SukiSU (Another kernel-based root solution) Root.
- Module installation support.

## Devices
- HUAWEI Nova 3i(INE-AL00) based on HarmonyOS 2.0. Feel free to test for your device. (Also works theoretically on Huawei nova 5i based on HarmonyOS 2.0).

## File description
- There are two types of kernel image:
PM：Permissive
Non-PM：Enforcing
- Non-PM image also work on EMUI9.1.0.241.

## Usage
- Make sure your device bootloader has been unlocked.
- Reboot into Fastboot mode, then type in adb command line: `fastboot flash kernel "PATH\TO\YOUR\KERNEL"`.
- Type `fastboot reboot` or reset by long-press the power button.
- Install official [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra/releases/latest) manager. 

### Note: If you're using my previous build of KernelSU, you have to WIPE DATA after flashing this kernel or the manager may crash! Please BACKUP YOUR DATA in advance!

## Attension
- Both kernels can be used when other GSIs are installed. Tested GSIs: [Arrow OS v9.0](https://sourceforge.net/projects/arrow-os/files/arrow-9.x/GSI/27_Jan_2020/), [LineageOS 16 by altairfr](https://sourceforge.net/projects/altairfr-huawei/files/LeaOS-16.0/).
- Do NOT flash PM kernel on EMUI9. It will cause Wifi function failure.

## Known Issues
- SELinux will remain Enforcing after flash PM kernel on HarmonyOS 2.0 and EMUI9.

## Downloads
- [Releases](https://github.com/LenseTech/android_kernel_huawei_kirin710_SukiSU-Ultra-EMUI9_HarmonyOS2/releases/latest).

## Troubleshooting
- Q1 : Stuck in "Phone is starting" after flashing a module?
- A1 : Please refer to KernelSU's [Rescue from Bootloop Guide](https://kernelsu.org/guide/rescue-from-bootloop.html).
- Q2 : Unable to download module updates in manager?
- A2 : Please manually grant stroage permission in system settings.
- Q3 : Blank page when opening WebUI?
- A3 : Please update your android system webview or chrome.
- Q4 : KPM or susfs support?
- A4 : No. The kernel source code does not support adding those features.


## Credits
- [KernelSU](https://github.com/tiann/KernelSU/), [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra): The powerful root tool.
- [@Coconutat](https://github.com/Coconutat/): Some kernel compilation skills.

Sorry for my poor English ;)

