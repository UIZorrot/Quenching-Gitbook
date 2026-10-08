---
description: 获取客户端、选择游戏目录并安装完整 MOD 资源包
---

# 安装

你需要分别下载 **客户端** 和 **完整 MOD 资源包**。客户端的 `resources` 目录属于程序文件，不是供你手动复制到魔兽目录的完整包。

## 选择安装方式

- [常规安装](chang-gui-an-zhuang.md)：在客户端选择游戏目录，再选择 ZIP 或已解压资源文件夹。
- [手动安装](shou-dong-an-zhuang.md)：把资源放入游戏分支目录，并开启本地文件读取。
- [Mac 安装](mac-an-zhuang.md)：使用 Mac 客户端，或在 macOS 下手动安装。
- [客户端与资源包更新](geng-xin.md)：区分两种更新，保留配置与旧便携包。

## 安装前

退出游戏，确认目标磁盘的空闲空间，备份你手动修改的模型、贴图或第三方 MOD。

在首页选择魔兽争霸 III 的安装根目录。客户端会使用该目录下的 `_retail_` 或 `_ptr_` 分支。目录名称两端的下划线需要保留；不要另建一个名叫 `retail` 或 `ptr` 的目录。

例如：

```text
Warcraft III/
  _retail_/
    x86_64/
      Warcraft III.exe
  _ptr_/
    x86_64/
      Warcraft III.exe
```

你只需使用已安装的分支，无需为了安装 MOD 创建另一个游戏分支。
