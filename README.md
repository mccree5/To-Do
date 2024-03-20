# To-Do List API

This API provides functionality to manage a to-do list. It is built using the Spring Boot framework in Java.

## Features

- **GET /tasks**: Retrieve all tasks in the to-do list.
- **GET /tasks/{id}**: Retrieve a specific task by ID.
- **POST /tasks**: Add a new task to the to-do list.
- **PUT /tasks/{id}**: Update an existing task.
- **DELETE /tasks/{id}**: Delete a task by ID.
- **DELETE /tasks: Delete all tasks in the to-do list.


JSON Format Explanation
task (String): The title or name of the task.
description (String): A description or additional information about the task.
completed (Boolean): Indicates whether the task is completed (true) or not (false).
dueDate (String): The due date of the task in the format "YYYY-MM-DD".


## Usage

### GET /tasks

Returns all tasks in the to-do list.

Example:

```
curl http://localhost:8080/tasks
```

### GET /tasks/{id}

Returns a specific task by ID.

Example:

```
curl http://localhost:8080/tasks/1
```

### POST /addTask

Adds a new task to the to-do list.

Example:

```
curl -X POST http://localhost:8080/addTask -H "Content-Type: application/json" -d '{"task":"Task title","description":"Task description","completed":false,"dueDate":"2024-03-20"}'
```

### PUT /tasks/{id}

Updates an existing task.

Example:

```
curl -X PUT http://localhost:8080/tasks/1 -H "Content-Type: application/json" -d '{"task":"Updated title","description":"Updated description","completed":true,"dueDate":"2024-03-25"}'
```

### DELETE /clearTasks

Deletes all tasks in the to-do list.

Example:
```
curl -X DELETE http://localhost:8080/clearTasks
```

