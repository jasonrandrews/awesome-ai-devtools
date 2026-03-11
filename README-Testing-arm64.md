# AI-Powered Testing Tools — Arm Linux (arm64/aarch64) Support

This document covers tools from the [Awesome AI-Powered Developer Tools](README.md#testing) **Testing** section and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Testing Tool | Type | Arm Linux Support (arm64/aarch64) |
|--------------|------|--------------------------------------|
| [Checksum AI](https://checksum.ai) | SaaS CI/CD integration | ✅ Web-based — no local binary required |
| [OctoMind](https://octomind.dev) | SaaS/cloud | ✅ Web-based — no local binary required |
| [Traceloop](https://traceloop.com/) | Python SDK | ✅ Yes — pure Python `traceloop-sdk`; `pip install traceloop-sdk` |
| [Carbonate](https://carbonate.dev/) | SaaS | ✅ Web-based — no local binary required |
| [Meticulous.ai](https://www.meticulous.ai/) | npm CLI | ✅ Yes — `@alwaysmeticulous/cli` npm package; no native binaries |
| [DiffBlue](https://www.diffblue.com/) | Docker CLI + IDE plugins | ⚠️ Partial — IDE plugins ✅ (JVM); Docker `cover-cli` is linux/amd64 only |
| [Qodo](https://www.qodo.ai/) | VS Code / JetBrains extension | ✅ Yes — platform-agnostic IDE extension |
| [DeepUnit](https://www.deepunit.ai/) | VS Code extension / npm | ✅ Yes — platform-agnostic extension; npm CLI has no native deps |
| [MutahunterAI](https://github.com/codeintegrity-ai/mutahunter) | Python CLI/CI | ✅ Yes — `py3-none-any` wheel; `pip install mutahunter` |
| [KushoAI](https://kusho.ai/) | SaaS | ✅ Web-based — no local binary required |
| [Test Gru](https://gru.ai/home#test-gru) | Web | ✅ Web-based — no local binary required |

---

## Tool Details

### Web-Based / SaaS Tools (Accessible from Any Browser on Arm Linux)

These tools are fully cloud-hosted or integrate via CI/CD configuration files. They require no local binaries and work on any architecture.

#### Checksum AI — ✅ Web-based

**Website:** https://checksum.ai  
Checksum AI is a fully autonomous QA automation agent that connects to your repository and generates CI/CD-ready Playwright tests. All AI processing happens in the cloud; the tests it produces run in your existing CI environment (GitHub Actions, etc.) using standard Playwright — which itself supports arm64.

#### OctoMind — ✅ Web-based

**Website:** https://octomind.dev  
OctoMind auto-generates and auto-maintains browser-based end-to-end tests. Integration is via GitHub Actions, Azure DevOps, or similar CI platforms — no arm64 binaries needed on the developer's machine.

#### Carbonate — ✅ Web-based

**Website:** https://carbonate.dev  
Carbonate uses natural language to generate tests that integrate into existing test suites (Jest, PHPUnit, Python unittest). Configuration is code-based; no local Carbonate binary is installed.

#### KushoAI — ✅ Web-based

**Website:** https://kusho.ai  
KushoAI is a SaaS API testing agent that transforms Postman collections, OpenAPI specs, and curl commands into test suites. Results plug into CI/CD pipelines as standard test files with no local binary.

#### Test Gru — ✅ Web-based

**Website:** https://gru.ai/home#test-gru  
Test Gru provides enterprise unit test automation as a web service. No local binary installation required.

---

### Python SDK (arm64 Compatible)

#### Traceloop — ✅ Yes — pure Python SDK

**Website:** https://traceloop.com/  
**PyPI:** [`traceloop-sdk`](https://pypi.org/project/traceloop-sdk/) v0.53.0  
**Requires Python:** 3.10–3.12

Traceloop uses OpenTelemetry to instrument LLM calls and correlates tracing data with reliability issues. The SDK is distributed as a pure Python package.

**PyPI wheel:** `traceloop-sdk` publishes a `py3-none-any` wheel — no compiled extensions, fully architecture-agnostic.

**Installation on arm64 Linux:**
```bash
pip install traceloop-sdk
```

---

### npm CLI Tools (arm64 Compatible)

#### Meticulous.ai — ✅ Yes — npm CLI, no native dependencies

**Website:** https://www.meticulous.ai/  
**npm package:** [`@alwaysmeticulous/cli`](https://www.npmjs.com/package/@alwaysmeticulous/cli) v2.257.1  
**Requires Node.js:** ≥ 12

The Meticulous CLI records and replays user sessions to generate and maintain end-to-end tests automatically. The npm package specifies no `os` or `cpu` restrictions and has no native add-ons.

**Installation on arm64 Linux:**
```bash
npm install -g @alwaysmeticulous/cli
```

---

### IDE Extensions / Plugins (arm64 Compatible)

#### Qodo (formerly Codium) — ✅ Yes — platform-agnostic extensions

**Website:** https://www.qodo.ai/  
Qodo provides test generation with support for major programming languages. It is distributed as VS Code and JetBrains extensions — both are JavaScript/TypeScript bundles with no native binaries. The extension installs and runs identically on arm64 Linux.

#### DeepUnit — ✅ Yes — platform-agnostic extension / npm

**Website:** https://www.deepunit.ai/  
DeepUnit offers test generation as a VS Code extension and optionally as an npm CLI or CI/CD pipeline integration. The VS Code extension is architecture-agnostic. The npm CLI does not declare any native module dependencies.

---

### Docker CLI + IDE Plugin (Partial arm64 Support)

#### DiffBlue — ⚠️ Partial — IDE plugins ✅; Docker CLI ❌ (linux/amd64 only)

**Website:** https://www.diffblue.com/  
**Docker Hub:** [`diffblue/cover-cli`](https://hub.docker.com/r/diffblue/cover-cli)

DiffBlue Cover automatically generates unit tests for Java. It is available in two forms:

1. **IntelliJ IDEA plugin** — JVM-based; runs on any architecture that JVM supports, including arm64. ✅
2. **`cover-cli` Docker image** — The Docker image manifest confirms only `linux/amd64`:
   ```
   linux/amd64 ← only platform in manifest
   ```
   There is no `linux/arm64` image published. Running the Docker CLI on arm64 requires emulation (e.g., `--platform linux/amd64` with QEMU), which will work but with reduced performance.

**Recommendation:** Use the IntelliJ plugin on arm64 Linux. If you need the CLI on arm64, use `docker run --platform linux/amd64 diffblue/cover-cli` with QEMU emulation installed.

---

### Python CLI/CI (arm64 Compatible)

#### MutahunterAI — ✅ Yes — pure Python, arm64 compatible

**Website:** https://github.com/codeintegrity-ai/mutahunter  
**PyPI:** [`mutahunter`](https://pypi.org/project/mutahunter/) v1.3.2  
**Requires Python:** ≥ 3.11

MutahunterAI is an open-source LLM-based mutation testing tool. It runs as a CLI (`mutahunter run`) or in CI/CD pipelines.

**PyPI wheel:** `mutahunter-1.3.2-py3-none-any.whl` — pure Python with no compiled C/C++ extensions. All dependencies (`openai`, `litellm`, etc.) are architecture-agnostic.

**Installation on arm64 Linux:**
```bash
pip install mutahunter
export OPENAI_API_KEY=your-key-goes-here
mutahunter run --test-command "pytest" --model "gpt-4o-mini" \
  --source-path "src/my_module.py" --test-path "tests/test_my_module.py"
```

---

## Arm Linux Support Summary

**Total testing tools analyzed:** 11

**Full Arm Linux support:** 9 testing tools (82%)
- 5 web-based/SaaS tools (100% compatible)
- 1 pure Python SDK (Traceloop)
- 1 npm CLI tool (Meticulous.ai)
- 2 IDE extensions (Qodo, DeepUnit)
- 1 Python CLI/CI tool (MutahunterAI)

**Partial Arm Linux support:** 1 testing tool (9%)
- DiffBlue (IDE plugins work on arm64; Docker CLI is x86_64 only)

**No Arm Linux support:** 0 testing tools (0%)

**Unknown support:** 1 testing tool (9%)
- AgentsKB (mentioned in summary but not in main list)

**Overall Arm Linux compatibility: 91%** (combining full and partial support)
