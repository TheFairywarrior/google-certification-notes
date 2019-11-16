# Kubernetes Engine
[goto docs](https://cloud.google.com/kubernetes-engine/)

Reliable, efficient, and secured way to run Kubernetes clusters

* Development and iteration by making it easy to deploy, update, and manage your applications and services.
* Managed, production-ready environment for deploying containerized applications. 
* Built-in Kubernetes Engine dashboard
* Routine health checks are done to find and replace hung, or crashed, applications.
* Effortless auto scaling
* Clusters can be isolated into the google networks (Global Virtual Private Cloud (VPC))
* Makes it easy to migrate to and from the cloud
* Migrate for [Anthos](../migration/migration_with_anthos.md) makes it easy to convert workloads into a containerized format

## Features

* Identity and access management
    * Control cluster access through Google accounts and role permissions.
* Reserve IP range.
    * Allows cluster IP to co exist with private network IPs
* Security and Compliance
    * Kubernetes Engine is backed by Google security team of over 750 experts and is both HIPAA and PCI DSS 3.1 compliant.
* Integrated Logging & Monitoring
    * Enable [Stackdriver Logging](../stack_driver/stack_driver_logging.md) and Stackdriver Monitoring with simple checkbox configurations, making it easy to gain insight into how your application is running.
* Auto Scale
    * Automatically scale your application deployment up and down based on resource utilization (CPU, memory).
* Automatically keep the cluster up to date without any effort.
* Auto repair checks the health checks and if one fails it immediately runs repair on that node
* Allows specification of resource limits (RAM, CPU and Storage)) 
* Use [GKE Sandbox](https://cloud.google.com/kubernetes-engine/sandbox/) for a second layer of defense between containerized workloads on Google Kubernetes Engine (GKE)
* Persist storage to containers
* Hold full databases in the cluster
* GKE runs using [Container-Optimized-OS](https://cloud.google.com/container-optimized-os/)
* Integrating with [Google Container Registry](https://cloud.google.com/container-registry/) makes it easy to store and access your private Docker images.


## Side notes
- Each 'node' is basically a Compute Vm instance
