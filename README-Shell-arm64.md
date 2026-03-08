# AI-Powered Shell Assistants — Arm Linux (arm64/aarch64) Support

This document lists all shell assistants from the [Awesome AI-Powered Developer Tools](README.md#shell-assistants) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Shell Assistant | Description | Arm Linux Support (arm64/aarch64) |
|-----------------|-------------|--------------------------------------|
| [AskCommand](https://www.askcommand.cppexpert.online/) | Web-based tool to generate Unix commands from text using AI | ✅ Web-based (runs in any browser) |
| [Butterfish](https://butterfi.sh) | CLI tool that embeds ChatGPT in your shell | ⚠️ No pre-built Linux binaries; install via `go install` |
| [Shell Whiz](https://github.com/beimzhan/shell-whiz) | Configurable CLI assistant for shell commands and explanations | ✅ Yes — pure Python pip package |
| [GitFluence](https://www.gitfluence.com/) | Web-based AI Git command generator | ✅ Web-based (runs in any browser) |
| [AutoComplete.sh](https://github.com/closedLoop-technologies/autocomplete-sh) | AI-powered TAB completion for any shell command | ✅ Yes — architecture-agnostic shell scripts |
| [code-collator](https://github.com/tawandakembo/code-collator) | CLI tool that collates a codebase into a single markdown file for LLMs | ✅ Yes — pure Python pip package |
| [Warp](https://www.warp.dev/) | AI-powered fast terminal with team knowledge features | ✅ Yes — official arm64 Linux builds (GPU driver required) |
| [TmuxAI](https://tmuxai.dev/) | AI-powered, non-intrusive terminal assistant for tmux | ✅ Yes — official Linux arm64 binary |
| [intelli-shell](https://github.com/lasantosr/intelli-shell) | Command template manager with AI integration and dynamic completions | ✅ Yes — official aarch64 Linux binaries (glibc and musl) |

## Shell Assistants That Support Arm Linux

### Web-Based (Accessible from Any Browser on Arm Linux)

- **[AskCommand](https://www.askcommand.cppexpert.online/)** — Purely web-based; no installation required. Works in any browser on any architecture.

- **[GitFluence](https://www.gitfluence.com/)** — Purely web-based Git command generator; no installation required. Works in any browser on any architecture.

### Native Arm64 Binaries

- **[Warp](https://www.warp.dev/)** — Official arm64 Debian packages are available (e.g., `warp-terminal_*_arm64.deb`) and it is listed in the Arch Linux pacman repository (`warp-terminal`). Warp uses GPU-accelerated rendering via wgpu and requires Vulkan drivers. Some arm64 systems with non-standard GPU drivers (e.g., Panfrost/Mali) may fail to launch. Ensure Mesa Vulkan drivers are installed and your GPU is supported.

- **[TmuxAI](https://tmuxai.dev/)** — Built in Go and distributed via [goreleaser](https://github.com/alvinunreal/tmuxai). Pre-built Linux arm64 binaries (`tmuxai_Linux_arm64.tar.gz`) are available on the [GitHub releases page](https://github.com/alvinunreal/tmuxai/releases). The install script (`curl -fsSL https://get.tmuxai.dev | bash`) auto-detects arm64 and downloads the correct binary. DEB, RPM, and APK packages are also produced for arm64.

- **[intelli-shell](https://github.com/lasantosr/intelli-shell)** — Built in Rust with full cross-compilation support. Releases include both `aarch64-unknown-linux-gnu` (glibc) and `aarch64-unknown-linux-musl` (musl) variants. The install script auto-detects the architecture and libc type:
  ```bash
  curl -sSf https://raw.githubusercontent.com/lasantosr/intelli-shell/main/install.sh | sh
  ```
  Can also be installed via `cargo install intelli-shell`.

### pip Packages (Pure Python — Arm64 Compatible)

- **[Shell Whiz](https://github.com/beimzhan/shell-whiz)** — Pure Python package with no native extensions. Requires Python ≥ 3.9. Install via:
  ```bash
  pip install shell-whiz
  # or
  pipx install shell-whiz
  ```
  Entry point: `sw`

- **[code-collator](https://github.com/tawandakembo/code-collator)** — Pure Python package; only dependency is `Pygments` (also pure Python). Requires Python ≥ 3.6. Install via:
  ```bash
  pip install code-collator
  ```

### Shell Scripts (Architecture-Agnostic)

- **[AutoComplete.sh](https://github.com/closedLoop-technologies/autocomplete-sh)** — Implemented entirely as Bash/Zsh shell scripts; no compiled binaries. Works on any architecture with standard Unix utilities (`jq`, `wget`, `bash-completion`). Install via:
  ```bash
  wget -qO- https://autocomplete.sh/install.sh | bash
  ```

## Shell Assistants With Partial Arm Linux Support

- **[Butterfish](https://butterfi.sh)** — Written in Go, but the `.goreleaser.yml` only configures builds for macOS (darwin). Pre-built Linux binaries (arm64 or x86_64) are not released. Users on Linux arm64 can build from source using the Go toolchain:
  ```bash
  go install github.com/bakks/butterfish/cmd/butterfish@latest
  ```
  This compiles natively for the host architecture and works on arm64 Linux with Go installed.
