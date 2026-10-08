---
description: 文档仓库、客户端与完整资源包的职责和版本区别
---

# 资源与版本说明

## 项目仓库

| 仓库 | 用途 |
| --- | --- |
| [Quenching-Gitbook](https://github.com/UIZorrot/Quenching-Gitbook) | 使用说明与常见问题 |
| [Quenching-Client](https://github.com/UIZorrot/Quenching-Client) | Electron 客户端与便携下载包 |
| [Quenching-Assets](https://github.com/UIZorrot/Quenching-Assets) | 完整 MOD 资源与资源发布 |

本仓库中的历史 `source files` 和 `shaders` 目录不作为最新安装包的下载入口。它们保留旧资源供参考，玩家请使用客户端与完整包 Release。

## 三种版本

魔兽游戏版本决定兼容配置；淬火 MOD 版本描述资源版本；客户端内部构建版本描述程序构建。三者不必相同。

对外名称为 3.5 的客户端可以有不同内部构建，查看[更新说明](../an-zhuang/geng-xin.md)和发布页，不能只凭首页显示“3.5”判断已包含某个测试修复。

## 资源配置

客户端按游戏版本、画质、分支和设置选择着色器、DNC、皮肤、地形与水面资源。玩家无需手动移动这些配置模板。

配套资源对齐要同时检查表结构、引用路径和对应纹理。透明水的特殊水表、HD 的地形/悬崖表与 3.0 DE 的直接地形替换有不同用途，不应互相代替。

## 维护文档

修改说明时保留现有页面路径和 SUMMARY 导航；新增页面需要加入目录。不要把本地测试包写成已经发布，也不要把玩家自定义资源列为应批量删除的文件。

文档不包含上传身份、签名私钥、玩家本机路径或测试配置。反馈功能错误请附[常见问题](../chang-jian-wen-ti/README.md)中列出的信息。
