# Storage Classes

This page explains the concept of storage class and the differences between storage classes

[Full docs here](https://cloud.google.com/storage/docs/storage-classes)

## Key concepts
* The class picked will affect the [pricing model](https://cloud.google.com/storage/pricing)
* When specifying a bucket you can choose a `default storage class`
    * Changing the `default storage class` of the bucket does not change the existing objects in the bucket.

## Available storage classes
* Standard Storage	standard	None	
>99.99% in multi-regions and dual-regions
99.99% in regions
Nearline Storage	nearline	30 days	
99.95% in multi-regions and dual-regions
99.9% in regions
Coldline Storage	coldline	90 days	
99.95% in multi-regions and dual-regions
99.9% in regions


|Storage Classes|Name for APIs and gutil|Minimum storage duration|Monthly availability|
|--------|-------|-----|----|
|Standard Storage|standard|None|99.99% uptime in multi regions<br> 99.9% uptime in regions|
|Nearline Storage|nearline|30 days|99.95% uptime in multi regions<br> 99.95% uptime in regions|
|Coldline Storage|coldline|90 days|99.95% uptime in multi regions<br> 99.9% uptime in regions|


## Class descriptions
The following aspects apply to all storage classes:

* Unlimited storage with no minimum object size.
* Worldwide accessibility and worldwide storage locations.
* Low latency (time to first byte typically tens of milliseconds).
* High durability (99.999999999% annual durability).
* Geo-redundancy if the data is stored in a multi-region or dual-region.
* A uniform experience with Cloud Storage features, security, tools, and APIs.


### Standard Storage
* Best for data that is accessed frequently ('hot' data)
* It it best to co-locate this kind of data in the same region as your **Kubernetes** or **Compute Engine**
* When working in dual region, you will get optimized performance to other GCP resources in the same region
* Using multi region, it is storing data around the world. This is the most expensive but means that you can get data to the end user asap.

## Nearline Storage
Used for data that is accessed in-frequently. Best suited for data that is only accessed once a month or less.

## Coldline Storage.
* Best if it's only accessed once a year or less.
* Get data faster than other cold storage solutions.
