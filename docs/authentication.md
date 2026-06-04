# Authentication

All API requests require Bearer Token authentication.

## Authorization Header

```http
Authorization: Bearer YOUR_API_KEY
```

## Example Request

```bash
curl -X GET https://api.robofleet.com/v1/robots \
-H "Authorization: Bearer YOUR_API_KEY"
```

## Authentication Errors

| Status Code | Description |
|-------------|-------------|
| 401 | Invalid API key |
| 403 | Access denied |
