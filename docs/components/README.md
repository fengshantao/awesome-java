---
title: Components Overview
---

# Components Overview

Use this template for each UI component to ensure consistency.

## <ComponentName>

- **Status**: Stable | Experimental | Deprecated
- **Framework**: React | Vue | Web Component
- **Import**:
  - React: `import { <ComponentName> } from '@org/ui'`
  - Vue: `import { <ComponentName> } from '@org/ui-vue'`
  - Web: `<script type="module" src="/components/<component-name>.js"></script>`

### Props / Attributes

| Name | Type | Required | Default | Description |
| ---- | ---- | -------- | ------- | ----------- |
| `propName` | string | no | `""` | What it does |

### Events / Emits

- `onSomething(detail: { ... })` — when something happens

### Slots / Children

- Default slot — content projected inside component

### Accessibility

- Keyboard: tab, enter/space activation
- ARIA: roles, labels

### Theming

- CSS variables: `--component-color`, `--component-padding`

### Examples

```tsx
// React
<ComponentName propName="value">Label</ComponentName>
```

```vue
<!-- Vue -->
<ComponentName prop-name="value">Label</ComponentName>
```

```html
<!-- Web Component -->
<component-name prop-name="value">Label</component-name>
```

### Notes

- Performance caveats, SSR behavior, browser support
