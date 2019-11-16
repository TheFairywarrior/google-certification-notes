# Regions and Zones

## Understanding Regions and Zones
[Full docs](https://cloud.google.com/compute/docs/regions-zones/)

Certain Compute Engine resources live in regions or zones. A region is a specific geographical location where you can run your resources. Each region has one or more zones. For example, the us-central1 region denotes a region in the Central United States that has zones us-central1-a, us-central1-b, us-central1-c, and us-central1-f.

[click here to view all zones](https://cloud.google.com/compute/docs/regions-zones/#available)

Resources that live in a zone are referred to as zonal resources. Virtual machine Instances and persistent disks live in a zone. To attach a persistent disk to a virtual machine instance, both resources must be in the same zone. Similarly, if you want to assign a static IP address to an instance, the instance must be in the same region as the static IP.

Putting recources in different zone helps to protect from hardware or software failures. Regional recources can be used by any recource in that region, zonal recources can also only access recources within the same zone. Basically some recources have to stay in their little box to be connected to eachother.

### Zones and Clusters
Compute Engine implements a layer of abstraction between zones and the physical clusters where the zones are hosted. A cluster represents a distinct physical infrastructure that is housed in a data center. Each cluster has independent software infrastructure, power, cooling, network, and security infrastructure, and includes a large pool of compute and storage resources.

* Zones are hosted in one or more clusters
* Compute Engine individually maps zones to clusters

Decoupling zones from clusters helps with scalibility and load balancing, as well as keeping the amount of zones managable.

## Choosing a Region and Zone
Choosing a region and zone is important for several reasons:
* Handling Failures:
    
    Distributing recources means that there are more points of failure before the system comes down. Meaning that if the one of the zones/regions is having an issue the services can still be run, with only a marginal reduction in effiency.

* Decreased NetWork Latency:
    Choosing a region/zone that is close to the customer means that they're data won't have to travel far to get between them and the server.

## Identyfying a Zone or Region

* **Regions**:
    * Collections of zones
    * Zones have high band width low latency connections to other zones within the same region
    * Try to choose regions close to the end user
* **Zones**:
    * A zone is an isolated location within a region. The fully-qualified name for a zone is made up of 'region'-'zone'

## Transparent maintenance
Google regularly maintains its infrastructure by patching systems with the latest software, performing routine tests and preventative maintenance, and generally ensuring that Google infrastructure is as fast and efficient as Google knows how to make it.
* All instances are configured so that these maintenance events are transparent to your applications and workloads.
* The running VMs are moved out of the way, but kept in the same zone, while maintenance is being performed.
* There are 2 options to move VMs:
    
    * [**Live Migrate:**](live_migrate.md)
    Compute Engine automatically migrates your running instance.
    * **Terminate and Reboot**: 
    Compute Engine automatically signals your instance to shut down, waits a short time for it to shut down cleanly, and then restarts it away from the maintenance event.

[More about setting instance scheduling options](setting_instance_sheduling_opetions.md)

## Zone Deprecation
It is never necessary to decommission an existing zone for a ground-up infrastructure refresh (power, cooling, network fabric, servers, etc.). Infrastructure refreshes are rare and zones typically run for three to five years between refreshes. These refreshes should be transparent to customers.

If it ever becomes necessary to deprecate a zone, Compute Engine will notify users well in advance of when it will go offline so you have ample time to move your virtual machine instances and workloads.

## Quotas
[Quotas page](https://console.cloud.google.com/iam-admin/quotas?_ga=2.74637650.-1169373855.1555318207)

Certain resources, such as static IPs, images, firewall rules, and VPC networks, have defined project-wide quota limits and per-region quota limits.