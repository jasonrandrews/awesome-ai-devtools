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
