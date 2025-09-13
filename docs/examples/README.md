---
title: Examples
---

# Examples

End‑to‑end examples showing common tasks.

## Example: Fetch and render users

### REST + React

```tsx
// fetch users then render a list with a Button component
import { useEffect, useState } from 'react'
import { Button } from '@org/ui'

type User = { id: string; name: string }

export default function Users() {
  const [users, setUsers] = useState<User[]>([])

  useEffect(() => {
    fetch('/api/users').then(r => r.json()).then(b => setUsers(b.items))
  }, [])

  return (
    <>
      <h2>Users</h2>
      <ul>
        {users.map(u => <li key={u.id}>{u.name}</li>)}
      </ul>
      <Button onClick={() => alert('Create user...')}>New</Button>
    </>
  )
}
```

### Curl only

```bash
curl -H "Authorization: Bearer $TOKEN" \
  "https://api.example.com/users?page=1&pageSize=20"
```
