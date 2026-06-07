# GitHub User API Backend

A simple REST API built with **Node.js**, **Express.js**, and **CORS** that provides GitHub-style user data. This project serves user information through API endpoints and can be used as a backend for frontend applications.

## Features

* Get all users
* Get a single user by ID
* JSON API responses
* CORS enabled
* Simple Express.js setup

## Tech Stack

* Node.js
* Express.js
* CORS

## Installation

1. Clone the repository:

```bash
git clone https://github.com/Rajeev-2100/backend-users.git
```

2. Navigate to the project directory:

```bash
cd backend
```

3. Install dependencies:

```bash
npm install
```

4. Start the server:

```bash
node index.js
```

Server will run on:

```text
http://localhost:3000
```

## API Endpoints

### Get All Users

**Endpoint**

```http
GET /users
```

**Response**

```json
{
  "users": [
    {
      "id": 1,
      "username": "octocat",
      "name": "The Octocat",
      "repoCount": 8,
      "location": "San Francisco"
    }
  ]
}
```

---

### Get User By ID

**Endpoint**

```http
GET /users/:id
```

**Example**

```http
GET /users/1
```

**Response**

```json
{
  "user": {
    "id": 1,
    "username": "octocat",
    "name": "The Octocat",
    "repoCount": 8,
    "location": "San Francisco"
  }
}
```

### User Not Found

**Response**

```json
{
  "message": "User not found."
}
```

Status Code:

```http
404 Not Found
```

## Project Structure

```text
backend/
│
├── index.js
├── package.json
└── README.md
```

## Sample Users

The API includes sample data for:

* The Octocat
* Linus Torvalds
* Dan Abramov
* Addy Osmani
* TJ Holowaychuk

## Future Improvements

* Add database integration
* Create POST, PUT, and DELETE endpoints
* Add authentication
* Add pagination and search functionality
* Add unit and integration tests

## License

This project is licensed under the MIT License.
