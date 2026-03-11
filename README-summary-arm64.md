# AI-Powered Developer Tools — Arm Linux (arm64/aarch64) Support Summary

This document provides a comprehensive overview of Arm Linux (arm64/aarch64) support across all categories of AI-powered developer tools from the [Awesome AI-Powered Developer Tools](README.md) collection.

**Last updated:** March 11, 2026

---

## Executive Summary

Out of **209 total AI developer tools** analyzed across 16 categories:

- **188 tools (90%)** have full Arm Linux support
- **13 tools (6%)** have partial Arm Linux support
- **6 tools (3%)** have no Arm Linux support
- **2 tools (1%)** have unknown support status

**Overall Arm Linux compatibility: 96%** (combining full and partial support)

---

## Category Breakdown

| Category | Total Tools | Full Support | Partial Support | No Support | Unknown | Compatibility |
|----------|-------------|--------------|-----------------|------------|---------|---------------|
| IDEs | 17 | 9 (53%) | 2 (12%) | 6 (35%) | 0 | **65%** |
| Git Clients | 4 | 2 (50%) | 0 | 1 (25%) | 1 (25%) | **50%** |
| Assistants | 56 | 51 (91%) | 3 (5%) | 2 (4%) | 0 | **96%** |
| Shell Assistants | 9 | 8 (89%) | 1 (11%) | 0 | 0 | **100%** |
| Agents | 31 | 25 (81%) | 5 (16%) | 1 (3%) | 0 | **97%** |
| PR Agents | 24 | 24 (100%) | 0 | 0 | 0 | **100%** |
| App Generators | 21 | 21 (100%) | 0 | 0 | 0 | **100%** |
| UI Generators | 13 | 13 (100%) | 0 | 0 | 0 | **100%** |
| Snippet Generators | 6 | 6 (100%) | 0 | 0 | 0 | **100%** |
| Documentation | 7 | 7 (100%) | 0 | 0 | 0 | **100%** |
| Observability | 1 | 1 (100%) | 0 | 0 | 0 | **100%** |
| OpenAI Plugins | 2 | 2 (100%) | 0 | 0 | 0 | **100%** |
| Search | 4 | 2 (50%) | 1 (25%) | 0 | 1 (25%) | **75%** |
| Testing | 11 | 9 (82%) | 1 (9%) | 0 | 1 (9%) | **91%** |
| Evaluation | 1 | 1 (100%) | 0 | 0 | 0 | **100%** |
| Resources | 2 | 2 (100%) | 0 | 0 | 0 | **100%** |
| **TOTAL** | **209** | **188 (90%)** | **13 (6%)** | **6 (3%)** | **2 (1%)** | **96%** |

---

## Key Findings

### Categories with Perfect Arm Linux Support (100%)

Nine categories have complete Arm Linux compatibility:

1. **PR Agents** (24 tools) — All operate as cloud services or architecture-neutral CLI tools
2. **App Generators** (21 tools) — Web-based platforms or Node.js applications
3. **UI Generators** (13 tools) — Web-based platforms and IDE extensions
4. **Snippet Generators** (6 tools) — Web-based tools and Node.js CLI
5. **Documentation** (7 tools) — Web platforms, IDE extensions, and Python packages
6. **Observability** (1 tool) — Web-based SaaS platform
7. **OpenAI Plugins** (2 tools) — Cloud-hosted or Python-based
8. **Evaluation** (1 tool) — Node.js CLI package
9. **Resources** (2 tools) — Web-based resources

### Categories with High Arm Linux Support (90%+)

- **Assistants** (96%) — 51 of 56 tools fully supported
- **Agents** (97%) — 25 of 31 tools fully supported
- **Testing** (91%) — 9 of 11 tools fully supported

### Categories with Moderate Arm Linux Support (50-89%)

- **IDEs** (65%) — 9 of 17 tools fully supported; 6 tools have no support
- **Search** (75%) — 2 of 4 tools fully supported; 1 unknown
- **Git Clients** (50%) — 2 of 4 tools fully supported; 1 unknown

---

## Why Most Tools Support Arm Linux

### Web-Based Tools (100% Compatible)

The majority of AI developer tools are **web-based SaaS platforms** or **cloud-hosted services** that require no local installation. These work on any architecture including arm64 Linux:

- All 24 PR agents
- 18 of 21 app generators
- 11 of 13 UI generators
- 14 of 56 assistants
- 5 of 7 documentation tools

### Architecture-Agnostic Packages

Many tools are distributed as **pure Python (pip)** or **pure JavaScript/TypeScript (npm)** packages with no native compiled extensions:

