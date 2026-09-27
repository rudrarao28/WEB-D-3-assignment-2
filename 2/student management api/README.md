# Student Management REST API

Simple REST API built with Node.js and Express to manage student records.
Data is stored in memory (a plain array), no database used.

## Setup

```
npm install
npm start
```

Server runs on `http://localhost:3000`

## Project Structure

```
app.js
routes/studentRoutes.js
middleware/logger.js
data/students.js
```

## API Endpoints

| Method | Endpoint       | Description           |
|--------|----------------|------------------------|
| GET    | /students      | Get all students       |
| GET    | /students/:id  | Get one student by id  |
| POST   | /students      | Add a new student      |
| PUT    | /students/:id  | Update a student       |
| DELETE | /students/:id  | Delete a student       |

## Sample Request Body (POST / PUT)

```json
{
  "name": "Himanshu",
  "course": "Law"
}
```

## Status Codes Used

- 200 Success
- 201 Created
- 400 Bad Request (missing name/course)
- 404 Not Found (student id doesn't exist)

## Testing

Tested using Postman for all CRUD operations.
