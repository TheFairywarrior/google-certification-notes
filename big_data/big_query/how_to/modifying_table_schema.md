# Modifying table schema
[Full docs here](https://cloud.google.com/bigquery/docs/managing-table-schemas)

This document describes how to modify the schema definitions for existing BigQuery tables. BigQuery natively supports the following schema modifications:

* Adding columns to a schema definition
* Relaxing a column's mode from REQUIRED to NULLABLE


It is valid to create a table without defining an initial schema and to add a schema definition to the table at a later time.
