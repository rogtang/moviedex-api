Given a JSON file containing information about thousands of movies, create an Express application that supports getting the movies filtered by genre, country or average vote. Secure the API so that it can be safely opened to the public.

The JSON file containing movie information was the 13MB file you downloaded at the start of this checkpoint. That file contained thousands of movies; when developing we can replace the real dataset with a representable sample of the data so that our lives as developers is easier. Here is a link to a smaller version of the movies data for you to download. Submit your project configured to use the smaller dataset as this is just for education purposes.

One movie in the dataset would have the following properties:

{
  "filmtv_ID": 2,
  "film_title": "Bugs Bunny's Third Movie: 1001 Rabbit Tales",
  "year": 1982,
  "genre": "Animation",
  "duration": 76,
  "country": "United States",
  "director": "David Detiege, Art Davis, Bill Perez",
  "actors": "N/A",
  "avg_vote": 7.7,
  "votes": 28
}
Requirements
Create a project called moviedex-api and initialize it as an Express app to meet the following requirements.

Users can search for Movies by genre, country or avg_vote
The endpoint is GET /movie
The search options for genre, country, and/or average vote are provided in query string parameters.
When searching by genre, users are searching for whether the Movie's genre includes a specified string. The search should be case insensitive.
When searching by country, users are searching for whether the Movie's country includes a specified string. The search should be case insensitive.
When searching by average vote, users are searching for Movies with an avg_vote that is greater than or equal to the supplied number.
The API responds with an array of full movie entries for the search results
The endpoint only responds when given a valid Authorization header with a Bearer API token value.
The endpoint should have general security in place such as best practice headers and support for CORS.

HINTS:
When comparing two numeric strings for greater than or less than, we can "cast" the strings to numbers like so:

Number('1') === 1
Number('3') === 3
Number('6.123') === 6.123