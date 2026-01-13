# CLAUDE.md - AI Assistant Guide for My_First_Repo

This document provides comprehensive guidance for AI assistants working with this repository. It covers the codebase structure, development workflows, conventions, and best practices.

## Repository Overview

**Repository Name:** My_First_Repo
**Repository Type:** Learning/Tutorial Repository
**Primary Purpose:** Introductory Git and GitHub workflow practice
**Current State:** Minimal structure with basic documentation

### Purpose and Context

This repository serves as a foundational learning environment for Git and GitHub workflows. It's designed to be simple and approachable, making it ideal for:
- Learning basic Git operations (commit, branch, merge, pull request)
- Practicing GitHub collaboration workflows
- Understanding version control fundamentals
- Testing AI-assisted development workflows

## Repository Structure

```
My_First_Repo/
├── .gitattributes          # Git line ending configuration
├── README.md               # Basic repository description
└── CLAUDE.md              # This file - AI assistant guide
```

### Key Files

#### .gitattributes
- Configures automatic LF (Line Feed) normalization for text files
- Ensures consistent line endings across different operating systems
- Content: `* text=auto`

#### README.md
- Simple repository description
- Contains minimal documentation: "BTW this is a way to get help"
- Should be expanded as the repository grows

## Git Workflow and Branch Strategy

### Branch Structure

**Main Branch:**
- Not explicitly shown in current configuration
- Serves as the stable base branch
- All feature branches should branch from and merge back to main

**Feature Branches:**
- Named descriptively based on the feature or change
- Examples: `Branch-1`, `claude/add-claude-documentation-dWFVl`
- Claude-specific branches follow the pattern: `claude/<feature-description>-<session-id>`

**Current Working Branch:**
- `claude/add-claude-documentation-dWFVl`
- All AI assistant development should occur on this branch

### Development Workflow

1. **Branch Creation**
   - Create feature branches from main
   - Use descriptive names that indicate the purpose
   - Claude branches must start with `claude/` prefix

2. **Making Changes**
   - Work on the feature branch
   - Commit changes with clear, descriptive messages
   - Keep commits atomic and focused

3. **Integration**
   - Use Pull Requests to merge changes
   - Review changes before merging
   - Merge to main branch after approval

4. **Push Strategy**
   - Always use: `git push -u origin <branch-name>`
   - Branch names must start with `claude/` and end with session ID
   - Retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s) if network errors occur

### Git History

The repository shows a clean history with:
- Initial commit establishing the repository
- Feature branch (Branch-1) with changes
- Merge via Pull Request #1
- Clear commit messages describing changes

## Conventions and Best Practices

### Commit Message Guidelines

- Use clear, descriptive commit messages
- Examples from history:
  - "Create README.md"
  - "Update .gitattributes"
  - "Change 1" (could be more descriptive)
- Prefer imperative mood: "Add feature" not "Added feature"
- Keep the first line under 72 characters

### File Conventions

1. **Line Endings**
   - Auto LF normalization is enabled
   - Git handles line ending conversions automatically
   - No need to manually manage line endings

2. **File Naming**
   - Use descriptive names
   - Follow standard conventions (README.md, CLAUDE.md)
   - Use uppercase for special documentation files

3. **Documentation**
   - Keep documentation simple and accessible
   - Update README.md as features are added
   - Maintain CLAUDE.md for AI assistant guidance

### Code Style and Quality

Since this is a minimal repository with no code files yet:
- Follow language-specific style guides when adding code
- Keep code simple and readable
- Add comments for complex logic
- Maintain consistency with existing patterns

## AI Assistant Specific Guidelines

### Working with This Repository

1. **Always Check Current State**
   - Run `git status` before making changes
   - Verify you're on the correct branch
   - Review recent commits to understand context

2. **Branch Management**
   - Develop on `claude/add-claude-documentation-dWFVl` branch
   - Never push to branches without `claude/` prefix unless explicitly authorized
   - Ensure branch name ends with matching session ID

3. **Making Changes**
   - Read existing files before suggesting modifications
   - Keep changes focused and minimal
   - Avoid over-engineering
   - Don't add unnecessary features or refactoring

4. **Committing Work**
   - Only commit when explicitly requested
   - Use clear, descriptive commit messages
   - Stage relevant files only
   - Verify changes with `git status` after committing

5. **Push Operations**
   - Use `git push -u origin claude/add-claude-documentation-dWFVl`
   - Implement retry logic for network failures
   - Confirm successful push

### Common Operations

```bash
# Check current status
git status

# View recent commits
git log --oneline -10

# View all branches
git branch -a

# Stage changes
git add <file>

# Commit changes
git commit -m "Descriptive message"

# Push to remote
git push -u origin claude/add-claude-documentation-dWFVl

# Fetch updates
git fetch origin claude/add-claude-documentation-dWFVl
```

### What to Avoid

1. **Don't:**
   - Create files unnecessarily
   - Add features not requested
   - Refactor code without explicit request
   - Push to wrong branches
   - Use force push without explicit permission
   - Skip Git hooks
   - Commit sensitive information (.env files, credentials)

2. **Don't Assume:**
   - Read files before modifying them
   - Verify branch before committing
   - Check git status before and after operations
   - Confirm understanding of requirements before implementing

## Repository Growth Guidelines

As this repository evolves, consider:

1. **Adding Structure**
   - Create `src/` for source code
   - Create `docs/` for additional documentation
   - Create `tests/` for test files
   - Add `.gitignore` for language-specific ignores

2. **Documentation Enhancement**
   - Expand README.md with usage instructions
   - Add contributing guidelines (CONTRIBUTING.md)
   - Add license file if needed
   - Document any setup requirements

3. **Workflow Improvements**
   - Establish CI/CD pipelines
   - Add automated testing
   - Implement code review processes
   - Define branch protection rules

## Pull Request Process

When creating pull requests:

1. **Preparation**
   - Ensure all changes are committed
   - Review git diff to understand all changes
   - Write comprehensive PR description

2. **PR Content**
   - Title: Clear, concise description
   - Body: Include:
     - Summary of changes (1-3 bullet points)
     - Test plan with checklist
     - Any relevant context

3. **Creating PR**
   ```bash
   gh pr create --title "Title" --body "$(cat <<'EOF'
   ## Summary
   - Change 1
   - Change 2

   ## Test plan
   - [ ] Test item 1
   - [ ] Test item 2
   EOF
   )"
   ```

## Troubleshooting

### Common Issues

1. **Push Failures (403 Error)**
   - Verify branch name starts with `claude/`
   - Verify branch name ends with session ID
   - Check authentication

2. **Merge Conflicts**
   - Fetch latest changes from main
   - Resolve conflicts manually
   - Test after resolution

3. **Network Errors**
   - Retry with exponential backoff
   - Check internet connectivity
   - Verify remote URL

## Additional Resources

- **Getting Help:** Use `/help` command in Claude Code CLI
- **Feedback:** Report issues at https://github.com/anthropics/claude-code/issues
- **Git Documentation:** https://git-scm.com/doc
- **GitHub Guides:** https://guides.github.com/

## Changelog

### 2026-01-13
- Created initial CLAUDE.md documentation
- Documented repository structure and conventions
- Added AI assistant guidelines
- Defined Git workflow and branch strategy

---

**Note:** This document should be updated as the repository evolves. Keep it current with actual practices and conventions used in the codebase.
