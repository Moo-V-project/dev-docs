# Analysis of the miscellaneous data provided by TMDB

* [TMDB Documentation](developer.themoviedb.org/docs)
* [TMDB API reference](https://developer.themoviedb.org/reference/intro/getting-started)

For the requests it's possible to use [append-to-response](https://developer.themoviedb.org/docs/append-to-response) to fetch data from multiple endpoints in a single request.

**Wrote with ChatGPT**

## Movie lists

Shortcuts to discover movies endpoint with predefined filters.

* [Now playing](https://api.themoviedb.org/3/movie/now_playing)
* [Popular](https://api.themoviedb.org/3/movie/popular)
* [Top rated](https://api.themoviedb.org/3/movie/top_rated)
* [Upcoming](https://api.themoviedb.org/3/movie/upcoming)


## Genres

### [Movie List](https://api.themoviedb.org/3/genre/movie/list)

Get the list of official genres for movies.

- **genres** (`array of objects`)
  A list of genre objects. Each object contains:
  - **id** (`integer`, default: `0`) – Unique identifier for the genre.
  - **name** (`string`) – The name of the genre.

### [TV List](https://api.themoviedb.org/3/genre/tv/list)

Get the list of official genres for TV shows.


## Discover

### [Movie](https://api.themoviedb.org/3/discover/movie)

#### Request query parameters

- **certification** (`string`)
  Filter by certification. Use in conjunction with `region`.

- **certification.gte** (`string`)
  Filter for certifications greater than or equal to the given value. Use with `region`.

- **certification.lte** (`string`)
  Filter for certifications less than or equal to the given value. Use with `region`.

- **certification_country** (`string`)
  Specify the country to use for certification-based filters.

- **include_adult** (`boolean`, default: `false`)
  Whether to include adult content.

- **include_video** (`boolean`, default: `false`)
  Whether to include videos.

- **language** (`string`, default: `en-US`)
  Specify the language of the results.

- **region** (`string`)
  Specify the region to filter release dates and certifications.

- **watch_region** (`string`)
  Region to use with `with_watch_monetization_types` or `with_watch_providers`.

- **page** (`int32`, default: `1`)
  Specify the page of results to return.

- **primary_release_year** (`int32`)
  Filter by primary release year.

- **primary_release_date.gte** (`date`)
  Filter for primary release date greater than or equal to this value.

- **primary_release_date.lte** (`date`)
  Filter for primary release date less than or equal to this value.

- **release_date.gte** (`date`)
  Filter for release date greater than or equal to this value.

- **release_date.lte** (`date`)
  Filter for release date less than or equal to this value.

- **sort_by** (`string`, enum, default: `popularity.desc`)
  Sort results by a specific field. Possible values are:

  - `original_title.asc`
  - `original_title.desc`
  - `popularity.asc`
  - `popularity.desc`
  - `revenue.asc`
  - `revenue.desc`
  - `primary_release_date.asc`
  - `primary_release_date.desc`
  - `title.asc`
  - `title.desc`
  - `vote_average.asc`
  - `vote_average.desc`
  - `vote_count.asc`
  - `vote_count.desc`

- **vote_average.gte** (`float`)
  Minimum average vote score.

- **vote_average.lte** (`float`)
  Maximum average vote score.

- **vote_count.gte** (`float`)
  Minimum number of votes.

- **vote_count.lte** (`float`)
  Maximum number of votes.

- - **with_cast** (`string`)
  Filter by cast IDs. Accepts comma (AND) or pipe (OR) separated values.

- **with_crew** (`string`)
  Filter by crew IDs. Accepts comma (AND) or pipe (OR) separated values.

- **with_people** (`string`)
  Filter by people IDs. Accepts comma (AND) or pipe (OR) separated values.

- **with_companies** (`string`)
  Filter by company IDs. Accepts comma (AND) or pipe (OR) separated values.

- **without_companies** (`string`)
  Exclude results with specified companies.

- **with_genres** (`string`)
  Filter by genre IDs. Accepts comma (AND) or pipe (OR) separated values.

- **without_genres** (`string`)
  Exclude results with specified genres.

- **with_keywords** (`string`)
  Filter by keyword IDs. Accepts comma (AND) or pipe (OR) separated values.

- **without_keywords** (`string`)
  Exclude results with specified keywords.

- **with_origin_country** (`string`)
  Filter by origin country.

- **with_original_language** (`string`)
  Filter by original language.

- **with_release_type** (`int32`)
  Possible values: `[1, 2, 3, 4, 5, 6]`.
  Accepts comma (AND) or pipe (OR) separated values. Can be used with `region`.

- **with_runtime.gte** (`int32`)
  Minimum runtime (in minutes).

- **with_runtime.lte** (`int32`)
  Maximum runtime (in minutes).

- **with_watch_monetization_types** (`string`)
  Possible values: `[flatrate, free, ads, rent, buy]`.
  Use with `watch_region`. Accepts comma (AND) or pipe (OR) separated values.

- **with_watch_providers** (`string`)
  Filter by watch providers. Use with `watch_region`. Accepts comma (AND) or pipe (OR) separated values.

- **without_watch_providers** (`string`)
  Exclude results with specified watch providers.

- **year** (`int32`)
  Filter by release year

## Search
