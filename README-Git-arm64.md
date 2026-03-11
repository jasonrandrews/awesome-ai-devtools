# AI-Powered Git Clients — Arm Linux (arm64/aarch64) Support

This document lists all Git clients from the [Awesome AI-Powered Developer Tools](README.md#git-clients) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| Git Client | Description | Arm Linux Support (arm64/aarch64) |
|------------|-------------|--------------------------------------|
| [git-lrc](https://github.com/HexmosTech/git-lrc) | Free, unlimited AI code reviews that run on every commit | ✅ Yes — official linux-arm64 binary via install script |
| [GitBrain](https://gitbrain.dev/) | Git client that simplifies the git workflow; splits code changes and generates commit messages | ❓ Unknown — website unreachable; no public source or release listings found |
| [GitButler](https://gitbutler.com/) | Git client for simultaneous branches on top of your existing workflow | ✅ Yes — official arm64 AppImage and CLI binary |
| [AI Git Narrator](https://github.com/pmusolino/AI-Git-Narrator) | CLI tool that uses AI to automatically generate Git commit messages and PR descriptions | ❌ macOS only — built specifically for macOS using Swift |

## Git Clients That Support Arm Linux

### Native Arm64 Binaries

- **[git-lrc](https://github.com/HexmosTech/git-lrc)** — The install script (`scripts/lrc-install.sh`) explicitly detects `aarch64`/`arm64` architecture and downloads a `linux-arm64` binary from the project's CDN. Installation is handled automatically:
  ```bash
  curl -fsSL https://hexmos.com/lrc-install.sh | bash
  ```

- **[GitButler](https://gitbutler.com/)** — Provides official arm64 Linux builds. The CI publish workflow explicitly includes an `ubuntu-22.04-arm` build matrix entry that produces native `aarch64` artifacts, including:
  - An **arm64 AppImage** (desktop GUI application)
  - A **`but` CLI binary** for `aarch64`, signed and published to the CDN

  Both binaries are available from [https://gitbutler.com/](https://gitbutler.com/). The `but` CLI can also be installed via the installer script at [https://gitbutler.com/cli](https://gitbutler.com/cli).

## Git Clients That Do Not Support Arm Linux

| Git Client | Notes |
|------------|-------|
| [AI Git Narrator](https://github.com/pmusolino/AI-Git-Narrator) | Built specifically for macOS using Swift 6; installed via Homebrew; no Linux binaries (arm64 or x86_64) are provided |

## Git Clients With Unknown Arm Linux Support

| Git Client | Notes |
|------------|-------|
| [GitBrain](https://gitbrain.dev/) | Closed-source desktop application; website was unreachable during research; no GitHub repository or public release listings were found to verify arm64 support |
