# Customization Guide

## Color Values

This theme uses a restrained neutral palette. The core colors are shared across both variants:

### Dark Theme

| Token | Hex | Usage |
|---|---|---|
| `#0a0a0a` | near-black | Editor background, inactive tabs |
| `#171717` | dark gray | Panels, sidebars, title bar |
| `#262626` | medium gray | Active selection, badges, buttons |
| `#fafafa` | off-white | Primary text, active foregrounds |
| `#a1a1a1` | muted gray | Secondary text, line numbers |
| `#ff6467` | red | Keywords, errors, deleted |
| `#facc15` | yellow | Numbers, classes, warnings |
| `#60a5fa` | blue | Functions, methods, links |
| `#a3e635` | green | Strings, inserted, attributes |

### Light Theme

| Token | Hex | Usage |
|---|---|---|
| `#ffffff` | white | Editor background |
| `#fafafa` | off-white | Panels, sidebars |
| `#f5f5f5` | light gray | Active selection, badges |
| `#0a0a0a` | near-black | Primary text |
| `#737373` | muted gray | Secondary text, line numbers |
| `#dc2626` | red | Keywords, errors, deleted |
| `#ca8a04` | yellow | Numbers, classes, warnings |
| `#2563eb` | blue | Functions, methods, links |
| `#4d7c0f` | green | Strings, inserted, attributes |

## Workbench Colors

Workbench colors control the VS Code UI chrome. They are defined under the `"colors"` key in the theme JSON.

### Key Sections

- **Activity Bar**: `activityBar.*`
- **Sidebar / Panel**: `sideBar.*`, `panel.*`
- **Editor Chrome**: `editor.*`, `editorGutter.*`, `editorLineNumber.*`
- **Tabs**: `tab.*`
- **Status Bar**: `statusBar.*`
- **Title Bar**: `titleBar.*`
- **Inputs & Dropdowns**: `input.*`, `dropdown.*`
- **Lists & Trees**: `list.*`, `tree.*`
- **Notifications**: `notifications.*`
- **Scrollbars**: `scrollbarSlider.*`

## Token Colors

Token colors define syntax highlighting. They are defined under the `"tokenColors"` key using TextMate scope selectors.

### Common Scopes

| Scope | Element |
|---|---|
| `comment` | Comments |
| `keyword` | `if`, `return`, `import` |
| `string` | String literals |
| `constant.numeric` | Numbers |
| `entity.name.function` | Function names |
| `entity.name.type.class` | Class names |
| `variable` | Variables |
| `storage.type` | `const`, `let`, `var` |

## Semantic Token Colors

Semantic tokens provide richer highlighting based on language server information. Defined under `"semanticTokenColors"`.

| Token | Element |
|---|---|
| `function` | Function calls |
| `method` | Method calls |
| `class` | Class references |
| `type` | Type references |
| `parameter` | Function parameters |
| `variable.readonly` | `const` variables |
| `variable.readWrite` | Mutable variables |
| `property.declaration` | Object property declarations |

## Adding a New Language

1. Open a file in that language
2. Use **Developer: Inspect Editor Tokens and Scopes** to identify scopes
3. Add a new entry in `"tokenColors"` matching the scope(s)
4. The change applies immediately in the Extension Development Host

## Adding Custom Workbench Colors

Add new entries under `"colors"` in the theme JSON. Use the color IDs from the [VS Code Theme Color Reference](https://code.visualstudio.com/api/references/theme-color).

```json
{
  "colors": {
    "myCustomColor": "#ff0000"
  }
}
```
