# User & Orders API – Test Cases

> Note: These tests assume a simulated API with a base URL like `https://api.example.com`.

---

## TC_API_01 – Successful Login with Valid Credentials

**Endpoint:** `POST /login`  
**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "Password123"
}
