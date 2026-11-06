# Theme — Agent Guide

## Project Overview

Theme is a VS Code color theme extension with Dark and Light variants. It uses a restrained neutral palette with semantic token highlighting for modern language server support.

## Quick Commands

```bash
# Launch extension dev host (within VS Code)
# Press F5

# Package extension
npx @vscode/vsce package

# Publish extension
npx @vscode/vsce publish
```

## Key Files

| File | Purpose |
|---|---|
| `themes/dark-theme.json` | Dark theme color + token definitions (~967 lines) |
| `themes/light-theme.json` | Light theme color + token definitions (~967 lines) |
| `package.json` | Extension manifest, contributes themes |
| `icon.png` | Marketplace icon |
| `banner.png` | README banner |

## Architecture

- **Workbench colors** (`"colors"`): Controls VS Code UI chrome (sidebar, tabs, status bar, etc.)
- **Token colors** (`"tokenColors"`): TextMate scope-based syntax highlighting
- **Semantic token colors** (`"semanticTokenColors"`): Language server-driven highlighting (overrides token colors when available)

Both theme files share the same structure and scope definitions, differing only in color values and the `"type"` field (`"dark"` vs `"light"`).

## Conventions

- Use hexagonal color values (e.g. `#fafafa`)
- Alpha transparency via 2-char suffix (e.g. `#ffffff1a`)
- Theme labels match theme file names: `"Dark"` and `"Light"`
- Keep token color scopes consistent across both themes
- Follow existing color palette — do not introduce hues outside the established neutral set

## Testing

- Press `F5` in VS Code to launch Extension Development Host
- Changes to theme files apply immediately
- Use **Developer: Inspect Editor Tokens and Scopes** to verify token scopes

## Documentation

- `docs/EXTENSION_QUICKSTART.md` — Development setup and testing
- `docs/CUSTOMIZATION.md` — Color palette reference and customization guide
- `docs/PUBLISHING.md` — Packaging and publishing workflow
