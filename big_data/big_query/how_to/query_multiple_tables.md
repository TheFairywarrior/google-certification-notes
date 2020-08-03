# Querying multiple tables using a wildcard table
[Full docs here](https://cloud.google.com/bigquery/docs/querying-wildcard-tables)

* Enable querying of multiple tables
* Concise SQL statements
* Can only be used in Standard SQL

A wildcarded table represents a union of all the tables that contain the wild carded value

eg. A wild card like 'this_is_*' <br>
Would bring back data from tables like:
* this_is_cool
* this_is_not_cool
* this_is_the_tragic_story_of_darth_plagius_the_wise_it's_not_a_story_that_the_jedi_would_of_told_you

Each row in the wildcard table contains a special column that contains the value matched by the wildcard character.

<a href="../wild_card_tables.md">Morer info here</a>

