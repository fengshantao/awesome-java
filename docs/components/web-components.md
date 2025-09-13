---
title: Web Components
---

# Web Components

Document Custom Elements with attributes, properties, methods, and events.

## <ui-button>

- **Registration**: `customElements.define('ui-button', UIButton)`
- **Module**: `@org/ui-wc/ui-button.js`

### Attributes / Properties

| Name | Type | Reflects | Default | Description |
| ---- | ---- | -------- | ------- | ----------- |
| `variant` | `'primary' | 'secondary'` | yes | `primary` | Visual style |
| `disabled` | `boolean` | yes | `false` | Disable interaction |

### Events

- `click` — fired on activation

### Examples

```html
<script type="module" src="/dist/ui-button.js"></script>

<ui-button onclick="alert('Clicked!')">Click me</ui-button>
<ui-button variant="secondary" disabled>Disabled</ui-button>
```

### Accessibility

- Manages focus, ARIA attributes, and keyboard activation.
