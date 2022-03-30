# Movies
# API endpoint to access a movie database

##This folder contains rql code that can be used if you need to access the movie database

Based on https://raw.githubusercontent.com/prust/wikipedia-movie-data/master/movies.json


Endpoints :

## movies-by-title
movies_by_title( `title`:string )

title: title or partial title to search<p>

Example: https://api.raw-labs.com/demos/1/public/movies/movies-by-title?title=Grease

## movies-by-year
movies_by_year( `year`:int )

year: movie year to search for<p>

Example: https://api.raw-labs.com/demos/1/public/movies/movies-by-year?year=2000


