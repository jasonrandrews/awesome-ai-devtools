# AI-Powered Search Tools — Arm Linux (arm64/aarch64) Support

This document covers tools from the [Awesome AI-Powered Developer Tools](README.md#search) **Search** section and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Search Tool | Type | Arm Linux Support (arm64/aarch64) |
|-------------|------|--------------------------------------|
| [Bloop](https://bloop.ai/) | Desktop app (Tauri/Rust; discontinued) | ⚠️ macOS arm64 only — Linux arm64 ❌; project appears defunct |
| [Buildt](https://www.buildt.ai/) | Web (appears defunct) | ✅ Web-based — no local binary |
| [SeaGOAT](https://kantord.github.io/SeaGOAT/latest/) | Python CLI/server | ✅ Yes — `py3-none-any` wheel; `pip install seagoat` |
| [ContextMCP](https://contextmcp.ai) | Self-hosted | ❓ Unknown — no public repository or Docker images found |

---

## Tool Details

### 1. Bloop — ⚠️ macOS arm64 only (Linux arm64 not available; project discontinued)

**Type:** Tauri-based desktop app (Rust + React frontend)  
**GitHub:** [BloopAI/bloop](https://github.com/BloopAI/bloop)  
**Last release:** v0.6.5 (April 2024) — project appears defunct (website `bloop.ai` is unreachable)

**Release assets (v0.6.5):**
| Asset | Architecture |
|-------|-------------|
| `bloop_0.6.5_aarch64.dmg` | ✅ macOS arm64 |
| `bloop_0.6.5_aarch64.app.tar.gz` | ✅ macOS arm64 |
| `bloop_0.6.5_amd64.AppImage` | ❌ Linux x86_64 only |
| `bloop_0.6.5_amd64.deb` | ❌ Linux x86_64 only |
| `bloop_0.6.5_x64-setup.exe` | ❌ Windows x86_64 only |

**Evidence:** The CI release workflow ([`.github/workflows/tauri-release.yml`](https://github.com/BloopAI/bloop/blob/main/.github/workflows/tauri-release.yml)) targets `x86_64-unknown-linux-gnu`, `x86_64-apple-darwin`, and `aarch64-apple-darwin` — no `aarch64-unknown-linux-gnu`. No Linux arm64 binary has ever been released.

**Summary:** macOS arm64 is supported. Linux arm64 is **not supported**. The project has not been updated since April 2024 and the website is unreachable — consider it discontinued.

---

### 2. Buildt — ✅ Web-based (no local binary)

**Type:** Web application  
**Website:** https://www.buildt.ai/ (currently unreachable — project may be defunct)

Buildt was a cloud-hosted natural language repository search tool. There was no local binary, CLI, or self-hosted server component. As a pure web application, it worked in any browser on any architecture — including arm64 Linux.

The website is currently unreachable; the project may have been discontinued.

---

### 3. SeaGOAT — ✅ Yes — pure Python; arm64 compatible

**Type:** Local Python CLI tool and server  
**GitHub:** [kantord/SeaGOAT](https://github.com/kantord/SeaGOAT)  
**PyPI:** [`seagoat`](https://pypi.org/project/seagoat/) v0.54.17  
**Requires Python:** 3.10–3.13

SeaGOAT is a local-first semantic code search tool. It runs a local server (`gt serve`) and a CLI query client (`gt`). Both are pure Python.

**PyPI wheel:** `seagoat-0.54.17-py3-none-any.whl` — the `py3-none-any` tag means the package itself has no compiled C/C++ extensions and is architecture-agnostic.

**Native dependency considerations:** SeaGOAT depends on `chromadb` (vector store) and `fastembed` (embedding models). Both publish pre-built arm64 wheels for Linux on PyPI, so installation completes without requiring a compiler on arm64 Linux.

**Installation on arm64 Linux:**
```bash
pip install seagoat
# Start the server
gt serve
# Query from another terminal
gt "your search query"
```

---

### 4. ContextMCP — ❓ Unknown (no public repository or images found)

**Type:** Self-hosted MCP server for semantic documentation search  
**Website:** https://contextmcp.ai (currently unreachable)

No public GitHub repository, Docker Hub images, or PyPI/npm packages were found for ContextMCP at the time of research. Without public artifacts, arm64 support cannot be verified. Contact the vendor directly to confirm whether a Linux arm64 deployment is available.

---

## Arm Linux Support Summary

**Total search tools analyzed:** 4

**Full Arm Linux support:** 2 search tools (50%)
- 1 web-based tool (Buildt, though appears defunct)
- 1 pure Python pip package (SeaGOAT, architecture-agnostic)

**Partial Arm Linux support:** 1 search tool (25%)
- Bloop (macOS arm64 supported; Linux arm64 not available; project discontinued)

**No Arm Linux support:** 0 search tools (0%)

**Unknown support:** 1 search tool (25%)
- ContextMCP (no public artifacts found)

**Overall Arm Linux compatibility: 75%** (combining full and partial support, excluding unknown tools)
