# BigQuery Connector
[Full docs here](https://cloud.google.com/dataproc/docs/concepts/connectors/bigquery)

 * Big Query connector enables read/write access to BigQUery. 
 * With the connector command line access is not exposed. 
 * Connector library allows spark and hadoop applications to process data from BigQuery and write data to BigQuery using its native terminology.


 ## Pricing considerations
When using the connector, charges include BigQuery usage fees. The following service-specific charges may also apply:

* Cloud Storage - the connector downloads data into a Cloud Storage bucket before or during job execution. After the job successfully completes, the data is deleted from Cloud Storage. You are charged for this storage according to Cloud Storage pricing. To avoid excess charges, check your Cloud Storage account and remove unneeded temporary files.
* BigQuery Storage API - to achieve better performance, the connector reads data using the BigQuery Storage API. You are charged for this usage according to BigQuery Storage API pricing.