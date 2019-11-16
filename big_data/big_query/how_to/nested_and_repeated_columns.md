
# Nested and repeated columns
[Full docs here](https://cloud.google.com/bigquery/docs/nested-repeated)

BigQuery performs best with denormalized data. Nested and repeated columns can maintain relationships without the performance impact of preserving a relational schema.

* Specify these columns through UI or in the JSON schema file
* Uses the RECORD (STRUCT) type which is basically just an array of objects.
* supports loading data from object oriented schemas eg: 
    * JSON
    * Avro
    * Cloud Firestore export files
    * Cloud Datastore export files 
* Nested and Repeated columns are defined using the [`STRUCT`](https://cloud.google.com/bigquery/docs/reference/standard-sql/data-types#struct-type) type
* Cannot have more than 15 levels of nests.
