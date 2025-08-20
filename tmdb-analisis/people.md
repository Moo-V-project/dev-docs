# Analysis of the movie makers data provided by TMDB

* [TMDB Documentation](developer.themoviedb.org/docs)
* [TMDB API reference](https://developer.themoviedb.org/reference/intro/getting-started)

For the requests it's possible to use [append-to-response](https://developer.themoviedb.org/docs/append-to-response) to fetch data from multiple endpoints in a single request.

**Wrote with ChatGPT**

## People data

### [Details](https://developer.themoviedb.org/reference/person-details)

The response contains general information about a person.

- **adult** (`boolean`, default: `true`)
  Indicates whether the person is an adult.

- **also_known_as** (`array of strings`)
  Alternative names the person is known by.

- **biography** (`string`)
  A short biography of the person.

- **birthday** (`string`)
  Date of birth (`YYYY-MM-DD`).

- **deathday** (`string`)
  Date of death (`YYYY-MM-DD`), if applicable.

- **gender** (`integer`, default: `0`)
  Gender identifier (0 = not set, 1 = female, 2 = male, 3 = non-binary).

- **homepage** (`string`)
  Official homepage URL.

- **id** (`integer`, default: `0`)
  Unique identifier for the person.

- **imdb_id** (`string`)
  IMDb identifier.

- **known_for_department** (`string`)
  The department the person is primarily known for (e.g., Acting, Directing).

- **name** (`string`)
  Full name of the person.

- **place_of_birth** (`string`)
  Place where the person was born.

- **popularity** (`number`, default: `0`)
  Popularity score.

- **profile_path** (`string`)
  Path to the profile image.


## Credits

### [Details](https://developer.themoviedb.org/reference/credit-details)

- **credit_type** (`string`)
  The type of credit (e.g., cast, crew).

- **department** (`string`)
  Department associated with the credit (for crew members).

- **job** (`string`)
  Specific job title within the department.

- **media** (`object`)
  Media details associated with the credit:
  - **adult** (`boolean`, default: `true`) – Indicates if the media is adult-rated.
  - **backdrop_path** (`string`) – Path to the backdrop image.
  - **id** (`integer`, default: `0`) – Unique identifier for the media.
  - **name** (`string`) – Title/name of the media.
  - **original_language** (`string`) – Original language code.
  - **original_name** (`string`) – Original title of the media.
  - **overview** (`string`) – Summary of the media.
  - **poster_path** (`string`) – Path to the poster image.
  - **media_type** (`string`) – Type of media (e.g., movie, tv).
  - **genre_ids** (`array of integers`) – List of genre identifiers.
  - **popularity** (`number`, default: `0`) – Popularity score.
  - **first_air_date** (`string`) – First air date (for TV shows).
  - **vote_average** (`number`, default: `0`) – Average rating.
  - **vote_count** (`integer`, default: `0`) – Number of votes.
  - **origin_country** (`array of strings`) – List of countries of origin.
  - **character** (`string`) – Character name (if cast).
  - **episodes** (`array`) – Episodes linked to the credit.
  - **seasons** (`array of objects`) – Seasons linked to the credit. Each object contains:
    - **air_date** (`string`) – Season air date.
    - **episode_count** (`integer`, default: `0`) – Number of episodes.
    - **id** (`integer`, default: `0`) – Season ID.
    - **name** (`string`) – Season name.
    - **overview** (`string`) – Season overview.
    - **poster_path** (`string`) – Path to the season’s poster image.
    - **season_number** (`integer`, default: `0`) – Season number.
    - **show_id** (`integer`, default: `0`) – Linked show ID.
    - **media_type** (`string`) – Type of media (should be `tv`).

- **id** (`string`)
  Unique identifier for the credit.

- **person** (`object`)
  Person associated with the credit:
  - **adult** (`boolean`, default: `true`) – Indicates if the person is an adult.
  - **id** (`integer`, default: `0`) – Unique identifier for the person.
  - **name** (`string`) – Display name.
  - **original_name** (`string`) – Original name.
  - **media_type** (`string`) – Type of person object.
  - **popularity** (`number`, default: `0`) – Popularity score.
  - **gender** (`integer`, default: `0`) – Gender identifier.
  - **known_for_department** (`string`) – Department the person is known for.
  - **profile_path** (`string`) – Path to the profile image.
