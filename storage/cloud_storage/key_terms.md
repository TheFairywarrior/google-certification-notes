# Key Terms
[Full docs here](https://cloud.google.com/storage/docs/key-terms)

## Buckets
* Buckets are the containers that hold all of the objects (files). 
* Everything in Cloud storage must be in a bucket
* All operations should be object intensive and not bucket intensive
* When creating a bucket you specify: 
    * Names are globally unique
    * A geographic location
    * Default storage class
        * The default storage class you choose applies to objects added to the bucket that don't have a storage class specified explicitly.
* Changing a bucket name involves re making the bucket

### Bucket names
* Globally unique because all bucket names are in the same Cloud Storage namespace
* Can be used with a CNAME redirect
* Must conform to DNS naming conventions
* [bucket naming guidelines](https://cloud.google.com/storage/docs/naming#requirements)

### Bucket labels
* key:value metadata pairs
    * Maximum of 64 labels per bucket
    * Cannot be longer than 64 chars
    * Can only contain lowercase letters, numeric characters, underscores, and dashes. International characters are allowed.
    * Keys cannot be empty.
* Allow you to group buckets along with other GCP resources

## Objects
* Individual pieces of data that are stored.
* No limit on amount of objects
* 2 components:
    * Object data: Typically the actual file
    * [Object metadata:](https://cloud.google.com/storage/docs/metadata) key:value pairs that describe the data in the object

### Object Names
* Treated as object meta data
* Less than 1024 bytes
* Any unicode chars
* Objects aren't stored in 'folders' they just appear to be stored in folders.

### Object versions and generation numbers
* Versions are unique
    * Found in object meta data
 