- **Python packages** — Architecture-agnostic wheels (`py3-none-any`) work on any platform
- **Node.js packages** — JavaScript/TypeScript code runs on any architecture with Node.js
- **IDE extensions** — VS Code and JetBrains extensions are JavaScript bundles

Examples:
- 10 agents are pure Python pip packages
- 8 assistants are command-line tools via npm or pip
- 29 assistants are IDE extensions

### Native Arm64 Binaries

Some tools provide **official arm64 Linux binaries**:

- **IDEs:** Cursor, Zed, CodeStory
- **Git Clients:** git-lrc, GitButler
- **Shell Assistants:** Warp, TmuxAI, intelli-shell
- **Assistants:** aloc, promptext, Tokscale, Arctic
- **Agents:** Grit

---

## Tools Without Arm Linux Support

### IDEs (6 tools)

- **Crystal** — Discontinued; x86_64 only
- **PearAI** — x86_64 Linux only
- **Windsurf** — x86_64 Linux only
- **trae** — macOS arm64 only; Linux arm64 pending
- **Nimbalyst** — x86_64 Linux only
- **Parallel Code** — x86_64 Linux only

### Assistants (2 tools)

- **Amazon Q Developer CLI** — x86_64 only (deprecated)
- **Mantra** — macOS only

### Agents (1 tool)

- **VibeBox** — macOS only (uses Apple Virtualization Framework)

### Git Clients (1 tool)

- **AI Git Narrator** — macOS only

---

## Tools With Partial Arm Linux Support

### IDEs (2 tools)

- **Theia IDE** — Docker/web supports arm64; desktop AppImage is x86_64 only
- **Melty** — Source code available; no pre-built arm64 binaries

### Assistants (3 tools)

- **Pieces** — CLI works on arm64; desktop backend (PiecesOS) is x86_64 only
- **Refact AI** — Extensions and LSP work; self-hosted Docker is x86_64 only
- **Tabby** — Extensions work; self-hosted server is x86_64 only on Linux

### Shell Assistants (1 tool)

- **Butterfish** — No pre-built binaries; can build from source with Go

### Agents (5 tools)

- **DevOpsGPT** — Docker-based; likely arm64-compatible but no explicit CI
- **Potpie** — Docker-based; likely arm64-compatible but no multi-arch images
- **Open Agent** — Docker-based; Dockerfile has arm64 awareness
- **Second.dev** — Web-based but appears defunct
- **Mentat** — pip package exists but project abandoned

### Search (1 tool)

- **Bloop** — macOS arm64 supported; Linux arm64 not available; project discontinued

### Testing (1 tool)

- **DiffBlue** — IDE plugins work on arm64; Docker CLI is x86_64 only

---

## Tools With Unknown Support

### Git Clients (1 tool)

- **GitBrain** — Website unreachable; no public artifacts

### Search (1 tool)

- **ContextMCP** — No public repository or artifacts found

---

## Recommendations for Arm Linux Users

### Fully Supported Categories (Use Any Tool)

If you're on Arm Linux, you can confidently use **any tool** from these categories:
- PR Agents
- App Generators
- UI Generators
- Snippet Generators
- Documentation
- Observability
- OpenAI Plugins
- Evaluation
- Resources

### High-Support Categories (Most Tools Work)

For **Assistants**, **Agents**, **Shell Assistants**, and **Testing**, over 90% of tools work on Arm Linux. Check individual tool documentation for specific compatibility.

### Moderate-Support Categories (Check Before Using)

For **IDEs**, **Git Clients**, and **Search** tools, verify Arm Linux support before committing to a tool:

**IDEs with native arm64 binaries:**
- Cursor (recommended)
- Zed (recommended)
- CodeStory (archived but functional)

**IDEs that are web-based (always work):**
- Google Antigravity
- Replit
- Mutable
- UI Pilot
- GitWit
- OneCompiler

**Git Clients with arm64 binaries:**
- git-lrc
- GitButler

### Workarounds for Partial Support

- **Build from source** — Tools like Butterfish and Melty can be compiled on arm64
- **Use Docker with emulation** — Run x86_64 Docker images with `--platform linux/amd64` (requires QEMU)
- **Use web alternatives** — Many desktop-only tools have web-based equivalents

---

## Distribution Methods by Compatibility

### 100% Arm Linux Compatible

- **Web-based SaaS platforms** — No local installation required
- **Pure Python pip packages** — `py3-none-any` wheels
- **Pure Node.js npm packages** — No native add-ons
- **IDE extensions** — VS Code, JetBrains (JavaScript/TypeScript bundles)
- **Browser extensions** — Chrome, Firefox (architecture-agnostic)
- **Shell scripts** — Bash, Zsh (no compiled binaries)

