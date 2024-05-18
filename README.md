# Movie API

## Introduction

Movie API is a simple RESTful API for managing movies. It allows users to perform CRUD (Create, Read, Update, Delete) operations on movie data.

## Installation

1. Make sure you have Go installed on your system. If not, you can download and install it from the [official Go website](https://golang.org/dl/).

2. Clone this repository:

    ```bash
    git clone <repository-url>
    ```

3. Navigate to the project directory:

    ```bash
    cd movie-api
    ```

4. Install dependencies:

    ```bash
    go mod tidy
    ```

5. Run the server:

    ```bash
    go run main.go
    ```

## Usage

### Endpoints

- `GET /movies`: Retrieve a list of all movies.
- `GET /movie/{id}`: Retrieve details of a specific movie by ID.
- `POST /movies`: Create a new movie.
- `PUT /movie/{id}`: Update an existing movie by ID.
- `DELETE /movie/{id}`: Delete a movie by ID.

### Request/Response Formats

- **GET /movies**: Returns a JSON array containing details of all movies.
- **GET /movie/{id}**: Returns JSON data of the movie with the specified ID.
- **POST /movies**: Expects JSON data of the new movie to be created. Returns JSON data of the created movie.
- **PUT /movie/{id}**: Expects JSON data of the updated movie. Returns JSON data of the updated movie.
- **DELETE /movie/{id}**: Deletes the movie with the specified ID. Returns JSON data of the remaining movies.

### Sample Movie JSON Format

```json
{
  "id": "1",
  "isbn": "978-0-06-112008-4",
  "title": "To Kill a Mockingbird",
  "director": {
    "firstName": "Robert",
    "lastName": "Mulligan"
  }
}
