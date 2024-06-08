---
title: 常见问题
project_name: GameLan 联机助手
keywords: "联机助手,游戏联机,联机工具,游戏,联机,组网,局域网,虚拟局域网,LAN,GameLan,MC联机"
credits: "Copyright 2022-2024 NKXingXh. All Rights Reserved."
layout: easy
---

## 软件相关

### 获取更新和服务器信息失败

Tip: 如果你所在地区的运营商存在限制 (例如福建)，则可能无法正常获取更新信息。因为我们的部分服务器位于国外。我们目前正在解决该问题。

如果你并非处于以上地区，请尝试以下步骤。

#### 设置DNS服务器

将 DNS 服务器设置为 223.5.5.5。

[图文设置教程](https://alidns.com/knowledge?type=SETTING_DOCS#user)

### 创建或加入房间后自动离开

### 无可用虚拟网卡

安装虚拟网卡

### 界面文字乱码

![软件文字乱码](/images/gui/1.png)

**解决方法**

![区域设置](/images/solution/1.webp)

### 登录失败，请重启客户端

重启软件后再试。如果问题依旧，说明当前选择的联机服务器处于维护状态。

### MAC或IP地址已被使用

通常是上一次使用该联机服务器后未正常退出导致地址资源未释放。

等待一段时间后重试，或者更换联机服务器。

## 虚拟网卡相关

如果已安装虚拟网卡驱动，但软件仍然提示**无可用虚拟网卡**，请按以下步骤检查。

打开**设备管理器**，查看**网络适配器**中是否有 `TAP-Windows Adapter V9`。

如果设备前显示**感叹号**，请双击查看**设备状态**。

### 驱动签名问题

![驱动签名问题](/images/device/1.webp)

如果显示 **Windows 无法验证此设备所需的驱动程序的数字签名**，请先卸载当前版本。

![卸载TAP-Windows](/images/solution/2.webp)

然后手动安装 `tap-windows-9.21.2.exe` 即可。

### 注册表无用项问题

![注册表无用项问题](/images/device/2.webp)

如果显示 **Windows 仍在设置此设备的类配置**，请使用 **CCleaner** 清理注册表。

清理后重启计算机。

## 网络相关

### NAT 类型

你可以在软件主界面的右下角查看当前的网络状况。

如果显示为<font color="orange">橙色空心圆 ○</font>，则有很大可能是你的路由器设备存在限制。

你可以参考下文的[路由器设置教程](#路由器设置教程)改善。

如果显示为**黑色空心圆 ○**，则无法与**同类用户**建立P2P连接。

如要改善 NAT 类型，你可以尝试在路由器管理页面中进行一些设置。

### 本侧网络连接可能受阻

**Tip: 建议以软件主界面右下角显示的网络状况为准**

说明路由器设备可能不支持 NAT-PMP 或 UPnP。

你可以尝试在路由器管理页面中启用相关选项。

### 路由器设置教程

如果软件右下角显示的网络状况不佳，你可以尝试在路由器后台进行部分设置来改善联机体验。

#### 登录路由器管理

先查看路由器的IP地址

![查看路由器的IP地址](./images/solution/3.webp)

记下该地址，并在浏览器地址栏中输入

![打开路由器管理地址](./images/solution/4.png)

输入管理账号与密码，登录路由器后台。

#### 启用 UPnP

找到标有 `UPnP` 的设置选项，不同厂商的路由器页面可能略有不同。

![打开路由器管理地址](./images/solution/5.png)

将 `UPnP` 功能启用。

[TP-LINK 官方设置教程](https://resource.tp-link.com.cn/pc/docCenter/showDoc?id=1655112527113938)

[华为路由器官方设置教程](https://consumer.huawei.com/cn/support/content/zh-cn00225379/)

#### 设置 DMZ 主机

Tip: 在设置 DMZ 主机前，建议为你的设备设置静态内网IP地址或者在DHCP设置中指定本机的内网IP。

[TP-LINK 官方设置教程](https://security.tp-link.com.cn/service/detail_article_2442.html)

[华为路由器官方设置教程](https://consumer.huawei.com/cn/support/content/zh-cn00225378/)
