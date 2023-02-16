# IMDB_evaluator
Sort IMDB movies based on linear algorithm.

Setup:
    - Scraper (1)
       - collects TOP20 movies from IMDB, with ratings and number of ratings
        - IMDB data source: https://www.imdb.com/interfaces/
          - title.ratings.tsv.gz - ratings, number of raters
          - title.basics.tsv.gz - movie title names
       - collects Oscar details for movies
        - Oscars data source: https://awardsdatabase.oscars.org/
    - Oscar Calculator (2) - linear algorithm, add extra point for award
      - 1 or 2 oscars → 0.3 point
      - 3 or 5 oscars → 0.5 point
      - 6 to 10 oscars → 1 point
      - 10+ oscars → 1.5 point
    - Review Penalizer (3) - linear algorithm, to subtract points for less feedback
      - 0.1 point substraction after 100k view difference compared to the most rated movie (
- Write out the TOP 20 movies in a sorted (descending) way, including both the original and the adjusted new ratings to a file (JSON, CSV, txt, etc.).
- Provide detailed instructions on how to run your assignment in a separate markdown file.

