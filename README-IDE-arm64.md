# AI-Powered IDEs — Arm Linux (arm64/aarch64) Support

This document lists all IDEs from the [Awesome AI-Powered Developer Tools](README.md#ides) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| IDE | Description | Arm Linux Support (arm64/aarch64) |
|-----|-------------|--------------------------------------|
| [Google Antigravity](https://antigravity.google/) | Agent-first IDE with deep browser integration | ✅ Web-based (runs in any browser) |
| [Crystal](https://github.com/stravu/crystal) | Dev environment for parallel Claude Code sessions | ❌ x86_64 Linux only (discontinued) |
| [Cursor](https://www.cursor.com/) | AI IDE forked from VSCodium, uses OpenAI | ✅ Yes — official arm64 AppImage |
| [PearAI](https://trypear.ai/) | Open source VS Code fork with chat and inline generation | ❌ x86_64 Linux only |
| [Melty](https://melty.sh/) | Open source VS Code fork with AI commits | ⚠️ Source code only — no pre-built arm64 binaries |
| [Replit](https://replit.com/) | Web-based IDE with cloud environments and AI agents | ✅ Web-based (runs in any browser) |
| [Mutable](https://github.com/mutableai/monitors4codegen) | Web-based IDE integrated with a chatbot and GitHub | ✅ Web-based (runs in any browser) |
| [CodeStory](https://codestory.ai/) | AI IDE forked from VSCodium with auto commits and PR summaries | ✅ Yes — arm64 Linux binaries available (project archived) |
| [UI Pilot](https://ui-pilot.com/) | Chat-based AI code editor for Material UI forms | ✅ Web-based (runs in any browser) |
| [GitWit](https://gitwit.dev/) | Web-based editor for building ReactJS apps with AI | ✅ Web-based (runs in any browser) |
| [Windsurf](https://windsurf.com) | Agentic AI IDE forked from VSCodium, formerly Codeium | ❌ x86_64 Linux only |
| [Theia IDE](https://theia-ide.org/#theiaide) | Extensible open-source web and desktop IDE with AI features | ⚠️ Docker/web supports arm64; desktop Linux is x86_64 only |
| [OneCompiler](https://onecompiler.com/) | Free AI-powered online compiler for 70+ languages | ✅ Web-based (runs in any browser) |
| [trae](https://www.trae.ai/) | Adaptive AI IDE by ByteDance | ❌ x86_64 Linux only |
| [Zed](https://zed.dev/) | High-performance multiplayer code editor | ✅ Yes — official arm64 tarball |
| [Nimbalyst](https://nimbalyst.com) | Agent management environment for Claude Code and Codex | ❌ x86_64 Linux only |
| [Parallel Code](https://github.com/johannesjo/parallel-code) | Desktop app for running multiple AI coding agents in parallel | ❌ x86_64 Linux only |

## IDEs That Support Arm Linux

### Native Desktop Arm64 Binaries

- **[Cursor](https://www.cursor.com/)** — Provides an official arm64 AppImage (`Cursor-*-aarch64.AppImage`) at `downloads.cursor.com`. Installable via NixOS/nixpkgs on `aarch64-linux`.

- **[Zed](https://zed.dev/)** — Provides an official arm64 tarball (`zed-linux-aarch64.tar.gz`) in its GitHub releases. Installable via the Zed download script or package managers.

- **[CodeStory](https://codestory.ai/)** *(archived)* — The last release (1.96.4.25031) included arm64 Linux packages: `.deb`, `.rpm`, `.tar.gz`, and `.snap`. The project was archived in February 2025.

### Web-Based IDEs (Accessible from Any Browser on Arm Linux)

These IDEs run entirely in the browser and therefore work on Arm Linux without any special binaries:

- **[Google Antigravity](https://antigravity.google/)** — Agent-first IDE orchestrating autonomous AI agents.
- **[Replit](https://replit.com/)** — Full-featured web IDE with cloud environments, code completion, and AI agents.
- **[Mutable](https://github.com/mutableai/monitors4codegen)** — Web-based IDE integrated with a chatbot and GitHub.
- **[UI Pilot](https://ui-pilot.com/)** — Chat-based editor for building Material UI forms.
- **[GitWit](https://gitwit.dev/)** — Web-based editor for building ReactJS applications with AI.
- **[OneCompiler](https://onecompiler.com/)** — Free AI-powered online compiler supporting 70+ languages.

## IDEs With Partial Arm Linux Support

- **[Theia IDE](https://theia-ide.org/#theiaide)** — The Docker/web image is published for `linux/arm64` and works on Arm. However, the downloadable desktop application for Linux is published as an x86_64-only AppImage.

- **[Melty](https://melty.sh/)** — Open source with code available on GitHub, so it can be built from source on Arm Linux. No pre-built arm64 binaries are provided.

## IDEs That Do Not Support Arm Linux

| IDE | Notes |
|-----|-------|
| [Crystal](https://github.com/stravu/crystal) | Linux release assets are `linux-amd64` only; project discontinued (succeeded by Nimbalyst) |
| [PearAI](https://trypear.ai/) | Linux release assets are x86_64 only |
| [Windsurf](https://windsurf.com) | Official downloads and NixOS package only provide `x86_64-linux` |
| [trae](https://www.trae.ai/) | Native arm64 support limited to macOS (Apple Silicon); Linux arm64 is a pending feature request |
| [Nimbalyst](https://nimbalyst.com) | Desktop app (successor to Crystal), x86_64 Linux only |
| [Parallel Code](https://github.com/johannesjo/parallel-code) | Linux release assets are `amd64` only |

---

## Arm Linux Support Summary

**Total IDEs analyzed:** 17

**Full Arm Linux support:** 9 IDEs (53%)
- 3 with native arm64 desktop binaries (Cursor, Zed, CodeStory)
- 6 web-based IDEs accessible from any browser

**Partial Arm Linux support:** 2 IDEs (12%)
- Theia IDE (Docker/web supports arm64; desktop is x86_64 only)
- Melty (source code available; no pre-built arm64 binaries)

**No Arm Linux support:** 6 IDEs (35%)
- Crystal, PearAI, Windsurf, trae, Nimbalyst, Parallel Code

**Overall Arm Linux compatibility: 65%** (combining full and partial support)
