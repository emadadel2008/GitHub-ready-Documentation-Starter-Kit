# 08 - API

## API Documentation Template

### GET /orders/{id}

**Purpose:** Retrieve an order.

**Authentication:** Bearer token

**Request**

```http
GET /orders/123
Authorization: Bearer <token>
```

**Response**

```json
{
  "id": "123",
  "status": "processing"
}
```

### Error Handling

| Code | Meaning |
|---|---|
| 400 | Invalid request |
| 401 | Authentication required |
| 403 | Not authorized |
| 404 | Resource not found |
| 500 | Server error |

## Never Guess

If the endpoint behavior has not been verified from code or an authoritative API definition, mark it as:

`⚠️ Example — requires validation`
