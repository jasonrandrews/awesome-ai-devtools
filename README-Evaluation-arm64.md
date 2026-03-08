# AI-Powered Evaluation Tools — Arm Linux (arm64/aarch64) Support

This document lists all evaluation tools from the [Awesome AI-Powered Developer Tools](README.md#evaluation) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Evaluation Tool | Description | Arm Linux Support (arm64/aarch64) |
|-----------------|-------------|--------------------------------------|
| [sniffbench](https://github.com/AnswerLayer/sniffbench) | Benchmark suite for evaluating coding agents | ✅ Yes — Node.js CLI package (architecture-agnostic) |

---

## About Evaluation Tools and Arm Linux

The evaluation tool listed is a **Node.js CLI package** with no native binary dependencies. It runs on any architecture that supports Node.js, including arm64 Linux.

- **[sniffbench](https://github.com/AnswerLayer/sniffbench)** — Benchmark suite for comparing coding agent configurations, tracking metrics, and A/B testing against real issues from your repositories. Published as `sniffbench` on npm (v0.1.1) with no `os` or `cpu` restrictions and no native add-ons. Requires Node.js ≥ 18. Install and run on arm64 Linux:
  ```bash
  npm install -g sniffbench
  sniffbench run
  ```
