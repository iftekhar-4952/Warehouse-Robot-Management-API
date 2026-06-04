# Task Management

## Create Task

Assigns a warehouse task to a robot.

### Endpoint

```http
POST /tasks
```

### Request Body

```json
{
  "robot_id": "RBT001",
  "task_type": "PICK",
  "location": "Zone A",
  "priority": "HIGH"
}
```

### Success Response

```json
{
  "task_id": "TASK-5001",
  "status": "ASSIGNED"
}
```

---

## Get Task Status

### Endpoint

```http
GET /tasks/{task_id}
```

### Example Response

```json
{
  "task_id": "TASK-5001",
  "status": "IN_PROGRESS",
  "assigned_robot": "RBT001"
}
```
