# taxiboatdriver.com - Copilot Instructions

This document provides instructions for GitHub Copilot coding agent when working with the taxiboatdriver.com repository.

## Repository Overview

taxiboatdriver.com is a personal website for Serhii (qizh, `;,;`, taxiboatdriver). The website uses simple Markdown files for content.

## Technology Stack

- **Content**: Markdown
- **Hosting**: GitHub Pages (or similar static site hosting)

## Project Structure

```
taxiboatdriver.com/
├── index.md           # Homepage
├── README.md          # Repository documentation
├── .gitignore         # Git ignore rules
└── .github/
    ├── agents/        # Custom agent configurations
    └── copilot-instructions.md
```

## Code Style and Conventions

### Markdown
- Use standard Markdown syntax
- Keep content simple and minimalistic
- Use proper heading hierarchy
- Ensure links are valid and working

### Documentation
- Keep README.md up to date with major changes
- Document any special configurations or requirements
- Include clear instructions for contributors

## What You Should Do

### For Content Changes
1. **Keep it simple** - follow minimalistic design principles
2. **Review existing content** before making changes
3. **Ensure consistency** across all pages
4. **Test links** to ensure they work properly
5. **Follow Markdown best practices**

### For Documentation
1. Update README.md when adding significant features
2. Keep documentation clear and concise
3. Include examples where helpful

## What You Should NOT Do

### Content
- **DO NOT** remove or modify working content unless absolutely necessary
- **DO NOT** commit secrets or sensitive data
- **DO NOT** make changes to `.github/agents/` directory (these are agent configuration files)

### Build Artifacts
- **DO NOT** commit `.DS_Store` or other system files (covered by `.gitignore`)
- **DO NOT** commit temporary files

## File and Directory Guidelines

### Files to Ignore
As per `.gitignore`:
- `.DS_Store`

### Files to Keep in Source Control
- All Markdown content files
- Configuration files
- Documentation

## Agent-Specific Notes

The repository has a custom agent configured in `.github/agents/taxiboatdriver.agent.md` with specific personality and responsibilities.

**Instruction Priority**: When the custom agent is active:
1. The custom agent's instructions in `.github/agents/taxiboatdriver.agent.md` take precedence
2. This file (`.github/copilot-instructions.md`) provides general repository context and conventions
3. Both sets of instructions are complementary

---

**Last Updated**: 2025-12-03
**Author**: Serhii (qizh, `;,;`, taxiboatdriver)
