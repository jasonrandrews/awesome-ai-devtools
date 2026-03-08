# AI-Powered PR Agents — Arm Linux (arm64/aarch64) Support

This document lists all PR agents from the [Awesome AI-Powered Developer Tools](README.md#pr-agents) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| PR Agent | Description | Arm Linux Support (arm64/aarch64) |
|----------|-------------|--------------------------------------|
| [Greptile](https://greptile.com/code-review-bot) | AI bot that reviews PRs with full codebase context | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Macroscope](https://macroscope.com/code-review) | AI-powered code review using AST graph representation | ✅ Web-based / GitHub integration (cloud-hosted) |
| [EntelligenceAI](https://entelligence.ai/pr) | AI powered code reviews for GitHub and GitLab | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Sweep](https://github.com/sweepai/sweep) | AI junior dev that generates, tests, and reviews PRs from issues | ✅ GitHub integration; Python self-hostable |
| [Codegen](https://www.codegen.com/) | GPT-4 based PR agent for enterprise codebases | ✅ Web-based (cloud-hosted) |
| [Code Review GPT](https://github.com/mattzcarey/code-review-gpt) | Open source tool for reviewing PRs | ✅ Node.js CLI / GitHub Action (architecture-agnostic) |
| [Qodo PR Agent](https://github.com/qodo-ai/pr-agent) | Open source automated code review tool | ✅ Python pip / Docker / GitHub Action |
| [Nova](https://www.trynova.ai/) | CI bot that adds summaries and tests to new PRs | ✅ Web-based / CI integration (cloud-hosted) |
| [CodeRabbit](https://coderabbit.ai/) | Customizable CI for PR summaries and code suggestions | ✅ Web-based / CI integration (cloud-hosted) |
| [SwePT](https://github.com/keerthanpg/SwePT) | Open source PR generator written in Python | ✅ Pure Python (architecture-agnostic) |
| [Duckie](https://duckie.ai/) | Web-based chat assistant for modifying GitHub repositories | ✅ Web-based (runs in any browser) |
| [PR Explainer Bot](https://pr-explainer-bot.web.app/) | GitHub integration that adds explanatory text to new PRs | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Goast](https://goast.ai/) | Hosted tool that ingests error logs and suggests fixes | ✅ Web-based (cloud-hosted) |
| [Corgea](https://corgea.com/) | GitHub integration that finds and fixes vulnerable code | ✅ Web-based / GitHub integration (cloud-hosted) |
| [vx.dev](https://github.com/Yuyz0112/vx.dev) | GitHub integration for UI generation with shadcn/lucide/nivo support | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Pixee](https://pixee.ai) | Finds security issues and creates merge-ready fix PRs | ✅ Web-based / GitHub integration (cloud-hosted) |
| [CodeAnt AI](https://www.codeant.ai/) | Automatically creates PRs to fix code issues | ✅ Web-based (cloud-hosted) |
| [What The Diff](https://whatthediff.ai/) | AI-powered app that writes descriptive PR diff comments | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Trag](https://usetrag.com/) | AI-powered code reviews with pre-defined patterns | ✅ Web-based (cloud-hosted) |
| [CodeReviewBot](https://codereviewbot.ai/) | AI-powered code reviews for GitHub | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Callstack.ai Code Reviewer](https://callstack.ai/code-reviewer) | AI-powered PR reviewer for GitHub | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Matter AI](https://matterai.dev) | Open Source AI Code Reviewer for GitHub | ✅ Web-based / GitHub Action (cloud-hosted) |
| [Gito](https://github.com/Nayjest/Gito) | AI code reviewer for any LLM locally or in GitHub Actions | ✅ Python CLI / GitHub Action (architecture-agnostic) |
| [Baz](https://baz.co) | AI Code Reviewer tailored to team guidelines | ✅ Web-based / GitHub integration (cloud-hosted) |
| [Revieko](https://synqra.tech/revieko/) | Architecture drift radar for PRs with structural risk scoring | ✅ Web-based / CI integration (cloud-hosted) |

---

## About PR Agents and Arm Linux

All PR agents in this list operate as **cloud-hosted services**, **GitHub integrations**, or **language-neutral CLI tools** (Python, Node.js). None require architecture-specific native binaries on the developer's machine.

### Why All PR Agents Are Arm64 Compatible

- **GitHub integrations and bots** — Run entirely in the cloud; developers configure them via `.yml` files or web dashboards. No local binary is installed.
- **CI/CD integrations** — Run inside GitHub Actions, GitLab CI, or similar platforms. The CI runner architecture does not affect these tools since the analysis happens server-side.
- **Python CLI tools** — Pure Python packages (`pip install`) are architecture-agnostic.
- **Node.js CLI tools** — npm packages with no native modules run on any architecture with Node.js.
- **Web dashboards** — Accessible from any browser on any OS and architecture.

### Tools That Can Be Self-Hosted on Arm Linux

- **[Qodo PR Agent](https://github.com/qodo-ai/pr-agent)** — The most fully-featured self-hostable option. Install via pip (`pip install pr-agent`, pure Python), Docker (the `codiumai/pr-agent` Docker image), or as a GitHub Action. The Python package is architecture-agnostic and works on arm64 Linux.

- **[Code Review GPT](https://github.com/mattzcarey/code-review-gpt)** — Open source Node.js/TypeScript tool. Available as a GitHub Action, GitLab CI job, or local CLI (`npm install -g code-review-gpt`). No native Node.js add-ons; runs on arm64 Linux.

- **[SwePT](https://github.com/keerthanpg/SwePT)** — 150-line open source Python PR generator. Pure Python; install via `pip install` or run directly. Works on any architecture.

- **[Gito](https://github.com/Nayjest/Gito)** — Python CLI tool and GitHub Actions workflow. Pure Python; compatible with any LLM (local or cloud). Works on arm64 Linux.
