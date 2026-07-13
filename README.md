<div align="center">

# `AP0110` Agent

**A coding agent that runs in your terminal.**

Describe a task in plain language. It reads the repository, makes the change
across the files that matter, runs your checks, and reports back what it did.

<!-- TODO: drop in a demo GIF or screenshot -->

</div>

---

`AP0110` Agent works a task end to end inside a real git repository. It plans
before it edits, traces the actual flow through the code it touches, runs the
build and tests, and iterates from the output rather than guessing. Three things
it is built to do well:

- **Ship changes.** Multi-file refactors, new features, bug fixes, and the tests
  that cover them, all through natural language.
- **Explain code.** Answer questions about how a codebase works without
  touching a line.
- **Handle the loop.** Run the build, tests, linter, and formatter, read the
  output, and keep going until the checks pass.

## Install

<!-- TODO: replace with the real install commands and runtime requirement -->

```bash
# one line
<curl one-liner>

# or a package manager
<package-manager install>
```

## Quickstart

From inside a git repository:

```bash
ap0110 "add input validation to the signup handler and cover it with a test"
```

The agent edits your **working tree**. It stages and changes files but does not
commit or push. You review the diff and commit yourself.

## What it does

- Reads before it writes, then makes the smallest change that holds.
- Edits across every file a change touches, not one file in isolation.
- Runs your tools and iterates from the real output.
- Reports what changed, what it skipped, and why, so a reviewer can follow it.

## How it works

Every run is one loop: **understand** the files the task touches, **plan** the
smallest change, **act** across the files involved, **verify** with the
project's own build and tests, then **report**. Roles and steps stay
operator-visible; actions that reach outside the repository ask first.

## Configuration

Per-project behavior lives in an `AGENTS.md` at the repository root. The agent
reads it at the start of every run and treats it as binding: build, test, and
lint commands, plus house conventions and anything it should never touch.

## Links

<!-- TODO: fill in real destinations -->

- Documentation: `<docs url>`
- Repositories: [github.com/AP0110-AI](https://github.com/AP0110-AI)

---

<div align="center">

An in-house agent from `AP0110`.

</div> 
