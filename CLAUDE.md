# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Structure

This is a **monorepo** — a single git repository that contains multiple independent projects. Each top-level folder is a separate project.

```
Projects/
├── CLAUDE.md              # This file
├── WHATS_HAPPENING.md     # Plain-language explainer for the user
├── to_learn.md            # User's personal learning list
├── .gitignore             # Files git should ignore
└── <project-folder>/     # Each folder = one project
```

## User Context

The user is a non-developer who interacts entirely through natural language. They do not write code, use the terminal, or understand programming concepts.

**Key rules:**
- Never ask them to run commands, edit files, or do anything technical — just do it
- Explain what you did in simple, non-technical language after completing tasks
- When creating new projects, add a subfolder under this root and keep things self-contained within it
- Update `WHATS_HAPPENING.md` when introducing new concepts or tools

## Repository Management

- **GitHub remote:** https://github.com/tartakovsky2006-ctrl/Projects
- **Branching:** Use `main` branch for everything (no complex branching needed for this setup)
- Commit messages should be simple and descriptive (e.g., "add recipe website project", "fix broken link on homepage")

## Adding a New Project

1. Create a new folder at the root with a descriptive name (e.g., `recipe-website/`)
2. Keep all project files inside that folder
3. If the project has its own dependencies or build steps, document them in a README.md inside that folder
4. The root .gitignore covers common patterns; add a project-specific .gitignore inside the folder if needed