### Often Arm Linux Compatible

- **Docker images** — If published as multi-arch (`linux/arm64` + `linux/amd64`)
- **Go binaries** — If GoReleaser targets `linux/arm64`
- **Rust binaries** — If CI builds for `aarch64-unknown-linux-gnu`
- **Native binaries** — If release workflow includes arm64 Linux

### Rarely Arm Linux Compatible

- **Electron apps** — Most only build for x86_64 Linux
- **Tauri apps** — Most only build for x86_64 Linux
- **Proprietary desktop apps** — Often x86_64 only
- **Platform-specific frameworks** — e.g., Apple Virtualization Framework

---

## Trends and Observations

1. **Web-first architecture dominates** — The shift to web-based and cloud-hosted tools naturally provides universal architecture support

2. **IDE extensions over desktop apps** — Tools distributed as VS Code/JetBrains extensions avoid architecture-specific builds

3. **Python and Node.js ecosystems excel** — Pure Python and Node.js packages are inherently cross-platform

4. **Docker adoption varies** — Some projects publish multi-arch images; others only support x86_64

5. **Native desktop apps lag** — Electron and Tauri apps often lack arm64 Linux builds despite macOS arm64 support

6. **Open source tools more likely to support arm64** — Community contributions and CI/CD automation make multi-arch builds easier

---

## Conclusion

**Arm Linux is well-supported** in the AI developer tools ecosystem, with **96% overall compatibility**. The dominance of web-based platforms, architecture-agnostic scripting languages (Python, Node.js), and IDE extensions ensures that most tools work seamlessly on arm64 Linux.

The main gaps are in **desktop IDEs** and **self-hosted infrastructure tools** (Docker images), where x86_64 remains the primary target. However, even in these categories, viable alternatives exist.

For developers using Arm Linux (including AWS Graviton, Raspberry Pi, and Apple Silicon via Linux VMs), the AI developer tools landscape is mature and production-ready.

---

## High-Impact Tools That Should Add Arm Linux Support

The following tools would have the **highest impact** if they added native Arm Linux support, based on popularity, market adoption, and developer demand:

### Critical Priority (Widely Used IDEs)

