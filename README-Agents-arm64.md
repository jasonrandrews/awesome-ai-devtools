# AI Coding Agents — Arm Linux (arm64/aarch64) Support

This document covers tools from the [Awesome AI-Powered Developer Tools](README.md#agents) **Agents** section and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Agent | Type | Arm Linux Support (arm64/aarch64) |
|-------|------|--------------------------------------|
| [Smol Developer](https://github.com/smol-ai/developer) | pip (Python CLI) | ✅ Yes — pure Python pip package |
| [Aider](https://github.com/paul-gauthier/aider) | pip (Python CLI) | ✅ Yes — pure Python pip package |
| [Blinky](https://github.com/seahyinghang8/blinky) | VS Code extension | ✅ Yes — platform-agnostic JS/TS extension |
| [Mentat](https://www.mentat.ai/) | pip (Python CLI) | ⚠️ pip package exists but project appears abandoned |
| [GPT Engineer](https://github.com/AntonOsika/gpt-engineer) | pip (Python CLI) | ✅ Yes — pure Python pip package |
| [GPT Migrate](https://github.com/0xpayne/gpt-migrate) | pip / Docker | ✅ Yes — Python is arm64-compatible; Docker required at runtime |
| [Grit](https://app.grit.io) | Binary CLI + web | ✅ Yes — official `aarch64-unknown-linux-gnu` binary released |
| [DemoGPT](https://github.com/melih-unsal/DemoGPT) | pip (Python) | ✅ Yes — pure Python pip package |
| [DevOpsGPT](https://github.com/kuafuai/DevOpsGPT) | Docker + Python | ⚠️ Likely — Docker image uses `ubuntu:22.04` (multiarch-capable) but no explicit arm64 CI |
| [CodeFlash AI](https://www.codeflash.ai/) | pip (Python CLI/CI) | ✅ Yes — universal `py3-none-any` wheel |
| [Micro Agent](https://www.builder.io/blog/micro-agent) | npm (Node.js CLI) | ✅ Yes — pure JS/TS; all native deps support arm64 |
| [Fine](https://fine.dev/) | Web (SaaS) | ✅ Web-based — runs in any browser |
| [Potpie](https://potpie.ai) | Docker + pip (Python) | ⚠️ Likely — Docker + Python stack; no explicit multi-arch images published |
| [Roundtable MCP Server](https://github.com/askbudi/roundtable) | pip (Python MCP server) | ✅ Yes — pure Python `py3-none-any` wheel |
| [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) | npm (Node.js CLI) | ✅ Yes — Node.js; ships `@img/sharp-linux-arm64` optional dep; Linux arm64 supported |
| [Open Agent](https://github.com/Th0rgal/openagent) | Docker (Rust + Node.js) | ⚠️ Likely — Docker build from source; Dockerfile has explicit arm64 RTK binary path |
| [Agentic Sprint](https://github.com/damienlaine/agentic-sprint) | Claude Code plugin | ✅ Yes — platform-agnostic markdown/config files |
| [VibeBox](https://vibebox.robcholz.com) | Binary (Rust, macOS only) | ❌ No — uses Apple Virtualization Framework; macOS/Apple Silicon only |
| [Leap.new](https://leap.new/) | Web (SaaS) | ✅ Web-based — runs in any browser |
| [Recurse ML](https://recurse.ml) | Web (SaaS) | ✅ Web-based — runs in any browser |
| [Zenable](https://zenable.io/) | Claude Code plugin + MCP | ✅ Yes — platform-agnostic plugin; MCP server is cloud-hosted |
| [Trellis](https://github.com/mindfold-ai/Trellis) | npm (Node.js CLI) | ✅ Yes — pure JS/TS npm package; no native binaries |

---

## Agents That Support Arm Linux

### pip Packages (Pure Python — Arm64 Compatible)

All of the following tools publish a `py3-none-any` wheel to PyPI (or are pure Python with no compiled extensions), making them architecture-agnostic and fully compatible with arm64 Linux.

- **[Smol Developer](https://github.com/smol-ai/developer)** — CLI agent that generates a full repository from a prompt. Distributed on PyPI as `smol-dev` (v0.0.4). Pure Python; dependencies are `openai`, `tenacity`, `agent-protocol`, etc. Install via:
  ```bash
  pip install smol-dev
  ```

- **[Aider](https://github.com/paul-gauthier/aider)** — CLI assistant and agent for making AI-powered commits to existing repositories. Distributed on PyPI as `aider-chat` (v0.86.2 at time of writing) with a `py3-none-any` wheel. Requires Python 3.10–3.12. Install via:
  ```bash
  pip install aider-chat
  ```

- **[GPT Engineer](https://github.com/AntonOsika/gpt-engineer)** — CLI agent that generates a repository from a prompt and asks clarifying questions. Distributed on PyPI as `gpt-engineer` (v0.3.1). Pure Python with no platform restrictions. Install via:
  ```bash
  pip install gpt-engineer
  ```

- **[DemoGPT](https://github.com/melih-unsal/DemoGPT)** — Auto-generates Streamlit applications from natural language prompts using Llama 2 / OpenAI. Distributed on PyPI as `demogpt` (v1.2.7). Requires Python ≥ 3.8. Install via:
  ```bash
  pip install demogpt
  ```

- **[CodeFlash AI](https://www.codeflash.ai/)** — CLI and CI tool for automatically optimizing Python code using AI. Distributed on PyPI as `codeflash` (v0.20.1) with a universal `py3-none-any` wheel, meaning no native binaries and no platform restrictions. Install via:
  ```bash
  pip install codeflash
  ```

### VS Code Extensions (Platform-Agnostic)

- **[Blinky](https://github.com/seahyinghang8/blinky)** — A VS Code debugging agent that identifies and fixes backend errors, inspired by SWE-agent. Implemented entirely in TypeScript/JavaScript and bundled as a VS Code extension. VS Code extensions run in VS Code's built-in Node.js runtime, making them architecture-agnostic. Works on any arm64 Linux machine running VS Code.

### Native Arm64 Binaries

- **[Grit](https://app.grit.io)** — GitHub-integrated agent for automating maintenance tasks such as migrations and code modernization. The open-source [GritQL](https://github.com/getgrit/gritql) CLI is written in Rust and ships official `aarch64-unknown-linux-gnu` binaries in every release. As of `v0.1.0-alpha.1743007075`, the release matrix explicitly includes an ARM64 Linux tarball:

  | Binary | Platform |
  |--------|----------|
  | `grit-aarch64-unknown-linux-gnu.tar.gz` | ARM64 Linux |
  | `grit-x86_64-unknown-linux-gnu.tar.gz` | x86_64 Linux |

  Install via the shell installer (auto-detects architecture):
  ```bash
  curl --proto '=https' --tlsv1.2 -LsSf \
    https://github.com/getgrit/gritql/releases/latest/download/grit-installer.sh | sh
  ```
  Or via npm:
  ```bash
  npm install -g @getgrit/cli
  ```
  The web platform at [app.grit.io](https://app.grit.io) is browser-based and works on any architecture.

### npm Packages (Node.js — Arm64 Compatible)

- **[Micro Agent](https://github.com/BuilderIO/micro-agent)** — An AI agent (by Builder.io) that writes and iteratively fixes code by running tests. Distributed as `@builder.io/micro-agent` on npm (v0.1.5). Written in TypeScript and compiled to JavaScript. Native dependencies (`sharp`, `playwright`) both publish arm64 Linux binaries. Requires Node.js ≥ 18. Install via:
  ```bash
  npm install -g @builder.io/micro-agent
  ```

### Docker-Based (Arm64 Likely Compatible)

- **[GPT Migrate](https://github.com/0xpayne/gpt-migrate)** — CLI agent that migrates a full-stack application from one language/framework to another. The Python tool itself is pure Python and arm64-compatible. However, GPT Migrate uses Docker at runtime to build and test the migrated code in containers, so Docker must be installed and working. Install via:
  ```bash
  git clone https://github.com/0xpayne/gpt-migrate && cd gpt-migrate
  pip install -r requirements.txt
  ```

---

## Agents With Partial Arm Linux Support

- **[DevOpsGPT](https://github.com/kuafuai/DevOpsGPT)** — AI-driven software development automation (requirements → code → CI/CD). The primary distribution is via Docker (`kuafuai/devopsgpt:latest`). The Dockerfile uses `ubuntu:22.04` as the base image, which is a multiarch image supporting arm64, so the container likely runs on arm64 Linux. However, no explicit arm64 build matrix or CI testing for arm64 was found. The web front end is browser-based. Run via:
  ```bash
  docker run -it -v$PWD/workspace:/app/workspace \
    -v$PWD/env.yaml:/app/env.yaml \
    -p8080:8080 -p8081:8081 kuafuai/devopsgpt:latest
  ```

---

## Agents With Unknown or No Active Maintenance

| Agent | Notes |
|-------|-------|
| [Mentat](https://www.mentat.ai/) | The `mentat` pip package (v1.0.19) still exists on PyPI and is pure Python (arm64-compatible), but the GitHub repository (`AbanteAI/mentat`) returns 404 — the project appears to have been abandoned or deleted. The pip package can be installed on arm64 Linux (`pip install mentat`) but the project is effectively unmaintained. |

---

## Additional Agents (Tools 21–31)

### Web-Based (Accessible from Any Browser on Arm Linux)

- **[Fine](https://fine.dev/)** — SaaS AI dev environment with GitHub, Sentry, and Linear integrations. Entirely web-based; no local installation required. Accessible from any browser on any architecture including arm64 Linux.

- **[Leap.new](https://leap.new/)** — Web-based app builder that generates functional apps with real backend services, APIs, and cloud deployment. Entirely browser-based; no local installation required. Works on any architecture.

- **[Recurse ML](https://recurse.ml)** — Web-based tool for finding bugs in AI-generated code. Entirely browser-based; no local installation required. Works on any architecture.

### pip Packages (Pure Python — Arm64 Compatible)

- **[Roundtable MCP Server](https://github.com/askbudi/roundtable)** — Local MCP server that lets a primary AI assistant delegate tasks to specialized sub-agents (Gemini, Claude, Codex, Cursor) in parallel. Distributed on PyPI as `roundtable-ai` with a `py3-none-any` wheel (pure Python). Requires Python ≥ 3.10. Install via:
  ```bash
  pip install roundtable-ai
  roundtable-ai --agents gemini,claude,codex
  ```
  No native binaries; fully arm64-compatible.

### npm Packages (Node.js — Arm64 Compatible)

- **[Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview)** — Anthropic's official agentic coding CLI. Distributed as `@anthropic-ai/claude-code` on npm (no `os`/`cpu` restrictions). Uses Node.js ≥ 18 with a `cli.js` entry point. Optional native dependencies include `@img/sharp-linux-arm64` and `@img/sharp-linuxmusl-arm64`, confirming arm64 Linux is supported. Recommended install method:
  ```bash
  curl -fsSL https://claude.ai/install.sh | bash
  # or via Homebrew (macOS/Linux):
  brew install --cask claude-code
  # or via npm (deprecated but functional):
  npm install -g @anthropic-ai/claude-code
  ```

- **[Trellis](https://github.com/mindfold-ai/Trellis)** — Multi-platform AI coding framework supporting Claude Code, Cursor, OpenCode, Codex, Gemini CLI, and more. Distributed as `@mindfoldhq/trellis` on npm (no `os`/`cpu` restrictions). Pure JavaScript/TypeScript CLI; no native binaries. Requires Node.js. Install via:
  ```bash
  npm install -g @mindfoldhq/trellis@latest
  trellis init -u your-name
  ```

### Claude Code Plugins (Platform-Agnostic)

- **[Agentic Sprint](https://github.com/damienlaine/agentic-sprint)** — Spec-driven, self-iterative multi-agent development plugin for Claude Code. Orchestrates specialized agents (Project Architect, Implementation, Testing) through structured sprint phases. Implemented entirely as markdown/config files (Claude Code plugin format) — no compiled binaries. Platform-agnostic. `agentic-sprint` is part of the `agentic-forge` marketplace collection; install via:
  ```bash
  /plugin marketplace add damienlaine/agentic-forge
  /plugin install sprint
  # or run locally from the cloned repo:
  git clone https://github.com/damienlaine/agentic-sprint.git
  claude --plugin-dir ./agentic-sprint
  ```

- **[Zenable](https://zenable.io/)** — AI guardrails that enforce organizational standards, security policies, and quality requirements in development workflows. Distributed as a Claude Code plugin (`Zenable-io/ai-guardrails`) and pre-commit hook (shell script). The MCP backend is cloud-hosted at `mcp.zenable.app`. No native binaries; fully platform-agnostic. Install via:
  ```bash
  /plugin marketplace add Zenable-io/ai-guardrails
  /plugin install zenable-guardrails@claude-plugins
  ```

### Docker-Based (Arm64 Likely Compatible)

- **[Potpie](https://potpie.ai)** — Open source AI agent platform that parses a codebase into a Neo4j knowledge graph and exposes pre-built agents for Q&A, testing, debugging, and system design. Self-hosted via Docker Compose (FastAPI + PostgreSQL + Neo4j + Redis + Celery). The Python stack (`FastAPI`, `uv`, Python 3.11+) is arm64-compatible, and the base images (`ubuntu`/`python`) support arm64. No pre-built multi-arch Docker images are published to Docker Hub, but users can build from source on arm64. Also has a VS Code extension (`PotpieAI.potpie-vscode-extension`). Clone and run:
  ```bash
  git clone --recurse-submodules https://github.com/potpie-ai/potpie.git
  cd potpie && cp .env.template .env
  # edit .env, then:
  ./scripts/start.sh
  ```

- **[Open Agent / sandboxed.sh](https://github.com/Th0rgal/sandboxed.sh)** — Self-hosted control plane for AI coding agents (Claude Code, OpenCode, Amp) with isolated Linux container workspaces (systemd-nspawn), real-time mission streaming, and a Next.js dashboard. (The original repo `Th0rgal/openagent` has been renamed to `sandboxed.sh`.) The Dockerfile builds a Rust backend + Next.js frontend on `ubuntu:24.04`. The Dockerfile has explicit arm64 support in the RTK binary download step (`aarch64|arm64`). No pre-built multi-arch Docker images confirmed; build from source on arm64. Install via:
  ```bash
  git clone https://github.com/Th0rgal/sandboxed.sh.git
  cd sandboxed.sh && cp .env.example .env
  docker compose up -d
  ```

---

## Agents That Do NOT Support Arm Linux

- **[VibeBox](https://vibebox.robcholz.com)** — Per-project micro-VM sandbox for running coding agents safely. Built in Rust and uses **Apple Virtualization Framework** (`objc2-virtualization` crate) — this is a macOS-only API. The `Cargo.toml` description explicitly states "Ultrafast CLI on Apple Silicon macOS." No Linux support is planned or possible without a full rewrite. Available via `cargo install vibebox` only on macOS (Apple Silicon). **Not available on Linux arm64.**
