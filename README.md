# USCN Agent

**连接你的资源，接入 USCN 智能容量网络。**

[平台首页](https://uscn.si) · [下载安装包](https://github.com/beijingcao/uscn-agent/releases/tag/v41) · [安装与使用](docs/INSTALL.md) · [English](README.en.md)

> 本仓库只发布 USCN Agent 的安装包和使用说明，不公开 Agent 实现源码或 USCN 平台服务端源码。

## USCN 是什么？

**USCN — Unified Superintelligence Compute Network**  
**One Network. Every Intelligence.**

[uscn.si](https://uscn.si) 是连接 AI 模型与计算资源供需双方的统一平台，围绕三类市场组织服务：

| 市场 | 功能与用途 |
| --- | --- |
| **交易市场** | 汇集卖家提供的模型订阅额度及 API 资源，展示支持模型、订阅级别、额度、价格、供给状态与卖家信息。 |
| **平台套餐** | 提供平台组织的模型访问套餐，方便买家按模型和使用周期选择。 |
| **GPU 算力** | 提供 GPU 资源登记、设备核验、审核及租赁管理入口。 |

买家可以浏览资源、查看价格与状态，并在符合交易条件时购买或开通使用；卖家可以接入资源、设置销售条件、提交审核和管理供给。同一普通账号可以切换买家与卖家工作台，管理员使用独立后台处理审核与平台配置。

资源是否能够购买、交付或调用，以平台当时显示的审核、连接、额度和执行资格为准；展示在目录中不等于所有能力均已完成验收。

## USCN Agent 有什么作用？

USCN Agent 是安装在**卖家供给电脑**上的连接助手，负责把供给设备与 USCN 平台关联起来：

- **连接平台账号与设备**：通过浏览器确认设备归属，建立供给设备与对应资源的关联。
- **完成厂商授权**：引导你在模型厂商的官方网站登录和授权，不要求把密码或 Token 发送给工作人员。
- **读取账号与额度**：当前 Mac 版本支持 ChatGPT 接入及 Codex 服务范围内的账号、订阅类型、模型目录与额度窗口信息。
- **持续同步状态**：运行期间按约每分钟同步额度，配合设备连接状态，让资源页面显示已用比例、可用比例、窗口时长和重置时间。
- **进入销售设置**：完成连接和数据同步后，按页面引导返回平台设置价格与销售窗口、提交审核。

本机供给需要保持电脑在线和 Agent 运行。设备离线、授权失效或额度不足时，平台继续按现有规则限制新销售与调用。买家通常不需要安装供给侧 Agent。

**额度范围说明：** 当前读取的是官方 Codex 服务返回的窗口，不代表全部 ChatGPT 网页模型的总额度，也不自动证明第三方收费共享获得厂商许可。缺失或失效的数据不会被当作可用额度。

## 下载当前版本

| 项目 | 当前发布内容 |
| --- | --- |
| 应用 | **USCN Agent 41.app** |
| 系统 | **macOS 13 或更新版本** |
| 架构 | **Apple Silicon 与 Intel 通用包** |
| 安装包 | [uscn-agent.zip](https://github.com/beijingcao/uscn-agent/releases/download/v41/uscn-agent.zip) |
| 校验文件 | [uscn-agent.zip.sha256](https://github.com/beijingcao/uscn-agent/releases/download/v41/uscn-agent.zip.sha256) |
| 平台入口 | `https://uscn.si` |

当前 GitHub 安装包与 USCN 网站提供的 Agent 41 公网包一致。应用显示版本为 41，内部程序版本为 `0.41.0-dev.1`。此包尚未完成 Apple Developer ID 签名和公证；macOS 可能阻止直接打开，不能保证无额外确认的安装体验。具体处理见[安装说明](docs/INSTALL.md)。

### 开始使用

1. 下载并解压 `uscn-agent.zip`，打开 **USCN Agent 41.app**。
2. 按浏览器引导登录 USCN，确认这台供给电脑关联的平台账号。
3. 在厂商官网完成登录和授权；官方页面可能要求选择账号、工作区或确认同意。
4. 等待账号、模型和额度同步，返回 USCN 的资源销售设置页面继续。

本机助手页面通常为 `http://127.0.0.1:18777/`，它运行在供给电脑上；它不是 USCN 平台的公网地址。额度读取需要受支持且可用的 Codex 登录环境，缺少时按助手提示安装或登录。

## 相关入口

- [USCN 平台](https://uscn.si)
- [USCN 下载中心](https://uscn.si/#/downloads)
- [交易市场](https://uscn.si/#/market)
- [平台套餐](https://uscn.si/#/packages)
- [GPU 资源与安装插件](https://github.com/beijingcao/uscn-gpu-agent) — 与本仓库的模型供给助手是两个不同程序。
- [平台协议与隐私说明](https://uscn.si/#/terms)

## 反馈与发布范围

功能问题可在本仓库提交 Issue；涉及隐私或安全问题请参阅 [SECURITY.md](SECURITY.md)。反馈时只提供版本、系统和不含秘密的状态文字，不要发送密码、API Key、Token、授权回调网址或本机配置文件。

此仓库用于安装包分发与文档维护，不授予 USCN Agent 或平台实现源码的开源许可。第三方组件的许可声明见 [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt)。
