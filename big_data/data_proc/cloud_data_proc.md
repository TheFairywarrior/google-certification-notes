# Cloud Dataproc

A faster, easier, more cost-effective way to run Apache Spark and Apache Hadoop

[Full docs here](https://cloud.google.com/dataproc/)

* Fully managed cloud service to run [Apache Spark](http://spark.apache.org/) and [Apache Hadoop](http://hadoop.apache.org/) clusters.
* Quickly scalable and can resize at any time.
* Price measured by second.
* Have 'preemptible' instances

## Features

### Fully managed

### Resizable clusters
Create and scale clusters with specific machine types.

### Versioning
[Image versioning](https://cloud.google.com/dataproc/docs/concepts/versioning/overview) allows you to switch between different versions of Apache Spark, Hadoop, and other tools

### Enterprise security
When you create a Cloud Dataproc cluster, you can enable Hadoop Secure Mode via Kerberos by adding a [Security Configuration](https://cloud.google.com/dataproc/docs/concepts/configuring-clusters/security). Also,GCP and Cloud Dataproc offer additional security features that help protect your data. Some of the most commonly used GCP-specific security features used with Cloud Dataproc include default at-rest encryption, OS Login, VPC Service Controls, and Customer Managed Encryption Keys (CMEK)

### Scheduled cluster deletion
To save money, there's an option to [delete a cluster](https://cloud.google.com/dataproc/docs/concepts/configuring-clusters/scheduled-deletion) if it's been idle for a specified amount of time.


### Automatic or manual configuration
Hardware and software automatically configured. But [manual control](https://cloud.google.com/dataproc/docs/concepts/cluster-properties) is possible

### Developer Tools
Multiple ways to manage a cluster, including an easy-to-use web UI, the Cloud SDK, RESTful APIs, and SSH access.

### Custom Images
Cloud Dataproc clusters can be provisioned with a custom image that includes your pre-installed Linux operating system packages.

### Flexible Virtual Machines
Clusters can use custom machine types and preemptible virtual machines to make them the perfect size for your needs.


## Notes from questions 
* The HDFS with Dataproc is volatile and cannot hold any information for long periods of time. It is recommended to use GCS.

