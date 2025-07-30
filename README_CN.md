# 适用于华为Nova 3i EMIU9.1/鸿蒙2.0底包的SukiSU-Ultra

[English](README.md) | **简体中文**

## 功能
- 为华为Nova 3i提供SukiSU-Ultra Root。
- 可安装模块。

## 适用设备
- 基于鸿蒙2.0的华为Nova 3i(INE-AL00)，其他同型号设备请自行测试（Nova 5i鸿蒙2.0底包理论可用）。

## 文件说明
- 压缩包内共有两种内核镜像，分别代表两种SELinux状态：
PM：宽容模式
无PM：强制执行

## 使用方法
- 确保Bootloader已经解锁。
- adb命令行输入`fastboot flash kernel "你的内核路径"`。
- 使用`fastboot reboot`或长按电源键重启手机。
- 安装[官方SukiSU-Ultra管理器](https://github.com/SukiSU-Ultra/SukiSU-Ultra/releases/latest)。

### 注意：如果你正在使用的是我的上一个KernelSU构建版本，请在刷入镜像后双清，否则管理器可能闪退！在操作前请提前备份好数据！

## 注意事项
- 在刷入其他GSI的情况下两种内核均可使用。已测试的GSI：[Arrow OS v9.0](https://sourceforge.net/projects/arrow-os/files/arrow-9.x/GSI/27_Jan_2020/)、[LineageOS 16 by altairfr](https://sourceforge.net/projects/altairfr-huawei/files/LeaOS-16.0/)。
- 请勿在EMUI9刷入PM内核，会导致连不上WIFI。

## 已知问题
- 由于KernelSU的ksud.c文件无法对低于安卓10的系统正确处理init以及应用KernelSU修改的SELinux规则，在EMUI9和HarmonyOS 2.0刷入PM内核后，SELinux状态仍为强制执行。

## 故障排除
- Q1 : 刷入模块后开机卡在“手机正在启动”？
- A1 : 请参照KernelSU [救砖教程](https://kernelsu.org/zh_CN/guide/rescue-from-bootloop.html)。
- Q2 : 在管理器内无法下载模块？
- A2 : 请在系统设置里手动为SukiSU-Ultra管理器授予存储权限。
- Q3 : 模块WebUI一片空白？
- A3 : 请更新Android System Webview或Chrome浏览器。
- Q4 : KPM或susfs支持？
- A4 : 无。内核源码不支持。

## 下载
- 请转到[发行版](https://github.com/LenseTech/android_kernel_huawei_kirin710_SukiSU-Ultra-EMUI9_HarmonyOS2/releases/latest)下载。

## 鸣谢
- [KernelSU](https://github.com/tiann/KernelSU/), [SukiSU-Ultra](https://github.com/SukiSU-Ultra/SukiSU-Ultra)：提供Root方案。
- [@Coconutat](https://github.com/Coconutat/)：提供内核的编译思路和技巧。
