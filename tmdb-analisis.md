# Analysis of the movie and movie makers data provided by TMDB

* [TMDB Documentation](developer.themoviedb.org/docs)
* [TMDB API reference](https://developer.themoviedb.org/reference/intro/getting-started)

**Wrote with ChatGPT**

## Movie data

All this endpoint take movie id as a parameter

### [Movie details](https://developer.themoviedb.org/reference/movie-details)

The response contains general information about a movie.

- **adult** (`boolean`, default: `true`)
  Indicates whether the movie is adult-rated.

- **backdrop_path** (`string`)
  Path to the backdrop image.

- **belongs_to_collection** (`string`)
  The collection the movie belongs to, if any.

- **budget** (`integer`, default: `0`)
  The budget of the movie.

- **genres** (`array of objects`)
  List of genre objects:
  - **id** (`integer`, default: `0`)
  - **name** (`string`)

- **homepage** (`string`)
  Official homepage URL.

- **id** (`integer`, default: `0`)
  Unique identifier for the movie.

- **imdb_id** (`string`)
  IMDb identifier.

- **original_language** (`string`)
  The original language code.

- **original_title** (`string`)
  The original title of the movie.

- **overview** (`string`)
  A brief summary of the movie.

- **popularity** (`number`, default: `0`)
  Popularity score.

- **poster_path** (`string`)
  Path to the poster image.

- **release_date** (`string`)
  Release date in `YYYY-MM-DD` format.

- **revenue** (`integer`, default: `0`)
  The total revenue earned.

- **runtime** (`integer`, default: `0`)
  Duration of the movie in minutes.

- **status** (`string`)
  Current release status (e.g., Released, Post Production).

- **tagline** (`string`)
  Tagline of the movie.

- **title** (`string`)
  Title of the movie.

- **video** (`boolean`, default: `true`)
  Indicates whether the entry has a video.

- **vote_average** (`number`, default: `0`)
  Average rating score.

- **vote_count** (`integer`, default: `0`)
  Number of votes received.

- **production_companies** (`array of objects`)
  - **id** (`integer`, default: `0`)
  - **logo_path** (`string`)
  - **name** (`string`)
  - **origin_country** (`string`)

- **production_countries** (`array of objects`)
  - **iso_3166_1** (`string`) – Country code
  - **name** (`string`) – Country name

- **spoken_languages** (`array of objects`)
  - **english_name** (`string`)
  - **iso_639_1** (`string`) – Language code
  - **name** (`string`) – Native language name

### [Movie Credits](https://developer.themoviedb.org/reference/movie-credits)

The response contains information about the cast and the crew of a movie.

- **id** (`integer`, default: `0`)
  Unique identifier for the movie or TV show.

- **cast** (`array of objects`)
  List of cast members. Each object contains:
  - **adult** (`boolean`, default: `true`) – Indicates if the person is an adult actor.
  - **gender** (`integer`, default: `0`) – Gender identifier (e.g., 1 = female, 2 = male, 0 = not set).
  - **id** (`integer`, default: `0`) – Unique identifier for the person.
  - **known_for_department** (`string`) – The department the person is known for (e.g., Acting).
  - **name** (`string`) – The person’s display name.
  - **original_name** (`string`) – The original name of the person.
  - **popularity** (`number`, default: `0`) – Popularity score.
  - **profile_path** (`string`) – Path to the profile image.
  - **cast_id** (`integer`, default: `0`) – Identifier for the cast entry.
  - **character** (`string`) – The character name played.
  - **credit_id** (`string`) – Unique identifier for the credit.
  - **order** (`integer`, default: `0`) – The order in which cast appears in credits.

- **crew** (`array of objects`)
  List of crew members. Each object contains:
  - **adult** (`boolean`, default: `true`) – Indicates if the person is an adult.
  - **gender** (`integer`, default: `0`) – Gender identifier.
  - **id** (`integer`, default: `0`) – Unique identifier for the person.
  - **known_for_department** (`string`) – The primary department (e.g., Directing).
  - **name** (`string`) – The person’s display name.
  - **original_name** (`string`) – The original name of the person.
  - **popularity** (`number`, default: `0`) – Popularity score.
  - **profile_path** (`string`) – Path to the profile image.
  - **credit_id** (`string`) – Unique identifier for the credit.
  - **department** (`string`) – The department for this specific crew job.
  - **job** (`string`) – The crew job title (e.g., Director, Producer).

### [External IDs](https://developer.themoviedb.org/reference/movie-external-ids)

The response contains identifiers for a movie in external services.

- **id** (`integer`, default: `0`)
  Unique identifier for the resource.

- **imdb_id** (`string`)
  IMDb identifier.

- **wikidata_id** (`string`)
  Wikidata entity ID.

- **facebook_id** (`string`)
  Facebook profile/page ID.

- **instagram_id** (`string`)
  Instagram handle/ID.

- **twitter_id** (`string`)
  Twitter (X) handle/ID.


### [Keywords](https://developer.themoviedb.org/reference/movie-keywords)

The response contains keywords associated with a movie.


- **id** (`integer`, default: `0`)
  Unique identifier for the resource.

- **keywords** (`array of objects`)
  List of keyword objects. Each object contains:
  - **id** (`integer`, default: `0`) – Unique identifier for the keyword.
  - **name** (`string`) – The keyword text.


### [Lists](https://developer.themoviedb.org/reference/movie-lists)

The response contains information about lists that a movie was added to.

- **id** (`integer`, default: `0`)
  Unique identifier for the resource.

- **page** (`integer`, default: `0`)
  The current page number.

- **results** (`array of objects`)
  A list of result objects. Each object contains:
  - **description** (`string`) – The description of the list.
  - **favorite_count** (`integer`, default: `0`) – Number of users who marked this list as favorite.
  - **id** (`integer`, default: `0`) – Unique identifier for the list.
  - **item_count** (`integer`, default: `0`) – Number of items in the list.
  - **iso_639_1** (`string`) – Language code of the list.
  - **list_type** (`string`) – The type of the list.
  - **name** (`string`) – Name of the list.
  - **poster_path** (`string`) – Path to the poster image representing the list.

- **total_pages** (`integer`, default: `0`)
  Total number of pages available.

- **total_results** (`integer`, default: `0`)
  Total number of results across all pages.


### [Recommendations](https://developer.themoviedb.org/reference/movie-recommendations)

The response contains a list of recommended movies based on the provided movie ID.

The API reference does not specify the fields in the response, but basically it includes the same fields as the movie details endpoint.


### [Reviews](https://developer.themoviedb.org/reference/movie-reviews)

The response contains a list of reviews for a movie.

- **id** (`integer`, default: `0`)
  Unique identifier for the resource.

- **page** (`integer`, default: `0`)
  The current page number.

- **results** (`array of objects`)
  A list of review objects. Each object contains:
  - **author** (`string`) – The name of the review’s author.
  - **author_details** (`object`) – Details about the author:
    - **name** (`string`) – The author’s display name.
    - **username** (`string`) – The author’s username.
    - **avatar_path** (`string`) – Path to the author’s avatar image.
    - **rating** (`string`) – Rating given by the author OR the author's rating.
  - **content** (`string`) – The text content of the review.
  - **created_at** (`string`) – The date and time when the review was created.
  - **id** (`string`) – Unique identifier for the review.
  - **updated_at** (`string`) – The date and time when the review was last updated.
  - **url** (`string`) – URL to the review.

- **total_pages** (`integer`, default: `0`)
  Total number of pages available.

- **total_results** (`integer`, default: `0`)
  Total number of reviews across all pages.


### [Similar](https://developer.themoviedb.org/reference/movie-similar)

The response contains a list of movies similar to the provided movie ID.

The response structure is similar to the recommendations endpoint.


### See also

Also the similar data is available for [TV shows](https://developer.themoviedb.org/reference/tv-series-details),
[their seasons](https://developer.themoviedb.org/reference/tv-season-details),
and [episodes](https://developer.themoviedb.org/reference/tv-episode-details).


## People data


## Movie lists


## Genres


## Discover


## Credits


## Search

