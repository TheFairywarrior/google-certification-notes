# Choosing between Native Mode and Datastore Mode

## Cloud Firestore in native mode
Mixture between Cloud Datastore and Firebase Realtime Database
Cloud Firestore introduces new features such as:

* A new, strongly consistent storage layer
* A collection and document data model
* Real-time updates
* Mobile and Web client libraries
* Backwards compatible with Datastore

## Cloud Firestore in Datastore mode
Cloud Firestore in Datastore mode uses Cloud Datastore system behavior but accesses Cloud Firestore's storage layer, removing the following Cloud Datastore limitations:

* Eventual consistency, all Cloud Datastore queries become strongly consistent.
* Transactions are no longer limited to 25 entity groups.
* Writes to an entity group are no longer limited to 1 per second.

Datastore mode disables Cloud Firestore features that are not compatible with Cloud Datastore:

* The project will accept Cloud Datastore API requests and deny Cloud Firestore API requests.
* The project will use Cloud Datastore indexes instead of Cloud Firestore indexes.
* You can use Cloud Datastore client libraries with this project but not Cloud Firestore client libraries.
* Cloud Firestore real-time capabilities will not be available.
* In the GCP Console, the database will use the Cloud Datastore viewer.
* Encrypts all of the data before it's written to the disk
    * Google manages the encryption keys
    
### Automatic upgrade to Datastore mode
Existing Cloud Datastore databases will be automatically upgraded to Cloud Firestore in Datastore mode. New projects that require a Cloud Datastore database should use Cloud Firestore in Datastore mode.


## Choosing a database mode
We recommend the following when choosing between database modes:

### Use Cloud Firestore in Datastore mode for new server projects.

Cloud Firestore in Datastore mode allows you to use established Cloud Datastore server architectures while removing fundamental Cloud Datastore limitations. Datastore mode can automatically scale to millions of writes per second.

### Use Cloud Firestore in Native mode for new mobile and web apps.

Cloud Firestore offers mobile and web client libraries with real-time and offline features. Native mode can automatically scale to millions of concurrent clients.