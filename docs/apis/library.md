---
title: Library APIs
---

# Library APIs

Document exported symbols from your libraries. Group by module/package.

Example function:

## sum(a, b)

- **Module**: `@acme/math`
- **Since**: v1.0.0

### Signature

```ts
declare function sum(a: number, b: number): number
```

```python
def sum(a: float, b: float) -> float:
    ...
```

```java
public static int sum(int a, int b)
```

### Parameters
- **a** (number): first addend
- **b** (number): second addend

### Returns
- number — arithmetic sum of `a` and `b`

### Examples

```ts
import { sum } from '@acme/math'
sum(2, 3) // 5
```

```python
from acme.math import sum
sum(2, 3)  # 5
```

```java
var s = MathUtils.sum(2, 3); // 5
```

Include classes, interfaces, enums and any configuration objects following the template in APIs Overview.
