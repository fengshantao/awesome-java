---
title: React Components
---

# React Components

Document React components with TypeScript types, props tables, and examples.

## Button

- **Import**: `import { Button } from '@org/ui'`
- **Since**: v1.0.0

### Props

| Name | Type | Required | Default | Description |
| ---- | ---- | -------- | ------- | ----------- |
| `variant` | `'primary' | 'secondary'` | no | `'primary'` | Visual style |
| `disabled` | `boolean` | no | `false` | Disable interaction |
| `onClick` | `(event: React.MouseEvent) => void` | no | — | Click handler |

### Examples

```tsx
import { Button } from '@org/ui'

export function Example() {
  return (
    <>
      <Button onClick={() => alert('Clicked!')}>Click me</Button>
      <Button variant="secondary" disabled>Disabled</Button>
    </>
  )
}
```

### Accessibility

- Renders `<button>` with appropriate `aria-disabled` when disabled.

---

Replicate this structure for all React components.
