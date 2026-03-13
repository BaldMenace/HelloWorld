# CLAUDE.md

This file provides guidance for AI assistants working with the HelloWorld repository.

## Project Overview

A minimal "Hello World" demonstration project originally written for the Raspberry Pi (RasPi). It greets the user and prompts for their name, then prints a personalised welcome message.

## Repository Structure

```
HelloWorld/
├── CLAUDE.md        # This file — AI assistant guidance
├── README.md        # Project title
└── helloworld.py    # Main (and only) Python script
```

## Language and Runtime

- **Language**: Python 2 (uses `print` statement and `raw_input`)
- The script is **not compatible with Python 3** as-is. Key differences:
  - `print "..."` is a statement in Python 2; Python 3 requires `print(...)`
  - `raw_input()` does not exist in Python 3; the equivalent is `input()`
- The shebang line (`#!/usr/bin/env python`) targets whichever `python` binary is on the PATH, which is typically Python 2 on legacy Raspberry Pi images.

## Development Workflow

### Branching convention
- The default branch is `master`.
- AI-generated changes must be developed on a branch prefixed with `claude/` (e.g. `claude/add-claude-documentation-IAP1M`).
- Never push directly to `master` without explicit permission.

### Making changes
1. Ensure you are on the correct feature branch before editing.
2. Commit with clear, descriptive messages that explain *why* the change was made.
3. Push with tracking: `git push -u origin <branch-name>`.

### Running the script
```bash
python helloworld.py      # Python 2
# or, if porting to Python 3:
python3 helloworld.py
```

No dependencies beyond the Python standard library are required.

## Key Conventions

- **Simplicity first** — this is an intentionally minimal project; avoid over-engineering.
- **Preserve original intent** — the script is a teaching/demo tool; keep changes focused and readable.
- **Python 2 compatibility** — unless explicitly asked to port to Python 3, keep the existing Python 2 syntax intact.
- **No external dependencies** — do not introduce packages or build tooling unless explicitly requested.

## Git History Summary

| Commit | Message |
|--------|---------|
| `fda58a9` | Adding Python example source |
| `d0ca85f` | Initial commit |
