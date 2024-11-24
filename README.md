
# Go Rest MongoDB Server

A RESTful API server built with Go (Golang) and MongoDB. This server provides CRUD (Create, Read, Update, Delete) functionality for handling data stored in MongoDB. 

## Features

- RESTful API structure
- MongoDB as the database for storing and retrieving data
- Simple and fast performance with Go
- Supports basic CRUD operations (Create, Read, Update, Delete)
- JSON format for API requests and responses

## Technologies Used

- **Go**: The programming language used to build the server.
- **MongoDB**: NoSQL database for storing the data.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Go](https://golang.org/dl/) (v1.18+)
- [MongoDB](https://www.mongodb.com/try/download/community) (v5.0+)
- A code editor (like [Visual Studio Code](https://code.visualstudio.com/))

## Getting Started

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Lingesh15/Go-Rest-MongoDB-Server.git
   cd Go-Rest-MongoDB-Server
   ```

2. **Install dependencies**:

   Make sure you have `mux` and `mongo-driver` Go packages installed:

   ```bash
   go get go.mongodb.org/mongo-driver/mongo
   ```

3. **Set up MongoDB**:

   - Ensure MongoDB Atlas is configured and a cluster is created.
   -  ensure you have the connection string.

4. **Configure environment variables**:

   Create a `.env` file in the root of the project and add your MongoDB URI:

   ```bash
   MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.bywdc.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
   ```

5. **Run the server**:

   Use the following command to start the server:

   ```bash
   go run main.go
   ```

   The server should now be running on `http://localhost:3000`.

## API Endpoints

| Method | Endpoint         | Description                   |
|--------|------------------|-------------------------------|
| GET    | `/api/todos`   | Get all resources             |
| GET    | `/api/todos/{id}` | Get a single resource by ID  |
| POST   | `/api/todos`   | Create a new resource         |
| PUT    | `/api/todos/{id}` | Update an existing resource |
| DELETE | `/api/todos/{id}` | Delete a resource by ID      |

### Example Request (Create Resource)

```bash
POST /api/resource
Content-Type: application/json

{
  "name": "Sample Resource",
  "description": "This is a sample resource."
}
```

### Example Response (Get All Resources)

```json
[
  {
    "_id": "60adf77e73c1e730fcd4f06b",
    "name": "Sample Resource",
    "description": "This is a sample resource."
  }
]
```

## Project Structure

```
├── main.go                # Entry point of the server
├── go.mod                 # Module definitions and dependencies
├── go.sum                 # Dependency checksums
├── .env                   # Environment variables
├── air.toml               # Air configuration for live reloading
├── .gitignore             # Ignored files and directories by Git
└── README.md              # This file
```



