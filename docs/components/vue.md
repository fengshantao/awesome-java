---
title: Vue Components
---

# Vue Components

Document Vue 3 components with props, emits, and slots.

## Button

- **Import**: `import { Button } from '@org/ui-vue'`

### Props

| Name | Type | Required | Default | Description |
| ---- | ---- | -------- | ------- | ----------- |
| `variant` | `'primary' | 'secondary'` | no | `'primary'` | Visual style |
| `disabled` | `boolean` | no | `false` | Disable interaction |

### Emits

- `click` — when user clicks the button

### Examples

```vue
<script setup lang="ts">
import { Button } from '@org/ui-vue'

function onClick() {
  alert('Clicked!')
}
</script>

<template>
  <Button @click="onClick">Click me</Button>
  <Button variant="secondary" disabled>Disabled</Button>
  </template>
```

### Accessibility

- Uses native `<button>` semantics.
