---
description: 淬火 3.5 系列 Electron 客户端与 MOD 使用手册
---

# 介绍

淬火（Quenching）是魔兽争霸 III 的画面与功能增强 MOD。你可以通过客户端安装资源包、管理地形与皮肤、调整光照，并启动游戏或地图。

本手册面向 **淬火 3.5 系列 Electron 客户端**。旧 WPF 客户端的按钮、截图和 .NET 安装步骤不适用于这一版。近期测试版的安装弹窗、重新安装文案和资源对齐修复，见[客户端与资源包更新](an-zhuang/geng-xin.md)中的版本说明。

## 下载与开始使用

- [官方网站](https://qm.txzy.net/)：公告、下载入口与资源说明。
- [Windows 和 Mac 客户端](https://github.com/UIZorrot/Quenching-Client/releases/tag/3.5)：下载便携 ZIP，解压后运行。
- [完整 MOD 资源包](https://github.com/UIZorrot/Quenching-Assets/releases/tag/3.5)：用于补齐模型、纹理等游戏资源。

第一次使用请读[常规安装](an-zhuang/chang-gui-an-zhuang.md)。Mac 用户请读[Mac 安装](an-zhuang/mac-an-zhuang.md)。

## 客户端与完整包

客户端负责设置、资源切换和启动；完整包提供 MOD 的模型、纹理等资源。下载客户端不会同时下载完整包。

没有完整包也可以开启 MOD 的基础功能。需要完整资源的选项会提示你安装完整包；你仍需另外获取并安装它。

## 游戏版本与画质

客户端可按检测结果选择游戏版本，也可在首页手动选择版本范围：

| 游戏版本范围 | 用途 |
| --- | --- |
| 1.36 及以下 | 1.32 至 1.36 系列重制版游戏 |
| 2.0–2.02 | 2.0.0 至 2.0.2 |
| 2.03–2.04 | 2.0.3 至 2.0.4 |
| 3.0 及以上 | 3.0 系列及后续版本对应的资源配置 |

这些范围指 **魔兽游戏版本**，与淬火 3.5 的 MOD 版本不同。

首页的 SD（经典）、HD（高清）、DE（决定版）选择决定客户端应用哪一套资源。DE 对应 3.0 及以上游戏；选择 MOD 画质不会为游戏账号解锁未购买的高清内容。

## 系统与平台

Windows 用户解压客户端 ZIP 后运行 `QMClient.exe`，保留旁边的 `resources` 等目录。Electron 客户端不要求安装旧 WPF 使用的 .NET Framework 4.7.2。

Mac 用户使用 `QMClient.app`。当前 3.5 Release 的 Mac 包面向 Apple Silicon；Intel Mac 用户需核对下载页是否提供 x64 包。Mac 客户端目前通过手动替换便携包更新。

你需要一份可以正常运行的魔兽争霸 III 游戏。Linux 原生客户端不在当前发布范围内。

## 遇到问题

- [安装与资源包排障](chang-jian-wen-ti/an-zhuang-yu-zi-yuan.md)
- [游戏画面与启动排障](chang-jian-wen-ti/you-xi-cuo-wu.md)
- [功能说明](gong-neng/README.md)

反馈时请附客户端版本、游戏版本、Retail/PTR 分支、SD/HD/DE 画质和完整错误截图。
