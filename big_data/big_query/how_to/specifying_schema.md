# Specifying a schema
[Full docs](https://cloud.google.com/bigquery/docs/schemas)

Specify schema in one of the following ways:
* Manually
    * Using GCP console
    * Using BigQuery UI
    * Inline using CLI
* Create schema in JSON file
    * ```
        [
            {
                "description": "[DESCRIPTION]",
                "name": "[NAME]",
                "type": "[TYPE]",
                "mode": "[MODE]"
            },
            {
                "description": "[DESCRIPTION]",
                "name": "[NAME]",
                "type": "[TYPE]",
                "mode": "[MODE]"
            }
        ] 
    * 
    
* Call the jobs.insert method and configure the schema property in the load job configuration.
* Call the tables.insert method and configure the schema in the table resource using the schema property.

After data is loaded you can [edit tables schema definition](./modifying_table_schema.md)


## Schema components
### Column names
A column name must contain only letters (a-z, A-Z), numbers (0-9), or underscores (_), and it must start with a letter or underscore. The maximum column name length is 128 characters. A column name cannot use any of the following prefixes:

* \_TABLE_
* \_FILE_
* \_PARTITION

Column names must be unique

### Data Types
* Integer - Numeric values without fractional components
* Floating point - Approximate numeric values with fractional components
* Numeric - Exact numeric values with fractional components
* Boolean - TRUE or FALSE (case insensitive)
* String - Variable-length character (Unicode) data
* Bytes - Variable-length binary data
* Date - A logical calendar date
* Datetime - A year, month, day, hour, minute, second, and subsecond
* Time - A time, independent of a specific date
* Timestamp - An absolute point in time, with microsecond precision
* Struct (Record) - Container of ordered fields each with a type (required) and field name (optional)
* Geography - A pointset on the Earth's surface (a set of points, lines and polygons on the WGS84 reference spheroid, with geodesic edges)

## Modes
BigQuery supports the following modes for your columns. Mode is optional. If the mode is unspecified, the column defaults to NULLABLE.

|Mode|Description|
|----|-----------|
|Nullable|Column allows NULL values (default)|
|Required|NULL values are not allowed|
|Repeated|Column contains an array of values of the specified type|


