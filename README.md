# Todo App Backend

REST API for the Todo App, built with Express and MongoDB.

## Requirements

- Node.js 18+
- MongoDB
- pnpm

## Getting Started

```bash
pnpm install
```

Create a `.env` file:

```env
MONGODB_URI=mongodb://localhost:27017/todoapp
PORT=5000
```

```bash
# Development
pnpm dev

# Production
pnpm start
```

## API

Base URL: `/api/todos`

| Method | Path  | Description    |
| ------ | ----- | -------------- |
| GET    | /     | Get all todos  |
| POST   | /     | Create a todo  |
| PUT    | /:id  | Update a todo  |
| DELETE | /:id  | Delete a todo  |

### Todo Object

```json
{
  "_id": "string",
  "title": "string",
  "description": "string",
  "completed": false,
  "createdAt": "ISO 8601",
  "updatedAt": "ISO 8601"
}
```

### POST / PUT Request Body

```json
{
  "title": "Buy groceries",
  "description": "Milk, eggs, bread",
  "completed": false
}
```

`title` is required for POST.

## Project Structure

```
backend/
├── server.js
└── src/
    ├── controllers/
    │   └── todoController.js
    ├── models/
    │   └── Todo.js
    └── routes/
        └── todos.js
```
