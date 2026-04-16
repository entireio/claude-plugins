# Entire Plugin for Claude Code

> [!WARNING]
> **This repository is deprecated.**
>
> Development has moved to [**entireio/skills**](https://github.com/entireio/skills). Please use that repository for the latest versions, installation instructions, and new features. This repo is no longer maintained and will not receive updates.

---

Tools for understanding code intent by tracing changes back to original session transcripts.

## Installation

In Claude Code, run:

```bash
/plugin marketplace add https://github.com/entireio/claude-plugins
/plugin install entire
```

## Local Development

Load the plugin without installing using the `--plugin-dir` flag:

```bash
claude --plugin-dir ./plugins/entire
```

## Commands

### /entire:explain

Explains the intent behind source code by finding original session transcripts.

**Usage:**

In Claude Code, use `/entire:explain` with a function, file, or line of code to understand why it exists.

**Examples:**

- Explain a function: `/entire:explain handleUserLogin`
- Explain a file: `/entire:explain src/auth/middleware.ts`
- Explain a line: `/entire:explain src/utils.ts:42`

**How it works:**

1. Uses `git blame` or `git log` to identify the commit that introduced the code
2. Uses `entire explain --commit COMMIT_SHA` to read the session transcripts

## Requirements

- [Claude Code](https://claude.com/claude-code) CLI
- [Entire CLI](https://entire.dev) installed and configured
