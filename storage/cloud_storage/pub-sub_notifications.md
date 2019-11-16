# Cloud Pub/Sub notifications for Cloud Storage
This page provides an overview of Cloud Pub/Sub Notifications for Cloud Storage. To learn how to set up and use Cloud Pub/Sub Notifications.

You can setup PUB/SUB to listen for certain events and then send a message to a topic.

Those events being: 

* OBJECT_FINALIZE	
    * Sent when an object is created or updated.
* OBJECT_METADATA_UPDATE	
    * Sent when the metadata of an existing object changes.
* OBJECT_DELETE	
    * Sent when an object has been permanently deleted. This includes objects that are overwritten or are deleted as part of the bucket's lifecycle configuration. For buckets with object versioning enabled, this is not sent when an object is archived (see OBJECT_ARCHIVE), even if archival occurs via the storage.objects.delete method.
* OBJECT_ARCHIVE
    * Only sent when a bucket has enabled object versioning. This event indicates that the live version of an object has become an archived version, either because it was archived or because it was overwritten by the upload of an object of the same name.


## Overwriting objects
Will send a OBJECT_FINALIZE with a `overwrittenByGeneration` flag.
And will send either a OBJECT_DELETE or a OBJECT_ARCHIVE. Depending on what storage technique is being used.
