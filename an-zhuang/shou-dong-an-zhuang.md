---
description: 识别资源层级并把完整包放入正确的游戏分支
---

# 手动安装

优先使用[常规安装](chang-gui-an-zhuang.md)。手动安装适合不能运行客户端或需要检查资源层级的情况。

## 解压与目录层级

退出游戏并备份目标分支中已有的自定义资源，再解压完整包。A/B 包需要两份资源都到位。

找到包含 `units`、`terrainart`、`replaceabletextures` 等资源目录的那一层，将其中内容放入所选游戏分支：

```text
Warcraft III/
  _retail_/                 # Retail；PTR 使用 _ptr_
    x86_64/
      Warcraft III.exe
    units/
    terrainart/
    replaceabletextures/
    environment/
    shaders/
```

如果 ZIP 外面还有 `QMF3.5` 或 `_retail_` 包装层，只复制其内部资源，不再把这一层嵌入已有的 `_retail_`。

以下层级会导致游戏读不到资源：

```text
Warcraft III/_retail_/_retail_/units/
Warcraft III/_retail_/QMF3.5/units/
```

你若安装到 PTR，把资源放在 `_ptr_` 中，并使用 PTR 的本地文件设置。

## 允许游戏读取本地资源

新版客户端会在界面启动后尝试开启 Windows 或 macOS 的本地文件读取设置。若不用客户端，可在 Windows 当前用户下执行对应分支的命令。

Retail：

```powershell
reg.exe add "HKCU\Software\Blizzard Entertainment\Warcraft III" /v "Allow Local Files" /t REG_DWORD /d 1 /f
```

PTR：

```powershell
reg.exe add "HKCU\Software\Blizzard Entertainment\Warcraft III Public Test" /v "Allow Local Files" /t REG_DWORD /d 1 /f
```

这些命令只修改所选游戏在当前 Windows 用户下的本地文件读取设置。Mac 命令见[Mac 安装](mac-an-zhuang.md)。

## 手动安装后

默认完整包的资源不一定对应你之前在客户端选过的 DE、原版地形、树木或光照配置。需要客户端管理这些设置时，重新打开客户端并确认版本、画质和 MOD 开关；新版客户端安装入口也支持选择已解压的完整资源文件夹。

如果游戏缺模型或贴图，请先检查 A/B 是否齐全、资源层级和当前分支。不要只凭“游戏能打开”判断完整包已装好。
