# Contributing to WastedTextEditor

> [!WARNING]
> 🧪 **This repository is an experiment.** It is developed and managed entirely by LLM agents and is **not recommended for production use**. Contributions are welcome, but expect an unconventional (and imperfect) development process.

Thanks for your interest! WastedTextEditor is unusual: its day-to-day development — planning, coding, reviewing, and merging — is performed by LLM agents. Both **humans** and **AI agents** can contribute, under the same mechanics but slightly different rules.

## Ground rules

- **No direct pushes to `main`.** All changes go through pull requests.
- **Every PR needs at least one review** before it can be merged. Never merge your own PR.
- **One logical change per PR.** Small, focused, reviewable.
- **The repo is the memory.** Decisions, plans, and discussions live in issues, PRs, and committed docs — not in private channels.
- **Be respectful.** Review code and ideas, not people (or models).

## For human contributors

### 1. Start with an issue

Open an issue for bugs, feature proposals, documentation problems, or questions. Significant features should be discussed before you invest time in a large PR.

### 2. Branch and commit

- Branch from `main` using a descriptive name: `feat/…`, `fix/…`, `docs/…`, `chore/…`.
- Follow [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`.
- Keep commits small and self-explanatory.

### 3. Open a pull request

- Link the related issue (e.g., `Closes #42`).
- Describe **what** changed and **why** — the reasoning matters more than the diff.
- Include or update tests where applicable, and note how the change was verified on each supported platform (Windows, Linux, macOS) if you can.

### 4. Respond to review

A reviewer (an LLM agent or a human) will review your PR. Address feedback by pushing new commits. Reviews may request changes; that's normal, not a rejection.

## For LLM agents

Read [AGENTS.md](AGENTS.md) before doing anything else. It defines the project context, the three roles (**Planner**, **Coder**, **Reviewer**), and the operating rules. Use the same branch, commit, and PR mechanics as human contributors.

## Review standards

Reviewers check for, in rough priority order:

1. **Correctness** — does it work, and is it tested?
2. **Security** — see below.
3. **Cross-platform behavior** — Windows, Linux, and macOS must all keep working.
4. **Performance** — the editor must stay fast and efficient.
5. **Consistency** — with existing code, docs, and recorded decisions.

## Security expectations

The **plugin permission system** is the project's core security boundary:

- Plugins run sandboxed and are trusted by default for nothing.
- Network access, file access, folder access, and other sensitive resources require an **explicit, per-plugin grant from the user**.

Pull requests that weaken this model — broadening default permissions, bypassing the sandbox, or adding silent access to sensitive resources — will be rejected.

## Style

There is no human-imposed style guide; the LLM agents establish conventions as the project grows. When in doubt, follow the existing code and keep your change consistent with its surroundings.

## License

By contributing to this repository, you agree that your contributions will be licensed under the [MIT License](LICENSE.md), the same as the rest of the project.
