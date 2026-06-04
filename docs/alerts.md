# Alerts & Monitoring

## List Alerts

Returns active system alerts.

### Endpoint

```http
GET /alerts
```

### Example Response

```json
{
  "alerts": [
    {
      "id": "ALT-101",
      "severity": "HIGH",
      "message": "Robot battery below threshold"
    }
  ]
}
```

---

## Acknowledge Alert

Marks an alert as reviewed.

### Endpoint

```http
POST /alerts/{alert_id}/acknowledge
```

### Success Response

```json
{
  "message": "Alert acknowledged."
}
```
