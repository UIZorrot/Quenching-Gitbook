---
description: macOS 客户端、资源安装和本地文件读取设置
---

# Mac 安装

3.5 系列提供 Electron Mac 客户端，不需要按旧 WPF 教程安装 .NET 或先安装 Windows 虚拟机。

## 打开客户端

从[客户端 Release](https://github.com/UIZorrot/Quenching-Client/releases/tag/3.5)下载 Mac ZIP，解压后打开 `QMClient.app`。当前 `QMC3.5-Mac.zip` 面向 Apple Silicon；Intel Mac 需要 x64 构建，请先查看下载页的架构说明。

Release 中的 Mac 包未做 Apple 公证。如果系统拦截首次打开，在确认文件来自项目下载页后尝试右键选择“打开”。若系统仍阻止启动，请保留完整提示反馈，不要为了运行来源不明的包关闭系统安全保护。

## 安装完整包

1. 在客户端选择 Warcraft III 的安装目录。
2. 确认 Retail 或 PTR 分支已安装。
3. 点击完整包安装入口，选择完整 ZIP、A/B 两个 ZIP，或已解压资源文件夹。
4. 确认 MOD 开关、游戏版本与画质，再启动游戏。

客户端和资源包需要分别下载。手动放置资源时，目录层级与[手动安装](shou-dong-an-zhuang.md)相同。

## 本地文件读取

新版客户端会在启动完成后根据 macOS 设置本地文件读取；注册错误不会阻止客户端打开。若手动安装后 MOD 仍未生效，可在 Terminal 中设置对应分支。

Retail：

```sh
defaults write "com.blizzard.Warcraft III" "Allow Local Files" -int 1
```

PTR：

```sh
defaults write "com.blizzard.Warcraft III Public Test" "Allow Local Files" -int 1
```

检查 Retail 设置：

```sh
defaults read "com.blizzard.Warcraft III" "Allow Local Files"
```

返回 `1` 表示已开启。PTR 查询请使用上面的 PTR 域名。

## 更新客户端

Mac 当前需要手动下载并替换客户端便携包。保留旧 `.app` 供回退，不要把 Windows 的更新文件放进 Mac 包。完整资源包的安装、MOD 更新与客户端替换是不同操作，见[更新说明](geng-xin.md)。
