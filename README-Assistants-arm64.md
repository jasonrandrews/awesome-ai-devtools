# AI-Powered Assistants — Arm Linux (arm64/aarch64) Support

This document lists all assistants from the [Awesome AI-Powered Developer Tools](README.md#assistants) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

### Web-based Assistants

| Assistant | Description | Arm Linux Support (arm64/aarch64) |
|-----------|-------------|--------------------------------------|
| [Replit Ghostwriter Chat](https://replit.com/site/ghostwriter) | Assistant with chat, proactive debugging, and autocomplete | ✅ Web-based (runs in any browser) |
| [Unblocked](https://getunblocked.com/) | Augment source code with knowledge from GitHub, Slack, Jira, Confluence | ✅ Web-based (runs in any browser) |
| [Sourcegraph Cody](https://about.sourcegraph.com/cody) | Assistant with chat, refactoring, and unit test generation | ✅ Web app and architecture-agnostic IDE extensions |
| [Magnet](https://www.magnet.run/) | Web-based chatbot with repositories and issues as context | ✅ Web-based (runs in any browser) |
| [Adrenaline](https://useadrenaline.com/) | Web-based chatbot using AI and ASTs to answer codebase questions | ✅ Web-based (runs in any browser) |
| [CodeSquire](https://codesquire.ai/) | Chrome extension for autocomplete in Google Colab, BigQuery, JupyterLab | ✅ Browser extension (architecture-agnostic) |
| [Incognito Pilot](https://github.com/silvanmelchior/IncognitoPilot) | Open source assistant with built-in Python editor and interpreter | ✅ Web-based self-hostable Python app |
| [Onboard](https://www.getonboardai.com) | Chat with an AI about public and private codebases | ✅ Web-based (runs in any browser) |
| [Code to Flow](https://codetoflow.com) | Visualize and understand code with interactive flowcharts | ✅ Web-based (runs in any browser) |
| [Pieces](https://pieces.app/) | On-device copilot for capturing, enriching, and reusing code snippets | ⚠️ CLI pip package works on arm64; PiecesOS desktop backend is Linux x86_64 only |
| [Wren AI](https://getwren.ai/oss) | Open-source SQL AI Agent | ✅ Web-based / self-hostable via Docker |
| [TEXT2SQL.AI](https://www.text2sql.ai/) | AI-powered SQL query builder | ✅ Web-based (runs in any browser) |
| [SQLAI.ai](https://www.sqlai.ai/) | AI SQL generation, fix, explain, and optimize | ✅ Web-based (runs in any browser) |
| [CodeWP](https://codewp.ai/) | AI chat and coding tools for WordPress developers | ✅ Web-based (runs in any browser) |
| [Gru.ai](https://www.gru.ai/) | AI developer for solving technical problems and daily coding tasks | ✅ Web-based (runs in any browser) |

### IDE Extension Assistants

| Assistant | Description | Arm Linux Support (arm64/aarch64) |
|-----------|-------------|--------------------------------------|
| [GitHub Copilot](https://github.com/features/copilot) | VS Code extension with chat, PR generation, and unit test generation | ✅ VS Code extension (architecture-agnostic) |
| [Cline](https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev) | Autonomous coding agent for VS Code | ✅ VS Code extension (architecture-agnostic) |
| [Refact AI](https://refact.ai/) | Open source assistant with chat, completion, and refactoring | ✅ Extensions work on arm64; `refact-lsp` binary has arm64 Linux build; self-hosted Docker is x86_64 only |
| [Continue](https://continue.dev/) | VS Code extension with chat, refactor, and code generation | ✅ VS Code extension (architecture-agnostic) |
| [Blackbox AI](https://www.useblackbox.io/) | VS Code extension with autocomplete and chat | ✅ VS Code extension (architecture-agnostic) |
| [CodeGeeX](https://codegeex.cn/) | Open source assistant with chat, completion, and refactoring | ✅ VS Code extension (architecture-agnostic) |
| [Quack AI](https://www.quackai.com/) | VS Code extension for adhering to project coding guidelines | ✅ VS Code extension (architecture-agnostic) |
| [Tabby](https://tabbyml.github.io/tabby/) | Open source, self-hosted code completion assistant | ✅ VS Code/Vim extensions; self-hosted server: macOS arm64 ✅; Linux arm64 ❌ (x86_64 only) |
| [Tabnine](https://www.tabnine.com/) | Self-hosted code completion with extensions for 15 editors | ✅ IDE extensions (architecture-agnostic); self-hosted deployment depends on configuration |
| [CodeMate](https://www.codemate.ai/) | VS Code extension for debugging and optimizing code | ✅ VS Code extension (architecture-agnostic) |
| [AskCodi](https://www.askcodi.com/) | AI coding assistant for VS Code, JetBrains, and Sublime Text | ✅ IDE extension (architecture-agnostic) |
| [Rubberduck](https://github.com/rubberduck-ai/rubberduck-vscode) | Open source chat assistant for VS Code sidebar | ✅ VS Code extension (architecture-agnostic) |
| [CodeComplete](https://codecomplete.ai/) | Self-hosted enterprise completion assistant | ❓ Unknown — proprietary; no public arm64 artifacts |
| [GoCodeo](https://www.gocodeo.com/) | AI agent for building and deploying full-stack apps in VS Code | ✅ VS Code extension (architecture-agnostic) |
| [JetBrains AI](https://www.jetbrains.com/ai/) | AI assistant in all JetBrains IDEs | ✅ JetBrains plugin (architecture-agnostic) |
| [aiXcoder](https://www.aixcoder.com/en/) | Local or cloud-based assistant with IDE extensions | ✅ IDE extensions (architecture-agnostic) |
| [Sourcery](https://sourcery.ai/) | AI assistant and linter for Python and JS/TS best practices | ✅ IDE extension (architecture-agnostic) |
| [Swimm](https://swimm.io) | Assistant for contextual code understanding and documentation | ✅ VS Code/JetBrains extension (architecture-agnostic) |
| [Supermaven](https://supermaven.com/) | VS Code extension for autocomplete with 300,000-token context | ✅ VS Code extension (architecture-agnostic) |
| [Amazon Q Developer](https://aws.amazon.com/q/developer/) | AI coding assistant for VS Code and IntelliJ IDEA | ✅ IDE extension (architecture-agnostic) |
| [Android Studio Bot](https://developer.android.com/studio/preview/studio-bot) | AI coding assistant integrated in Android Studio | ✅ IDE plugin (architecture-agnostic) |
| [IBM watsonx Code Assistant for Z](https://www.ibm.com/products/watsonx-code-assistant-z) | AI-powered mainframe application modernization | ✅ Cloud-based / IDE extension |
| [EasyCode](https://www.easycode.ai/) | VS Code extension with GPT-4 chat | ✅ VS Code extension (architecture-agnostic) |
| [Kilo Code](https://kilocode.ai) | Open Source AI coding assistant for VS Code | ✅ VS Code extension (architecture-agnostic) |
| [Mysti](https://github.com/DeepMyst/Mysti) | Multi-agent AI coding assistant for VS Code | ✅ VS Code extension (architecture-agnostic) |
| [FlyonUI MCP](https://flyonui.com/mcp) | Tailwind AI Builder MCP for IDEs | ✅ MCP server integration (architecture-agnostic) |
| [Traycer](https://traycer.ai) | Plan-First Coding Assistant in VS Code | ✅ VS Code extension (architecture-agnostic) |
| [shadcn/studio MCP](https://shadcnstudio.com/mcp) | shadcn/ui component builder MCP for IDEs | ✅ MCP server integration (architecture-agnostic) |

### Command-line Assistants

| Assistant | Description | Arm Linux Support (arm64/aarch64) |
|-----------|-------------|--------------------------------------|
| [Amazon Q Developer CLI](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html) | CLI with command completion, translation, and agentic chat | ❌ Linux x86_64 only (also deprecated; succeeded by Kiro CLI) |
| [aloc](https://github.com/modern-tooling/aloc) | AI-augmented lines of code counter built with Go | ✅ Yes — official `linux_arm64.tar.gz` via GoReleaser |
| [talk-codebase](https://github.com/rsaryev/talk-codebase) | CLI chatbot with repository as context | ✅ Yes — pure Python pip package (architecture-agnostic) |
| [gptcomet](https://github.com/belingud/gptcomet) | CLI for generating commit messages and reviewing changes | ✅ Yes — pure Python pip package (architecture-agnostic) |
| [poorcoder](https://github.com/vgrichina/poorcoder) | Bash scripts for AI commit messages and code context | ✅ Yes — plain Bash scripts (no binaries) |
| [Vibe Compiler (vibec)](https://github.com/Strawberry-Computer/vibe-compiler) | Self-compiling tool for LLM-driven code generation | ✅ Yes — npm package (architecture-agnostic) |
| [cmd-ai](https://github.com/BrodaNoel/cmd-ai) | Natural language to executable shell commands | ✅ Yes — npm package (architecture-agnostic) |
| [promptext](https://github.com/1broseidon/promptext) | Smart code context extractor for AI assistants | ✅ Yes — official `Linux_arm64.tar.gz` via GoReleaser |
| [Conduit8](https://github.com/conduit8/conduit8) | CLI registry for managing Claude Code skills | ❓ Unknown — repository not found |
| [Baz CLI](https://github.com/baz-scm/baz-cli) | CLI for AI-assisted code review | ✅ Yes — npm package (architecture-agnostic) |
| [AdaL](https://sylph.ai/) | Self-evolving AI coding agent running locally | ❓ Unknown — website unreachable; no public repository found |
| [Tokscale](https://github.com/junhoyeo/tokscale) | CLI for tracking token usage from AI coding agents | ✅ Yes — explicitly lists Linux aarch64 (glibc and musl) as supported |
| [vsync](https://github.com/nicepkg/vsync) | CLI for syncing AI IDE configs across tools | ✅ Yes — npm package (architecture-agnostic) |
| [rule-porter](https://github.com/nedcodes-ok/rule-porter) | Zero-dependency CLI for converting AI IDE rule files | ✅ Yes — npm package (architecture-agnostic) |
| [Claude Code Open](https://github.com/kill136/claude-code-open) | Open-source AI coding platform with Web IDE and multi-agent system | ✅ Yes — npm package; Docker image also available |
| [Arctic](https://github.com/arctic-cli/interface) | Terminal-first TUI for AI coding plans and APIs | ✅ Yes — install script explicitly supports `linux-arm64` |

### Desktop Assistants

| Assistant | Description | Arm Linux Support (arm64/aarch64) |
|-----------|-------------|--------------------------------------|
| [Memex](https://memex.tech/) | Build anything with natural language on your desktop | ❓ Unknown — website unreachable; no public repository found |
| [Pieces](https://pieces.app/) | AI-enabled desktop app and browser extension for developer productivity | ⚠️ Partial — `pieces-cli` pip package works on arm64; PiecesOS backend is Linux x86_64 only |
| [Mantra](https://mantra.gonewx.com) | Desktop session time machine for Claude Code, Cursor, and Windsurf | ❌ macOS only — explicitly described as "Free for macOS" |

---

## Assistants That Support Arm Linux

### Web-Based (Accessible from Any Browser on Arm Linux)

All web-based assistants work on Arm Linux through any browser. This includes: Replit Ghostwriter Chat, Sourcegraph Cody (web), Magnet, Adrenaline, CodeSquire, Incognito Pilot, Onboard, Code to Flow, Wren AI, TEXT2SQL.AI, SQLAI.ai, CodeWP, and Gru.ai.

### IDE Extensions (Work Wherever the IDE Runs)

All VS Code, JetBrains, and other IDE extensions are architecture-agnostic JavaScript/TypeScript bundles. They work on Arm Linux as long as the host IDE supports arm64 — VS Code has official Linux arm64 support.

### Command-line Tools With Native arm64 Binaries

- **[aloc](https://github.com/modern-tooling/aloc)** — Go binary; GoReleaser targets `linux/arm64`. Download `aloc_*_linux_arm64.tar.gz` from GitHub Releases.
- **[promptext](https://github.com/1broseidon/promptext)** — Go binary; GoReleaser targets `linux/arm64`. Download `promptext_Linux_arm64.tar.gz` from GitHub Releases.
- **[Tokscale](https://github.com/junhoyeo/tokscale)** — Rust binary via npm platform packages. README explicitly lists `Linux aarch64 (glibc) ✅` and `Linux aarch64 (musl) ✅`.
- **[Arctic](https://github.com/arctic-cli/interface)** — Bun-compiled binary; install script detects `aarch64` and downloads `@arctic-cli/arctic-linux-arm64`.

### Command-line via Architecture-Neutral Runtimes (npm/pip)

- `talk-codebase`, `gptcomet` — Python pip (pure Python, no native wheels)
- `poorcoder` — Bash scripts only
- `vibec`, `cmd-ai`, `Baz CLI`, `vsync`, `rule-porter`, `Claude Code Open` — npm/Node.js packages

---

## Assistants With Partial Arm Linux Support

- **[Pieces](https://pieces.app/)** — The `pieces-cli` Python package installs on arm64, but requires **PiecesOS** as a local backend, which is Linux x86_64 only. Full desktop functionality is blocked on arm64 Linux.
- **[Refact AI](https://refact.ai/)** — Extensions are arm64-compatible. The `refact-lsp` binary provides `aarch64-unknown-linux-gnu` builds. However, the self-hosting Docker image (`smallcloud/refact_self_hosting`) is `linux/amd64` only.
- **[Tabby](https://tabbyml.github.io/tabby/)** — Extensions are arm64-compatible. The self-hosted server supports macOS arm64 but **not** Linux arm64; the official Docker image is `linux/amd64` only.

---

## Assistants That Do Not Support Arm Linux

| Assistant | Notes |
|-----------|-------|
| [Amazon Q Developer CLI](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line.html) | Linux release targets x86_64 only; also deprecated |
| [Mantra](https://mantra.gonewx.com) | macOS-only desktop application |
