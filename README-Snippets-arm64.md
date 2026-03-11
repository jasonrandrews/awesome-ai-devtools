# AI-Powered Snippet Generators — Arm Linux (arm64/aarch64) Support

This document lists all snippet generators from the [Awesome AI-Powered Developer Tools](README.md#snippet-generators) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Snippet Generator | Description | Arm Linux Support (arm64/aarch64) |
|-------------------|-------------|--------------------------------------|
| [CodePal](https://codepal.ai/) | Web tool for quickly generating or refactoring code | ✅ Web-based (runs in any browser) |
| [AI Code Convert](https://aicodeconvert.com/) | Web tool for translating code between programming languages | ✅ Web-based (runs in any browser) |
| [AI Code Playground](https://aicodeplayground.com/) | Web tool for refactoring and improving code | ✅ Web-based (runs in any browser) |
| [AutoRegex](https://www.autoregex.xyz/) | Produces regular expressions from plain English using GPT-3 | ✅ Web-based (runs in any browser) |
| [unpkg.ai](https://unpkg.ai/) | Open source AI-powered ESM module generation service via URL | ✅ Web-based (runs in any browser) |
| [rule-gen](https://github.com/nedcodes-ok/rule-gen) | CLI tool that generates AI coding rules from your codebase using Gemini | ✅ Yes — Node.js CLI; zero dependencies (architecture-agnostic) |

---

## About Snippet Generators and Arm Linux

All snippet generators in this list are either **web-based platforms** or **Node.js CLI tools**. None require architecture-specific native binaries.

### Web-Based Tools (Accessible from Any Browser on Arm Linux)

CodePal, AI Code Convert, AI Code Playground, AutoRegex, and unpkg.ai are all entirely web-based. They require no local installation and work from any browser on any architecture including arm64 Linux.

### CLI Tool on Arm Linux

- **[rule-gen](https://github.com/nedcodes-ok/rule-gen)** — Node.js CLI tool with zero dependencies. Feeds your source files into Google Gemini's context window to produce project-specific AI coding rules for Cursor, Claude Code, Copilot, and Windsurf. Install via npx or npm — runs on any architecture with Node.js:
  ```bash
  npx rule-gen
  ```
