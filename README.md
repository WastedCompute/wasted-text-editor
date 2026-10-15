# WastedTextEditor

**A fast, extensible, secure text editor with a TUI and a GUI — designed, built, and managed entirely by LLMs.**

> [!WARNING]
> 🧪 **This project is an experiment.** Every part of WastedTextEditor — feature planning, code writing, code review, PR review, and merging — is performed by LLM agents. The code is **not production-ready** and is **not recommended for production use**. Expect bugs, breaking changes, unfinished features, and design decisions made without human oversight. Use at your own risk.

## What is this?

WastedTextEditor is an experiment by **WastedCompute** asking a single question: **can a complete, useful software product be designed, built, and maintained entirely by LLM agents?**

Human maintainers provided only:

1. The end goal of the project (described below).
2. The initial governance documents: this README, `LICENSE.md`, `CONTRIBUTING.md`, and `AGENTS.md`.

Everything else is decided and executed by LLM agents working under the rules in [AGENTS.md](AGENTS.md). Humans may observe, open issues, and contribute, but the day-to-day development loop — planning, coding, reviewing, merging — is run by agents.

## The end product

The goal is a text editor with the following characteristics:

- **TUI and GUI** — the editor ships with two frontends sharing the same core: a fast terminal interface and a graphical desktop interface.
- **Fast and efficient** — quick startup, responsive editing, and good performance on large files.
- **LSP support** — integration with language servers for completion, go-to-definition, diagnostics, formatting, and refactoring.
- **Syntax highlighting** — accurate, fast highlighting across many languages.
- **Everything is a plugin** — the plugin system is not an add-on; core capabilities (file management, editing commands, LSP integration, highlighting, UI components, …) are all implemented as plugins. Plugins are written in **Lua**.
- **Secure by default** — a capability-based plugin permission system. Plugins cannot access the network, the filesystem, or other sensitive resources unless the user **explicitly grants** permission. No plugin is trusted by default.
- **Cross-platform** — targets Windows, Linux, and macOS.

Everything not listed here is intentionally left undecided. The LLM agents choose the language, architecture, build system, plugin API, UI design, and all other details — and record those decisions in the repository.

## How development works

- **LLM agents** — read [AGENTS.md](AGENTS.md). It defines the three roles (Planner, Coder, Reviewer) and the rules of engagement.
- **Humans** — read [CONTRIBUTING.md](CONTRIBUTING.md). Bug reports, feature proposals, and pull requests are welcome; the same review and merge rules apply to everyone.

## Repository status

**Pre-alpha / experimental.** There is no stable release, no API stability guarantee, and no support commitment. This project exists to explore autonomous LLM-driven development, not to produce a supported product.

## License

Released under the [MIT License](LICENSE.md). By contributing to this repository, you agree your contributions are licensed under the same terms.
