# CODTECK-Task1
# Simple Movie Rental RESTful API
# Overview
    This project demonstrates the creation of a simple RESTful API for managing a movie rental database using Express.js (Node.js). The API provides functionality for registering movies, retrieving movie details, updating movie status, and deleting movies from the database.

# Features
## Basic Routing:
  Handle various HTTP methods (GET, POST, PUT, DELETE).
## CRUD Operations:
  Perform Create, Read, Update, and Delete functionalities for movie records.
## Status Management:
  Track the rental status of each movie (available/rented).
## HTML Table Display:
  Display movie data in a structured HTML table format.
## Error Handling:   
  User-friendly error messages for invalid operations.
# Technologies Used

## Node.js: 
  JavaScript runtime environment for server-side programming.
## Express.js:
  Minimal and flexible Node.js web application framework.
## body-parser:
  Middleware to parse incoming request bodies.
## CORS:
  Middleware to enable Cross-Origin Resource Sharing.
## HTML & CSS: 
  For rendering data in a tabular format.
# Endpoints
 GET /database: Retrieve all movie registrations in HTML table format.
GET /database/get/:rented: Retrieve movies filtered by rental status (available/rented).
GET /database/:movieid: Retrieve a single movie by its ID.
POST /register: Register a new movie.
PUT /database/:movieid: Update the rental status of a movie by its ID.
DELETE /database/delete/:movieid: Delete a movie by its ID.
## Installation
## Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/simple-movie-rental-api.git
cd simple-movie-rental-api
## Install dependencies:

bash
Copy code
npm install
## Start the server:

bash
Copy code
npm start
## Access the API:
T## ## he API will be accessible at http://localhost:3000.

# Usage
## Register a New Movie:

Endpoint: POST /register
Body:
json
Copy code
{
  "movieid": 3,
  "movie": "Interstellar",
  "status": "available"
}
## Retrieve All Movies:

Endpoint: GET /database
Retrieve Movies by Rental Status:

Endpoint: GET /database/get/available or GET /database/get/rented
Retrieve a Movie by ID:

Endpoint: GET /database/:movieid
Example: GET /database/1
## Update Movie Rental Status:

Endpoint: PUT /database/:movieid
Example: PUT /database/1
## Delete a Movie by ID:

Endpoint: DELETE /database/delete/:movieid
Example: DELETE /database/delete/1
## Sample Data Structure (movies.json)
[
  {
    "movieid": 1,
    "movie": "The Matrix",
    "status": "available"
  },
  {
    "movieid": 2,
    "movie": "Inception",
    "status": "rented"
  }
]

# Error Handling
## Invalid Movie ID: Alerts the user with an "Invalid Movie Id" message.
## Already Rented Movie: Alerts the user with an "Already rented Movie Id" message.
