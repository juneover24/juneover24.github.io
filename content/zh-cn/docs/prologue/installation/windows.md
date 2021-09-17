---
title: "Windows"
description: "安装核心和 v2rayA"
lead: "v2rayA 的功能依赖于 V2Ray 核心，因此需要安装内核。"
date: 2021-08-31T14:48:45+08:00
lastmod: 2021-08-31T14:48:45+08:00
draft: false
images: []
menu:
  docs:
    parent: "installation"
weight: 15
toc: true
---

{{% notice info %}}
v2rayA 目前不支持 TUN，因此 Windows 之上的透明代理无法启用。安全起见，本 wiki 将以非管理员权限来运行 v2rayA。
{{% /notice %}}

{{% notice info %}}
建议从 scoop 安装 v2ray 核心，这样你可以很容易地获取后续更新。可以通过 [Qv2ray 的 Mochi 仓库](https://github.com/qv2ray/mochi) 安装核心。
{{% /notice %}}

## 下载 v2rayA

从 [GitHub Releases](https://github.com/v2rayA/v2rayA/releases) 或 GitHub Action 下载适用于 Windows 的二进制文件，然后重命名为 `v2raya.exe`（格外注意 Windows 系统下不能丢失扩展名）。

## 下载 V2Ray 核心 / Xray 核心

### 方法一：从 scoop 安装

```pwsh
scoop install v2ray  ## 或者安装 xray 
```

### 方法二：手动下载安装

> 安装 V2Ray：<https://www.v2fly.org/guide/install.html>  
> 安装 Xray：<https://xray.sh/document/install.html>

下载压缩包之后解压即可。

## 运行 v2rayA

假设 v2rayA 与核心都保存到了 D 盘：

```pwsh
Start-Process "D:\v2rayA\v2raya.exe" -Arg "--lite --v2ray-bin 'D:\v2ray\v2ray.exe' "
```

后台运行：

```pwsh
Start-Process "D:\v2rayA\v2raya.exe" -Arg "--lite --v2ray-bin 'D:\v2ray\v2ray.exe' " -WindowStyle Hidden
```