# Publishing Guide

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [VS Code Extension Manager](https://github.com/microsoft/vscode-vsce):
  ```bash
  npm install -g @vscode/vsce
  ```
- A [Visual Studio Marketplace publisher](https://marketplace.visualstudio.com/manage) account

## Packaging

Create a `.vsix` bundle for manual distribution:

```bash
vsce package
```

Output: `fluent-theme-0.0.1.vsix`

## Publishing to Marketplace

### First Time

1. Create a publisher at [marketplace.visualstudio.com/manage](https://marketplace.visualstudio.com/manage)
2. Generate a Personal Access Token
3. Log in:
   ```bash
   vsce login <publisher-name>
   ```

### Publish

```bash
vsce publish
```

### Version Bump

```bash
vsce publish patch  # 0.0.1 -> 0.0.2
vsce publish minor  # 0.0.1 -> 0.1.0
vsce publish major  # 0.0.1 -> 1.0.0
```

## Pre-Release Checklist

- [ ] Version bumped in `package.json`
- [ ] `CHANGELOG.md` updated
- [ ] Both themes load without errors in the Extension Development Host
- [ ] Token scopes render correctly across supported languages
- [ ] Semantic tokens work with relevant language servers
- [ ] UI colors render correctly (tabs, sidebar, status bar, etc.)
- [ ] Icon and banner are up to date

## Resources

- [Publishing Extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
- [Marketplace Documentation](https://code.visualstudio.com/docs/editor/extension-marketplace)
