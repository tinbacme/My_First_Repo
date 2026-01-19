# CLAUDE.md - AI Assistant Guide

This file provides context and guidelines for AI assistants working with this repository.

## Repository Overview

**Name:** My_First_Repo
**Owner:** tinbacme
**Purpose:** Starter repository (currently in early development)

## Current Structure

```
My_First_Repo/
├── .gitattributes    # Git line ending configuration (LF normalization)
├── README.md         # Project documentation
└── CLAUDE.md         # This file - AI assistant guidelines
```

## Development Workflow

### Branch Strategy

- Main branch contains stable code
- Feature branches should be descriptive (e.g., `feature/add-login`, `fix/typo-readme`)
- Claude-generated branches use format: `claude/<description>-<session-id>`

### Git Conventions

1. **Commit Messages:** Use clear, descriptive messages
   - Start with a verb (Add, Fix, Update, Remove, Refactor)
   - Keep the first line under 72 characters
   - Example: `Add user authentication module`

2. **Line Endings:** This repository uses LF normalization (configured in `.gitattributes`)

### Making Changes

1. Always read existing files before modifying them
2. Keep changes focused and minimal
3. Test changes when applicable
4. Commit with clear messages

## Code Conventions

*Note: As this repository grows, document language-specific conventions here.*

### General Guidelines

- Write clean, readable code
- Follow existing patterns in the codebase
- Add comments only where logic isn't self-evident
- Avoid over-engineering - keep solutions simple

## Key Files

| File | Purpose |
|------|---------|
| `README.md` | Main project documentation |
| `.gitattributes` | Git configuration for line endings |
| `CLAUDE.md` | AI assistant guidelines (this file) |

## Commands

*Add common development commands as the project grows:*

```bash
# Example placeholder commands
# npm install     # Install dependencies
# npm test        # Run tests
# npm run build   # Build project
```

## Important Notes for AI Assistants

1. **Read before writing:** Always read files before making modifications
2. **Minimal changes:** Only make changes that are directly requested
3. **No assumptions:** Ask for clarification when requirements are unclear
4. **Security first:** Never introduce security vulnerabilities
5. **Preserve style:** Match existing code style and conventions

## Project Status

This repository is in its **initial setup phase**. The structure and content will evolve as the project develops.

---

*Last updated: January 2026*
