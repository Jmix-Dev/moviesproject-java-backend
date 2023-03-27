README Project Description:
This is a simple movie API that allows users to retrieve movie information from a MongoDB database. The API provides two
endpoints: one to get all movies and another to get a single movie by its IMDB ID.

Prerequisites:
Before running the application, ensure that you have the following installed:

Java 17 MongoDB Maven

Installation To install the project, follow these steps:

1. Clone the repository to your local machine.
2. Create a .env file in the root directory of the project.
3. Add the following environment variables to the .env file:

MONGO_DATABASE=<your-mongodb-database>
MONGO_USER=<your-mongodb-username>
MONGO_PASSWORD=<your-mongodb-password>
MONGO_CLUSTER=<your-mongodb-cluster-url>

4. Replace <your-mongodb-*> placeholders with your actual MongoDB database, username, password, and cluster URL.
5. Open a terminal in the project's root directory.
6. Run mvn clean install to build the project.
7. Run java -jar target/movies-0.0.1-SNAPSHOT.jar to start the application.

API Endpoints The API has two endpoints:

GET /api/v1/movies This endpoint returns a list of all movies in the database. The response body is a JSON array
containing movie objects. Example response:

[    {        "id": "61ec5d1d8e37b94375217cb3",        "imdbId": "tt0111161",        "title": "The Shawshank Redemption"
,        "releaseDate": "1994-09-23",        "trailerLink": "https://www.youtube.com/watch?v=6hB3S9bIaco",        "
poster": "https://image.tmdb.org/t/p/w500/9O7gLzmreU0nGkIB6K3BsJbzvNv.jpg",        "
genres": [            "Drama",            "Crime"        ],
"backdrops": [
"https://image.tmdb.org/t/p/w500/j9XKiZrVeViAixVRzCta7h1VU9W.jpg",
"https://image.tmdb.org/t/p/w500/xOjRNnQw1SQxGx3jKbzcqw6Af0R.jpg"
],
"reviewIds": [
{
"id": "61ec5d9b8e37b94375217cb6"
}
]
}, ...
]

GET /api/v1/movies/{imdbId} This endpoint returns a single movie with the specified IMDB ID. The response body is a JSON
object representing the movie. Example response:

{
"id": "61ec5d1d8e37b94375217cb3",
"imdbId": "tt0111161",
"title": "The Shawshank Redemption",
"releaseDate": "1994-09-23",
"trailerLink": "https://www.youtube.com/watch?v=6hB3S9bIaco",
"poster": "https://image.tmdb.org/t/p/w500/9O7gLzmreU0nGkIB6K3BsJbzvNv.jpg",
"genres": [
"Drama",
"Crime"
],
"backdrops": [
"https://image.tmdb.org/t/p/w500/j9XKiZrVeViAixVRzCta7h1VU9W.jpg",
"https://image.tmdb.org/t/p/w500/xOjRNnQw1SQxGx3jKbzcqw6Af0R.jpg"
],
"reviewIds": [
{
"id": "61ec5d9b8e37b94375217cb6"
}
]
}

This response includes the following fields:

- id: The unique identifier of the movie in the database.
- imdbId: The IMDB ID of the movie.
- title: The title of the movie.
- releaseDate: The release date of the movie.
- trailerLink: The link to the trailer of the movie.
- poster: The link to the poster of the movie.
- genres: An array of genres of the movie.
- backdrops: An array of links to the backdrops of the movie.
- reviewIds: An array of review IDs associated with the movie.

Further Development This project can be further improved in the following ways:

Add endpoints for creating, updating, and deleting movies. Implement authentication and authorization for the API. Add
pagination and sorting to the API endpoints for better performance. Improve error handling and response messages.

## Acknowledgements

This project was developed as a learning exercise. The code was inspired by various tutorials and online resources.