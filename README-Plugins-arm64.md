# AI-Powered OpenAI Plugins — Arm Linux (arm64/aarch64) Support

This document lists all OpenAI plugins from the [Awesome AI-Powered Developer Tools](README.md#openai-plugins) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| OpenAI Plugin | Description | Arm Linux Support (arm64/aarch64) |
|---------------|-------------|--------------------------------------|
| [ChatWithGit](https://gitsearch.sdan.io/) | Enables ChatGPT to search GitHub and return relevant repositories | ✅ Web-based / ChatGPT plugin (cloud-hosted) |
| [Code ChatGPT Plugin](https://github.com/kesor/chatgpt-code-plugin) | Open source ChatGPT plugin that provides file directory context | ✅ Yes — Python self-hosted server (arm64-compatible) |

---

## About OpenAI Plugins and Arm Linux

Both plugins in this list are either **cloud-hosted ChatGPT plugins** or **self-hostable Python web servers**. Neither requires architecture-specific native binaries.

### Cloud-Hosted Plugin

- **[ChatWithGit](https://gitsearch.sdan.io/)** — A hosted ChatGPT plugin that searches GitHub via the ChatGPT plugins interface. All processing is server-side and cloud-hosted; no local installation required. Accessible from any browser/ChatGPT session on any architecture.

### Self-Hosted Plugin (arm64 Compatible)

- **[Code ChatGPT Plugin](https://github.com/kesor/chatgpt-code-plugin)** — Open source example of a ChatGPT plugin that serves a local directory of files as context. Implemented as a Python FastAPI server. Install and run on arm64 Linux:
  ```bash
  git clone https://github.com/kesor/chatgpt-code-plugin
  cd chatgpt-code-plugin
  pip install -r requirements.txt
  python main.py
  ```
  Pure Python; no native compiled extensions. Fully arm64-compatible.
