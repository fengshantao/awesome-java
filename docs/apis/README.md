---
title: APIs Overview
---

# APIs Overview

This section standardizes documentation for all public APIs.

Each API entry must include:

- Summary: one‑line purpose
- Availability: module/package and version
- Signature: function/class signature or HTTP method/path
- Parameters: name, type, required, description
- Returns: type and semantics
- Errors: error types and when they occur
- Examples: minimal and advanced usage
- Notes: performance, security, or compatibility considerations

Template (library function/class):

```markdown
## <Symbol Name>

**Module**: `<module>`  |  **Since**: `vX.Y.Z`

### Signature
<language-specific signature(s)>

### Parameters
- **paramName** (Type, required?): description

### Returns
- Type — description

### Errors
- `ErrorType` — when and why

### Examples
```ts
// TypeScript
import { example } from '<module>'
const result = example('input')
```

```python
# Python
from package import example
result = example('input')
```

```java
// Java
var result = Example.example("input");
```

### Notes
- Anything noteworthy
```

Template (REST endpoint): see REST APIs page.
