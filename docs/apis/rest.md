---
title: REST APIs
---

# REST APIs

Document each endpoint with: method, path, purpose, auth, params, request/response schemas, status codes, and examples.

Example structure:

## GET /users

- **Purpose**: List users
- **Auth**: Bearer token
- **Query params**:
  - `page` (integer, optional): page index starting at 1
  - `pageSize` (integer, optional): items per page (max 100)
- **Responses**:
  - 200 OK — `application/json`
  - 401 Unauthorized

```json
{
  "items": [{"id": "u_123", "name": "Ada"}],
  "page": 1,
  "pageSize": 20,
  "total": 1
}
```

### Examples

```bash
curl -H "Authorization: Bearer $TOKEN" \
  "https://api.example.com/users?page=1&pageSize=20"
```

```ts
// TypeScript (fetch)
const res = await fetch(`${baseUrl}/users?page=1&pageSize=20`, {
  headers: { Authorization: `Bearer ${token}` }
});
const body = await res.json();
```

---

## POST /users

- **Purpose**: Create a user
- **Auth**: Bearer token
- **Body** (`application/json`):
```json
{
  "name": "Ada"
}
```
- **Responses**:
  - 201 Created — `Location` header points to new resource
  - 400 Bad Request — validation errors

### Examples

```bash
curl -X POST -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name":"Ada"}' \
  "https://api.example.com/users"
```

```ts
// TypeScript (axios)
const { data } = await axios.post(`${baseUrl}/users`, { name: 'Ada' }, {
  headers: { Authorization: `Bearer ${token}` }
});
```

Provide similar sections for update, delete, and any domain endpoints.
