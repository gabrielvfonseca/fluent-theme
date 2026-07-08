# Extension Quickstart

## Folder Structure

```
fluent-theme/
├── themes/
│   ├── dark-theme.json    # Dark theme definition
│   └── light-theme.json   # Light theme definition
├── docs/                  # Documentation
├── package.json           # Extension manifest
├── icon.png               # Extension icon
└── banner.png             # README banner
```

## Development

1. Open the project in VS Code
2. Press `F5` to launch the Extension Development Host
3. Open the Command Palette (`Ctrl+K Ctrl+T` or `Cmd+Shift+P`) → **Color Theme** → select **Dark** or **Light**
4. Changes to theme files are automatically applied to the development host

## Testing Token Scopes

1. Open a file with a supported language
2. Run **Developer: Inspect Editor Tokens and Scopes** from the Command Palette
3. Hover over tokens to see their TextMate scopes
4. Use these scopes to add or adjust token color rules in the theme file

## Packaging

```bash
npx @vscode/vsce package
```

This produces a `.vsix` file that can be shared or installed manually.

## Publishing

```bash
npx @vscode/vsce publish
```

Requires a personal access token from the VS Code Marketplace. See [Publishing Extension](https://code.visualstudio.com/api/working-with-extensions/publishing-extension).

## Resources

- [VS Code Color Theme API](https://code.visualstudio.com/api/extension-guides/color-theme)
- [Semantic Highlighting](https://code.visualstudio.com/api/language-extensions/semantic-highlight-guide)
- [TextMate Scopes](https://macromates.com/manual/en/language_grammars)
- [Color Reference](https://code.visualstudio.com/api/references/theme-color)
