
# Compute Engine
Google Compute Engine lets you create virtual machines running different operating systems, including multiple flavors of Linux (Debian, Ubuntu, Suse, Red Hat, CoreOS) and Windows Server, on Google infrastructure. You can run thousands of virtual CPUs on a system that has been designed to be fast and to offer strong consistency of performance.

## High-Performance, Scalable VMs
Google Compute Engine delivers virtual machines running in Google's innovative data centers and worldwide fiber network. Compute Engine's tooling and workflow support enable scaling from single instances to global, load-balanced cloud computing.


* Boot quickly
* Have persistent disk (HDD or SSD)
* Utilizes ssd performance
* Use pre-defined or custom options in setup

For extra performance requirements look (or running ML models) look into [cloud tpu](cloud_tpu.md) or [cloud gpu](cloud_gpu.md)


## Low cost, automatic discounts
* Compute engine uses second level increments
* Only pay for the time you use
* Auto discounts on larger loads

## Fast & Efficient Networking

* Consistent cross-machine bandwidth
* Connect to machines in other datacenters because of google fiber

## Environmentally Friendly Global Network
* Infrastructure is entirely carbon-neutral. 
* Global network of data centers consume 50% of typical datacenters. 
* Growing footprint to bring services closer to the end user

## Compute Engine feature summary
* Pre-defined machine types:
    * Cover almost all common use cases from micro performance to mega data proccessing
    * Makes it easier to create an instance
* Custom machine types:
    * Ability to build the vm to your exact specifications. 
    * Can create an image of 
* Persistent Disks:
    * Network storage
    * Up to 64 TB
    * HDD or SSD
    * Snapshot of persistant disk can make another instance of persistance disk
    * Persistance disks retain data even if VM is terminated
* Local SSD:
    * SSD attached to physical server
    * Always encrypted SSD
    * Size up to 3 TB
* Transparent Maintenance:
    *  [Live migration](live_migrate.md) technology makes it so that the hardware is upgraded without any input from you.
* Global Load Balancing:
    * Disperse requests accross pools of instances
    * Accross multiple regions
* Batch Proccessing:
    * Cost effectively run large compute and batch jobs using [Preemtible instances](preemtible.md)
    * Fixed pricing
* Per-Second Billing:
    * Google bills in second-level increments. You pay only for the compute time that you use.
* Automatic Discounts: 
    * With [Sustained Use Discounts](sustained_user_discounts.md), we automatically give you discounted prices for long-running workloads with no sign-up fees or up-front commitment.
* Commitment savings:
    * With [Committed Use Discounts](committed_use_discounts.md) you can save up to 57% with no upfront costs or instance-type lockin.
* Containers:
    * Run, manage, and orchestrate Docer containers on [Compute Egnine vms](https://cloud.google.com/compute/docs/containers/) or with Google [Kubernetes Engine](https://cloud.google.com/kubernetes-engine/)
