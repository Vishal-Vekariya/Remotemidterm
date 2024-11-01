# Student API

A simple RESTful API built with Flask that supports basic CRUD operations (Create, Read, Update, Delete) for managing students. Each student has the following attributes:
- **ID** (Integer)
- **Name** (String)
- **Grade** (String)
- **Email** (String)

## Table of Contents
- [Getting Started](#getting-started)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Testing the API](#testing-the-api)

---

## Getting Started

### Prerequisites
- [Python 3.x](https://www.python.org/downloads/) installed on your machine
- [pip](https://pip.pypa.io/en/stable/installation/) package installer for Python
- Optional: [VS Code REST Client extension](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) for testing with `.http` files

### Project Setup
Clone this repository and navigate into the project directory:
```bash
git clone <your-repo-url>
cd student-api
```

### Installation

1. Create a Virtual Environment (optional but recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use 'venv\Scripts\activate'
```

2. Install Required Packages Use the requirements.txt file to install dependencies:

```bash
pip install -r requirements.txt
```

## Running the Application:
To start the this app, run the following command:

```bash
python app.py
```
The app will be accessible at http://localhost:8000

## API Endpoints

| Method | Endpoint           | Description                |
|--------|---------------------|----------------------------|
| GET    | `/`                | Welcome message            |
| GET    | `/health`          | Health check               |
| GET    | `/students`        | Retrieve all students      |
| GET    | `/students/{id}`   | Retrieve student by ID     |
| POST   | `/students`        | Add a new student          |
| PUT    | `/students/{id}`   | Update a student by ID     |
| DELETE | `/students/{id}`   | Delete a student by ID     |

## Example Request and Response

### GET all students

**Request:**
```http
GET /students
```

### Response:

```json
[
    {
        "id": 1,
        "name": "Alice",
        "grade": "A",
        "email": "alice@example.com"
    },
]
```
### Testing the API
You can use the .http file provided in the repository for easy testing using the REST Client extension in VS Code. The file contains sample HTTP requests for each endpoint.
