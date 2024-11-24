# Movie API

A simple RESTful API built with Go and the Gorilla Mux package to manage a collection of movies. The API supports CRUD operations on movie data.

## Features

- **Get all movies:** Retrieve the list of movies.
- **Get a movie by ID:** Fetch details of a specific movie by ID.
- **Create a movie:** Add a new movie to the collection.
- **Update a movie:** Update an existing movie by ID.
- **Delete a movie:** Remove a movie from the collection by ID.

## Prerequisites

- Go version 1.16 or higher installed on your system.
- `gorilla/mux` package installed.

## Installation

1. Clone the repository:
   ```bash
   git clone github.com/DeepLeau/CRUD_movies_management
   ```
2. Navigate to the project directory:
   ```bash
   cd CRUD_movies_management
   ```
3. Install dependencies:
   ```bash
   go get -u github.com/gorilla/mux
   ```

## Usage

1. Run the server:
   ```bash
   go run main.go
   ```
2. The server will start on `http://localhost:8000`.

## API Endpoints

### GET `/movies`
- **Description:** Get a list of all movies.
- **Response:** JSON array of movie objects.

### GET `/movies/{id}`
- **Description:** Get details of a specific movie by ID.
- **Path Parameter:**
  - `id` (string): The ID of the movie.
- **Response:** JSON object of the requested movie.

### POST `/movies`
- **Description:** Add a new movie to the collection.
- **Request Body:** JSON object representing the movie to add.
- **Response:** JSON object of the created movie.

### PUT `/movies/{id}`
- **Description:** Update an existing movie by ID.
- **Path Parameter:**
  - `id` (string): The ID of the movie to update.
- **Request Body:** JSON object representing the updated movie data.
- **Response:** JSON object of the updated movie.

### DELETE `/movies/{id}`
- **Description:** Delete a movie by ID.
- **Path Parameter:**
  - `id` (string): The ID of the movie to delete.
- **Response:** JSON array of remaining movies.

## Example Movie Object

```json
{
  "id": "1",
  "isbn": "438227",
  "title": "Movie One",
  "director": {
    "firstname": "John",
    "lastname": "Doe"
  }
}
```

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes and commit them (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

## License

This project is licensed under the MIT License.

## Acknowledgements

- [Gorilla Mux](https://github.com/gorilla/mux) for routing in Go.
