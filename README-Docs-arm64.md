# AI-Powered Documentation Tools — Arm Linux (arm64/aarch64) Support

This document lists all documentation tools from the [Awesome AI-Powered Developer Tools](README.md#documentation) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Documentation Tool | Description | Arm Linux Support (arm64/aarch64) |
|--------------------|-------------|--------------------------------------|
| [Trelent](https://trelent.net/) | VS Code extension to generate docstrings | ✅ VS Code extension (architecture-agnostic) |
| [DiagramGPT](https://www.eraser.io/diagramgpt) | AI web app that converts code or plain language into diagrams | ✅ Web-based (runs in any browser) |
| [DocuWriter.ai](https://www.docuwriter.ai/) | AI-powered web app to generate Code & API documentation | ✅ Web-based (runs in any browser) |
| [README-AI](https://github.com/eli64s/readme-ai) | Automated README.md file generator powered by LLM APIs | ✅ Yes — pure Python pip package (architecture-agnostic) |
| [Supacodes](https://www.supacodes.com) | AI tool that automates writing and updating code documentation on GitHub | ✅ Web-based / GitHub integration (cloud-hosted) |
| [CodexAtlas](https://codedocumentation.app/) | Automated code and API documentation using AI | ✅ Web-based (runs in any browser) |
| [EkLine](https://ekline.io/) | AI-powered documentation quality checks and style guide enforcement | ✅ Web-based (runs in any browser) |

---

## About Documentation Tools and Arm Linux

All documentation tools in this list are **web-based platforms**, **VS Code extensions**, or **Python pip packages**. None require architecture-specific native binaries on the developer's machine.

### Web-Based (Accessible from Any Browser on Arm Linux)

DiagramGPT, DocuWriter.ai, Supacodes, CodexAtlas, and EkLine are all fully cloud-hosted web applications. They require no local installation and work from any browser on any architecture.

### IDE Extension

- **[Trelent](https://trelent.net/)** — VS Code extension for generating docstrings automatically. Extensions are architecture-agnostic JavaScript bundles and run wherever VS Code runs, including arm64 Linux.

### Python CLI / Library (arm64 Compatible)

- **[README-AI](https://github.com/eli64s/readme-ai)** — Automated README generator using LLM APIs (OpenAI, Anthropic, Google). Distributed on PyPI as a pure Python package. Install and run on arm64 Linux:
  ```bash
  pip install readmeai
  readmeai --repository https://github.com/your/repo --api openai
  ```
