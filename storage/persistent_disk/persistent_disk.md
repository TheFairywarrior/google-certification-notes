# Persistent Disk

Reliable, high-performance block storage for virtual machine instances.

[Full docs here](https://cloud.google.com/persistent-disk/)

* Instances that can be attached to other GCP resources (Compute Engine, Kubernetes Clusters)
* Transparently resized
* Easily backed up
* Can be accessed by multiple readers.
    * Many VMs can read from the same Persistent Disk instance.
* Snap shots are geo-replicated
    * Available to restore in all regions.
* Resize storage while it's in use.
* Automatic encryption


## Features
* Stores data redundantly to ensure its integrity
* Size up to 64TB
* Independent of VM, which means you can switch Disks easily.
* Resize without restarting.