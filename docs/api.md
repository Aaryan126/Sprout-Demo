# API Documentation

## Authentication

All API requests require an API key passed via the `Authorization` header.

Rate limit: 2000 requests per minute

Responses include an `X-RateLimit-Remaining` header indicating how many requests remain in the current window.

## Endpoints

### GET /api/v2/users

Fetch a list of users. Requires `users:read` scope.

**Response:**
```json
{
  "users": [...],
  "total": 42
}
```

### POST /api/v2/users

Create a new user. Requires `users:write` scope.

## Error Codes

| Code | Meaning |
|------|---------|
| 401  | Invalid or missing API key |
| 429  | Rate limit exceeded |
| 500  | Internal server error |
