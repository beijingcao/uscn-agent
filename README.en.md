# USCN Agent

**Connect your capacity to the USCN network.**

[USCN](https://uscn.si) · [Download Agent 41](https://github.com/beijingcao/uscn-agent/releases/tag/v41) · [中文说明](README.md)

This repository distributes installation packages and documentation only. It does not contain the USCN Agent implementation or the USCN platform's server source code.

## The USCN platform

**USCN — Unified Superintelligence Compute Network**  
**One Network. Every Intelligence.**

USCN brings AI and compute supply together through three product areas:

- **Resource marketplace:** model subscription capacity and API resources, with model support, quota, price, seller and availability information.
- **Platform packages:** model access packages organized by the platform.
- **GPU compute:** GPU registration, device verification, review and rental management.

Buyers browse eligible resources and manage access. Sellers connect resources, set sales conditions, submit them for review and manage supply. A regular account can switch between buyer and seller workspaces; administrators use a separate console. Listing a resource does not establish that every purchase or execution capability has been verified.

## What the Agent does

USCN Agent runs on a seller's supply computer. It connects the device to the platform account, guides official provider authorization, reads supported account and quota metadata, and synchronizes the associated resource. It then guides the seller to the platform's sales settings. Buyers normally do not need this supply-side application.

The current Mac release supports ChatGPT connection and quota observations within the Codex service scope. It can display subscription type, available models, usage and remaining percentages, window duration and reset time. It synchronizes approximately once a minute while running. These windows do not represent every ChatGPT web model's quota, nor do they establish permission for third-party commercial sharing.

## Current release

- **Application:** USCN Agent 41.app
- **System:** macOS 13 or newer
- **Architecture:** Apple Silicon and Intel universal package
- **Internal binary version:** `0.41.0-dev.1`
- **Platform:** `https://uscn.si`
- **Package:** [uscn-agent.zip](https://github.com/beijingcao/uscn-agent/releases/download/v41/uscn-agent.zip)
- **Checksum:** [uscn-agent.zip.sha256](https://github.com/beijingcao/uscn-agent/releases/download/v41/uscn-agent.zip.sha256)

This is the same public Agent 41 package provided by the USCN website. Developer ID signing and Apple notarization are not yet available; macOS may require additional confirmation or block opening it.

Extract the archive and open the application. Follow the browser flow to connect your USCN account and complete the provider's official account, workspace and consent steps. The local assistant normally runs at `http://127.0.0.1:18777/`. Supported Codex login may be required for quota synchronization. Keep the Agent running and the computer online for local supply.

Do not post passwords, API keys, tokens, authorization callback URLs or local configuration files in Issues. Report security concerns privately using [SECURITY.md](SECURITY.md).

For GPU server inventory and installation, see the separate [USCN GPU Agent](https://github.com/beijingcao/uscn-gpu-agent).

No open-source license for the USCN Agent or platform implementation is granted by this distribution repository. Third-party component notices are provided in [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt).
