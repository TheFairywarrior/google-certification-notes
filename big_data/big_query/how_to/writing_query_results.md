# Writing query results

## Temporary table:
* Randomly named.
* Saved in special dataset.
* Caches a query reults
* Not charged for storing temporary tables.

## Permanent Tables
* Basics:
    * New or existing table
    * Writing data to a new table is charged for.
    *  When writing data, the queried tables need to be in the same location as the destination table. 
* Writing queries to permanent tables:
    * When writing queries to permanent tables you can:
        * Create a new table
        * Append to a previous table
        * Overwrite an existing table.
    * You can write query results to a permanent table by:
        * Using the GCP Console or the classic BigQuery web UI
        * Using the command-line tool's bq query command
        * Calling the jobs.insert API method and configuring a query job
        * Using the client libraries

## Writing large query results
Normally, queries have a maximum response size. If you plan to run a query that might return larger results, you can:

* In standard SQL, specify a destination table for the query results.
* In legacy SQL, specify a destination table and set the allowLargeResults option.
When you specify a destination table for large query results, you are charged for storing the data.

### Limitations
In legacy SQL, writing large results is subject to these limitations:

* You must specify a destination table.
* You cannot specify a top-level ORDER BY, TOP or LIMIT clause. Doing so negates the benefit of using allowLargeResults, because the query output can no longer be computed in parallel.
* Window functions can return large query results only if used in conjunction with a PARTITION BY clause.

## Required permissions
At a minimum, to write query results a table, you must be granted the following permissions:

* bigquery.tables.create permissions to create a new table
* bigquery.tables.updateData to write data to a new table, overwrite a table, or append data to a table
* bigquery.jobs.create to run a query job    

The following predefined Cloud IAM roles include bigquery.jobs.create permissions:

* bigquery.user
* bigquery.jobUser
* bigquery.admin

# In addition
* Also if a user has `bigquery.datasets.create` and they create a dataset, they will get `bigquery.datasets.dataOwner` permission. 
* bigquery.dataOwner access gives the user the ability to create and update tables in the dataset.