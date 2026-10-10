<div align="center">

# 👻 GhostInject

**A lightweight Windows DLL injector with a modern dark-themed GUI.**

Supports classic `LoadLibrary` injection and **Manual Mapping** for Chromium-based browsers — without `--no-sandbox`.

<br>

<img src="https://img.shields.io/badge/C%2B%2B-17-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++17">
<img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
<img src="https://img.shields.io/badge/Architecture-x64%20%7C%20x86-6366F1?style=for-the-badge" alt="Arch">

<img src="https://img.shields.io/badge/Injection-LoadLibrary%20%7C%20Manual%20Map-EF4444?style=for-the-badge" alt="Injection">
<img src="https://img.shields.io/badge/Browsers-Chromium%20Family-10B981?style=for-the-badge" alt="Browsers">
<img src="https://img.shields.io/badge/Status-Active-22C55E?style=for-the-badge" alt="Status">

<br><br>

> ⚠️ Built for **authorized security testing**, **defensive research**, and **controlled lab environments**.

</div>

---

## 📸 Screenshots

<div align="center">

### 🖥️ Main Window

<img src="https://i.imgur.com/yoeN99k.png" alt="GhostInject Main Window" width="420">

<br><br>

### 🔍 Process Selection

<img src="https://i.imgur.com/ijbTMel.png" alt="Select Process Dialog" width="520">

</div>

---

## ✦ Overview

**GhostInject** is an advanced DLL injection tool designed for **security researchers**, **penetration testers**, and **reverse engineers**.

It follows a **Loader → Payload** model — the operator selects a target process, chooses a DLL, and injects using either classic or manual-mapping techniques.

The tool automatically detects Chromium-based browsers and switches to **Manual Mapping** to bypass `Renderer Code Integrity (CIG)` and `Arbitrary Code Guard (ACG)` — **without requiring `--no-sandbox` flags**.

---

## ✦ Features

<div align="center">

| | Feature | Description |
|:---:|:---|:---|
| 🖥️ | **Modern Dark GUI** | Custom title bar, flat buttons, smooth hover animations. |
| 🔍 | **Process Picker** | Real-time process list with live search by name or PID. |
| 🧠 | **Auto Mode** | Detects Chromium browsers and selects the correct method. |
| 🔧 | **Classic Injection** | `LoadLibraryA` / `LoadLibraryW` via `CreateRemoteThread`. |
| 🧩 | **Manual Mapping** | Full PE loader — Sections, Relocations, Imports, TLS, DllMain. |
| 🛡️ | **Protected Detection** | Rejects PPL / system processes with a clear message. |
| 🔐 | **String Encryption** | XOR-encrypted strings to reduce static detection. |
| 🕵️ | **Anti-Debug** | Multi-layer debugger detection (PEB, NtGlobalFlag, etc.). |
| 🎯 | **Chromium Ready** | Injects into Chrome, Brave, Edge, Opera, Vivaldi renderers. |
| 📝 | **Live Log** | Detailed log of every injection step. |

</div>

---

## ⚙️ Build Pipeline

```mermaid
flowchart LR
    A[GhostInject.exe] --> B[Select Target Process]
    B --> C[Choose DLL]
    C --> D{Chromium?}
    D -->|Yes| E[Manual Mapping]
    D -->|No| F[LoadLibraryW]
    E --> G[Injection Successful]
    F --> G
    G --> H[Target Process]

    style A fill:#1a1a20,stroke:#a064b4,color:#fff
    style D fill:#1a1a20,stroke:#a064b4,color:#fff
    style G fill:#1a1a20,stroke:#22c55e,color:#fff
    style H fill:#1a1a20,stroke:#5865f2,color:#fff
```
## 📬 Contact

<div align="center">

[![Discord Server](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/5-6)
[![Discord User](https://img.shields.io/badge/Discord-@ghoststeal-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discordapp.com/users/970282290905231390)

</div>
