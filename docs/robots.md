# Robot Management

## List Robots

Returns all registered robots.

### Endpoint

```http
GET /robots
```

### Example Response

```json
{
  "robots": [
    {
      "id": "RBT001",
      "type": "Picker Robot",
      "status": "ACTIVE",
      "battery": 87
    },
    {
      "id": "RBT002",
      "type": "Pallet Mover",
      "status": "CHARGING",
      "battery": 45
    }
  ]
}
```

---

## Get Robot Status

Returns detailed information about a specific robot.

### Endpoint

```http
GET /robots/{robot_id}
```

### Parameters

| Name | Type | Required |
|--------|--------|--------|
| robot_id | string | Yes |

### Example Request

```http
GET /robots/RBT001
```

### Example Response

```json
{
  "id": "RBT001",
  "status": "ACTIVE",
  "battery": 87,
  "location": "Zone A",
  "current_task": "PICK-1201"
}
```

---

## Stop Robot

Temporarily pauses robot operations.

### Endpoint

```http
POST /robots/{robot_id}/stop
```

### Success Response

```json
{
  "message": "Robot successfully stopped."
}
```

---

## Resume Robot

Resumes robot operations.

### Endpoint

```http
POST /robots/{robot_id}/resume
```

### Success Response

```json
{
  "message": "Robot successfully resumed."
}
```