1. **[Windsurf](https://windsurf.com)** (formerly Codeium)
   - **Why:** One of the most popular AI IDEs; forked from VSCodium with agentic capabilities
   - **Current status:** x86_64 Linux only
   - **Impact:** High — Large user base; VSCodium already supports arm64, so technical path exists
   - **Workaround:** Use Cursor or web-based alternatives

2. **[Cursor](https://www.cursor.com/)** ✅ **Already supports arm64**
   - **Note:** Cursor is the market leader and already provides arm64 AppImage — excellent reference for other IDEs

3. **[PearAI](https://trypear.ai/)**
   - **Why:** Open source VS Code fork with growing community
   - **Current status:** x86_64 Linux only
   - **Impact:** Medium-High — Open source nature makes community contributions possible
   - **Workaround:** Use Cursor or Continue extension in VS Code

### High Priority (Popular Tools)

4. **[Pieces](https://pieces.app/)** (Partial support)
   - **Why:** Popular on-device copilot for code snippet management
   - **Current status:** CLI works on arm64; PiecesOS backend is x86_64 only
   - **Impact:** High — Desktop functionality blocked on arm64 Linux
   - **Workaround:** CLI-only usage or x86_64 emulation

5. **[Tabby](https://tabbyml.github.io/tabby/)** (Partial support)
   - **Why:** Leading open source, self-hosted code completion assistant
   - **Current status:** Extensions work; self-hosted server is x86_64 Linux only
   - **Impact:** High — Self-hosting on AWS Graviton or Raspberry Pi clusters blocked
   - **Workaround:** Host on x86_64 server; use extensions from arm64 clients

6. **[Refact AI](https://refact.ai/)** (Partial support)
   - **Why:** Open source assistant with codebase-specific fine-tuning
   - **Current status:** Extensions and LSP work; self-hosted Docker is x86_64 only
   - **Impact:** Medium-High — Self-hosting blocked; LSP binary exists for arm64
   - **Workaround:** Use LSP binary; host Docker on x86_64

### Medium Priority (Niche but Growing)

7. **[trae](https://www.trae.ai/)**
   - **Why:** Adaptive AI IDE by ByteDance with unique collaboration features
   - **Current status:** macOS arm64 supported; Linux arm64 is a pending feature request
   - **Impact:** Medium — Growing user base; already has macOS arm64 build
   - **Workaround:** Use on macOS or x86_64 Linux

8. **[Nimbalyst](https://nimbalyst.com)**
   - **Why:** Agent management environment for Claude Code and Codex
   - **Current status:** x86_64 Linux only
   - **Impact:** Medium — Specialized tool for managing multiple AI agents
   - **Workaround:** Use Dorothy or Parallel Code alternatives (also x86_64 only)

9. **[DiffBlue](https://www.diffblue.com/)** (Partial support)
   - **Why:** Enterprise-grade automated unit test generation for Java
   - **Current status:** IDE plugins work; Docker CLI is x86_64 only
   - **Impact:** Medium — Enterprise adoption; CI/CD integration blocked
   - **Workaround:** Use IDE plugin or Docker with emulation

### Lower Priority (Alternatives Exist)

10. **[Bloop](https://bloop.ai/)** (Discontinued)
    - **Why:** Natural language code search (project appears defunct)
    - **Current status:** macOS arm64 only; Linux arm64 never released
    - **Impact:** Low — Project discontinued; website unreachable
    - **Workaround:** Use SeaGOAT or Sourcegraph Cody

11. **[Amazon Q Developer CLI](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html)** (Deprecated)
    - **Why:** AWS's AI coding assistant CLI
    - **Current status:** x86_64 only; deprecated in favor of Kiro CLI
    - **Impact:** Low — Officially deprecated
    - **Workaround:** Use successor tools

12. **[AI Git Narrator](https://github.com/pmusolino/AI-Git-Narrator)**
    - **Why:** AI-powered Git commit message generator
    - **Current status:** macOS only (Swift-based)
    - **Impact:** Low — Many cross-platform alternatives exist
    - **Workaround:** Use gptcomet, git-lrc, or GitButler

---

## Why These Tools Matter for Arm Linux

### Cloud Infrastructure (AWS Graviton, Oracle Ampere)

- **Tabby** and **Refact AI** self-hosted servers would enable cost-effective AI code completion on Graviton instances
- **DiffBlue** Docker CLI would enable CI/CD test generation on arm64 runners
- Self-hosted tools reduce API costs and improve latency

### Edge Computing and Development Boards

- **Pieces** desktop backend would enable offline AI assistance on Raspberry Pi and similar devices
- Lightweight IDEs on arm64 enable development directly on edge hardware

### Apple Silicon Linux VMs

- Developers running Linux VMs on Apple Silicon Macs (via UTM, Parallels, or Asahi Linux) need native arm64 tools
- **Windsurf**, **PearAI**, and **trae** would provide feature parity with macOS versions

### Cost and Performance

- Arm64 cloud instances (AWS Graviton, Azure Ampere) offer 20-40% better price-performance
- Native arm64 tools eliminate emulation overhead (20-50% performance penalty)

---

## Call to Action for Tool Maintainers

If you maintain one of the tools listed above, adding Arm Linux support would:

1. **Expand your addressable market** — AWS Graviton adoption is growing rapidly in enterprise
2. **Improve performance** — Native execution is 20-50% faster than emulation
3. **Enable new use cases** — Edge computing, Raspberry Pi clusters, Apple Silicon Linux VMs
4. **Future-proof your tool** — Arm64 is the fastest-growing server architecture

### Technical Path Forward

- **Electron/Tauri apps:** Add `aarch64-unknown-linux-gnu` to CI build matrix
- **Docker images:** Publish multi-arch manifests with `linux/arm64`
- **Go/Rust binaries:** Add `linux/arm64` to GoReleaser/cross-compilation targets
- **Python packages:** Ensure dependencies have arm64 wheels (most already do)

---

## Related Documents

- [IDEs — Arm Linux Support](README-IDE-arm64.md)
- [Git Clients — Arm Linux Support](README-Git-arm64.md)
- [Assistants — Arm Linux Support](README-Assistants-arm64.md)
- [Shell Assistants — Arm Linux Support](README-Shell-arm64.md)
- [Agents — Arm Linux Support](README-Agents-arm64.md)
- [PR Agents — Arm Linux Support](README-PR-arm64.md)
- [App Generators — Arm Linux Support](README-AppGen-arm64.md)
- [UI Generators — Arm Linux Support](README-UIGen-arm64.md)
- [Snippet Generators — Arm Linux Support](README-Snippets-arm64.md)
- [Documentation — Arm Linux Support](README-Docs-arm64.md)
- [Observability — Arm Linux Support](README-Observability-arm64.md)
- [OpenAI Plugins — Arm Linux Support](README-Plugins-arm64.md)
- [Search — Arm Linux Support](README-Search-arm64.md)
- [Testing — Arm Linux Support](README-Testing-arm64.md)
- [Evaluation — Arm Linux Support](README-Evaluation-arm64.md)
- [Resources — Arm Linux Support](README-Resources-arm64.md)
