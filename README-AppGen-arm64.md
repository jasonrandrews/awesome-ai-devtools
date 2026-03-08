# AI-Powered App Generators — Arm Linux (arm64/aarch64) Support

This document lists all app generators from the [Awesome AI-Powered Developer Tools](README.md#app-generators) collection and indicates whether each one runs natively on Arm Linux (arm64 / aarch64).

## Summary Table

| App Generator | Description | Arm Linux Support (arm64/aarch64) |
|---------------|-------------|--------------------------------------|
| [Pico](https://picoapps.xyz) | End-to-end micro app generator with instant deployment | ✅ Web-based (runs in any browser) |
| [Co.dev](https://www.co.dev/) | AI-powered app development platform for full-stack applications | ✅ Web-based (runs in any browser) |
| [SoftGen](https://softgen.ai/) | AI-powered software generation platform for Web Apps | ✅ Web-based (runs in any browser) |
| [LlamaCoder](https://llamacoder.together.ai/) | Open source code generation model for building applications | ✅ Web-based (runs in any browser) |
| [e2b_Fragments](https://fragments.e2b.dev/) | Platform for AI-powered applications with sandboxed environments | ✅ Web-based (runs in any browser) |
| [Bolt.new](https://bolt.new) | AI-powered web development agent using WebContainers | ✅ Web-based (runs in any browser) |
| [Bolt.diy](https://github.com/stackblitz-labs/bolt.diy) | Open source Bolt.new supporting multiple LLM providers | ✅ Self-hostable Node.js app (arm64-compatible) |
| [Srcbook](https://github.com/srcbookdev/srcbook) | TypeScript-centric app development platform with AI app builder | ✅ Node.js / self-hostable (arm64-compatible) |
| [Capacity](https://capacity.so) | AI-powered full-stack web app development from natural language | ✅ Web-based (runs in any browser) |
| [Lovable](https://lovable.dev/) | AI-powered full-stack app development with GitHub integration | ✅ Web-based (runs in any browser) |
| [Literally anything](https://literallyanything.io) | HTML and JavaScript web app generator | ✅ Web-based (runs in any browser) |
| [GPT Web App Generator](https://magic-app-generator.wasp-lang.dev/) | Generates a full-stack React/Node.js/Prisma/Wasp app | ✅ Web-based (runs in any browser) |
| [Make Real](https://makereal.tldraw.com/) | Online canvas for generating HTML/JavaScript apps | ✅ Web-based (runs in any browser) |
| [Marblism](https://marblism.com) | Generate a SaaS boilerplate from a prompt | ✅ Web-based (runs in any browser) |
| [Glowbom](https://glowbom.com/) | Generate apps with AI and export to multiple platforms | ✅ Web-based (runs in any browser) |
| [Mage](https://usemage.ai/) | Generate full-stack web apps in Wasp, React, Node.js, and Prisma | ✅ Web-based (runs in any browser) |
| [ScrollHub](https://hub.scroll.pub/) | Generate and publish websites using the Scroll programming language | ✅ Web-based (runs in any browser) |
| [Taskade Genesis](https://taskade.com/genesis) | AI platform for building custom agents, workflows, and apps | ✅ Web-based (runs in any browser) |
| [Berrry](https://berrry.app) | Twitter/Reddit post to functional web app generator | ✅ Web-based (runs in any browser) |
| [Blank Space](https://www.blankspace.build/) | Open-source AI app builder; self-hostable alternative to v0/Lovable | ✅ Self-hostable Node.js app (arm64-compatible) |
| [Fastshot](https://fastshot.ai/) | AI-driven no-code platform for building and deploying mobile apps | ✅ Web-based (runs in any browser) |

---

## About App Generators and Arm Linux

All app generators in this list are **web-based platforms** or **self-hostable Node.js applications**. None require architecture-specific native binaries on the developer's machine.

### Why All App Generators Are Arm64 Compatible

- **Web platforms** — Run entirely in the cloud; accessible from any browser on any architecture.
- **Self-hostable Node.js apps** — Tools like Bolt.diy, Srcbook, and Blank Space run as Node.js web servers. Node.js has full arm64 Linux support, so self-hosting on arm64 works without any special configuration.

### Self-Hostable App Generators on Arm Linux

- **[Bolt.diy](https://github.com/stackblitz-labs/bolt.diy)** — Open source version of Bolt.new. Runs as a Node.js/Vite application. Clone the repo and run `pnpm install && pnpm run dev` — fully arm64-compatible.

- **[Srcbook](https://github.com/srcbookdev/srcbook)** — TypeScript notebook and AI app builder. Distributed as an npm package; install via `npx srcbook@latest start`. Node.js-based; fully arm64-compatible.

- **[Blank Space](https://www.blankspace.build/)** — Open source alternative to v0/Lovable/Bolt. Self-hostable Node.js application. Clone and run; fully arm64-compatible.
