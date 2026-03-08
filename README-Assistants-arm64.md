# AI Coding Assistants (IDE Extensions) — Arm Linux (arm64/aarch64) Support

This document covers tools from the [Awesome AI-Powered Developer Tools](README.md#ide-extensions) **Assistants › IDE extensions** section that include **self-hosted server components**. Pure IDE extensions (VS Code / JetBrains bundles) are architecture-agnostic JavaScript and always work on arm64; this file focuses on the compiled server-side binaries.

## Summary Table

| Tool | Extension Platforms | Self-Hosted Server — Arm Linux Support (arm64/aarch64) |
|------|--------------------|---------------------------------------------------------|
| [Tabby](https://tabbyml.github.io/tabby/) | VS Code, Vim, JetBrains | ⚠️ macOS arm64 ✅; Linux arm64 ❌ (no linux/aarch64 binary or Docker image) |
| [Refact AI](https://refact.ai/) | VS Code, JetBrains | ✅ `refact-lsp` binary: Linux arm64 ✅ & macOS arm64 ✅; self-hosting server Docker ❌ (linux/amd64 only) |
| [CodeComplete](https://codecomplete.ai/) | VS Code, JetBrains | ❓ Unknown — proprietary enterprise product; no public binaries or images found |

---

## Tool Details

### 1. Tabby — ⚠️ macOS arm64 ✅; Linux arm64 ❌

**Website:** https://tabbyml.github.io/tabby/  
**GitHub:** [TabbyML/tabby](https://github.com/TabbyML/tabby)  
**Type:** Self-hosted Rust server + VS Code / Vim / JetBrains extensions  
**Latest release:** v0.32.0

Tabby is an open-source, self-hosted code completion server. The IDE extensions are architecture-agnostic. The server binary is a Rust application compiled for specific targets.

#### Server binary release assets (v0.32.0)

| Asset | Platform | arm64? |
|-------|---------|--------|
| `tabby_aarch64-apple-darwin.tar.gz` | macOS Apple Silicon | ✅ |
| `tabby_x86_64-manylinux_2_28.tar.gz` | Linux x86_64 | ❌ |
| `tabby_x86_64-manylinux_2_28-cuda123.tar.gz` | Linux x86_64 + CUDA | ❌ |
| `tabby_x86_64-manylinux_2_28-vulkan.tar.gz` | Linux x86_64 + Vulkan | ❌ |
| `tabby_x86_64-windows-msvc-*.zip` | Windows x86_64 | ❌ |

**No `aarch64-unknown-linux-gnu` binary is published.**

#### Docker image

The Docker workflow ([`.github/workflows/docker.yml`](https://github.com/TabbyML/tabby/blob/main/.github/workflows/docker.yml)) builds on `buildjet-2vcpu-ubuntu-2204` (x86_64) with no `platforms:` multi-arch directive. Docker Hub confirms only `linux/amd64` is present in the `tabbyml/tabby:latest` manifest.

#### Summary

| Deployment | arm64 Linux Support |
|------------|---------------------|
| macOS arm64 binary | ✅ Official release |
| Linux arm64 binary | ❌ Not available |
| Docker (`tabbyml/tabby`) | ❌ `linux/amd64` only |
| VS Code extension | ✅ Architecture-agnostic |

**Workaround:** To run the Tabby server on Linux arm64, you must compile from source:
```bash
git clone --recurse-submodules https://github.com/TabbyML/tabby
cd tabby
cargo build --release --package tabby
```
Rust's cross-compilation toolchain (`cross`) can build `aarch64-unknown-linux-gnu` targets; however, llama.cpp integration requires additional configuration.

---

### 2. Refact AI — ✅ `refact-lsp` Linux arm64 binary available; server Docker ❌

**Website:** https://refact.ai/  
**GitHub:** [smallcloudai/refact](https://github.com/smallcloudai/refact)  
**Type:** Self-hosted Rust agent engine (`refact-lsp`) + optional Python inference server + VS Code / JetBrains extensions

Refact AI has two distinct self-hosted components:

#### Component A: `refact-lsp` agent engine (Rust binary)

The agent engine CI release workflow ([`.github/workflows/agent_engine_release.yml`](https://github.com/smallcloudai/refact/blob/main/.github/workflows/agent_engine_release.yml)) builds for these targets:

| Target | Platform | arm64? |
|--------|---------|--------|
| `x86_64-pc-windows-msvc` | Windows x86_64 | ❌ |
| `aarch64-pc-windows-msvc` | Windows arm64 | ✅ |
| `x86_64-unknown-linux-gnu` | Linux x86_64 | ❌ |
| **`aarch64-unknown-linux-gnu`** | **Linux arm64** | ✅ via `cross-rs` |
| `x86_64-apple-darwin` | macOS Intel | ❌ |
| **`aarch64-apple-darwin`** | **macOS Apple Silicon** | ✅ |

Linux arm64 is built using [`cross-rs`](https://github.com/cross-rs/cross) for `aarch64-unknown-linux-gnu`. A Python wheel (`manylinux2014_aarch64`) and a release ZIP (`dist-aarch64-unknown-linux-gnu.zip`) are both published to GitHub Releases.

#### Component B: Refact self-hosting inference server (Docker)

The server release workflow ([`.github/workflows/server_release.yml`](https://github.com/smallcloudai/refact/blob/main/.github/workflows/server_release.yml)) builds the Docker image with:
```yaml
platforms: |
  linux/amd64
```
The `smallcloud/refact_self_hosting` Docker image is **linux/amd64 only**. No arm64 Docker image is published.

#### Summary

| Deployment | arm64 Linux Support |
|------------|---------------------|
| `refact-lsp` Linux arm64 binary | ✅ Official release (`aarch64-unknown-linux-gnu`) |
| `refact-lsp` Python wheel (aarch64) | ✅ `manylinux2014_aarch64` wheel on PyPI |
| macOS arm64 binary | ✅ Official release (`aarch64-apple-darwin`) |
| Self-hosting Docker (`smallcloud/refact_self_hosting`) | ❌ `linux/amd64` only |
| VS Code / JetBrains extension | ✅ Architecture-agnostic |

**Note:** If you only need the **agent/LSP functionality** (code completion, chat, agent actions), the `refact-lsp` binary supports arm64 Linux. If you need to run Refact's **local inference server** (to serve open-source models locally), the Docker image does not support arm64 and you would need to build from source.

---

### 3. CodeComplete — ❓ Unknown

**Website:** https://codecomplete.ai/ (currently unreachable)  
**Type:** Self-hosted enterprise code completion server + VS Code / JetBrains extensions

CodeComplete is a proprietary enterprise product. No public GitHub repository, Docker Hub images, PyPI packages, or npm packages were found at the time of research. The website was unreachable.

Without public artifacts, arm64 Linux support cannot be verified. Contact the vendor directly to determine whether a Linux arm64 deployment is available.
