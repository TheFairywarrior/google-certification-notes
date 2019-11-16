# Live Migration
Compute Engine offers live migration to keep your virtual machine instances running even when a host system event occurs, such as a software or hardware update. Compute Engine live migrates your running instances to another host in the same zone rather than requiring your VMs to be rebooted. This allows Google to perform maintenance that is integral to keeping infrastructure protected and reliable without interrupting any of your VMs.

Live migration keeps your instances running during:

* Regular infrastructure maintenance and upgrades.
* Network and power grid maintenance in the data centers.
* Failed hardware such as memory, CPU, network interface cards, disks, power, and so on. This is done on a best-effort basis; if a hardware fails completely or otherwise prevents live migration, the VM crashes and restarts automatically and a hostError is logged.
* Host OS and BIOS upgrades.
* Security-related updates, with the need to respond quickly.
* System configuration changes, including changing the size of the host root partition, for storage of the host image and packages.

## How does the live migration process work?
When Google migrates a running VM instance from one host to another, it moves the complete instance state from the source to the destination in a way that is transparent to the guest OS and anyone communicating with it. There are many components involved in making this work seamlessly, but the high-level steps are illustrated [here](https://cloud.google.com/compute/images/live-migration.svg)

The process begins with a notification that VMs need to be evicted from their current host machine. The notification might start with a file change indicating that a new BIOS version is available, a hardware operation scheduling maintenance, or an automatic signal from an impending hardware failure.

Google's cluster management software constantly watches for these events and schedules them based on policies that control the data centers, such as capacity utilization rates and the number of VMs that a single customer can migrate at once.

After a VM is selected for migration, Google provides a notification to the guest that a migration is imminent. After a waiting period, a target host is selected and the host is asked to set up a new, empty "target" VM to receive the migrating "source" VM. Authentication is used to establish a connection between the source and the target.

There are three stages involved in the VM’s migration:

* **During pre-migration brownout**:
    * the VM is still executing on the source, while most state is sent from the source to the target.
    * The time spent in pre-migration brownout is a function of the size of the guest memory and the rate at which pages are being changed.
* **During blackout**:
    * which is a very brief moment when the VM is not running anywhere, the VM is paused and all the remaining state required to begin running the VM on the target is sent
* **During post-migration brownout**:
    * the VM executes on the target VM. The source VM is present and might provide supporting functionality for the target VM. For example, until the network fabric has caught up with the new location of the target VM, the source VM provides forwarding services for packets to and from the target VM.

Finally, the migration is complete and the system deletes the source VM. You can see that the migration took place in your VM logs.

* Google continuously tests live migration with a very high level of scrutiny.
* We generate both active and passive failures for each component.

## Live migration and GPUs
Instances with GPUs attached cannot be live migrated. They must be set to terminate and optionally restart. Compute Engine offers a 60 minute notice before a VM instance with a GPU attached is terminated. To learn more about these maintenance event notices, read Getting live migration notices.

To learn more about handling host maintenance with GPUs, read [Handling host maintenance](handling_host_maintenance.md)on the GPUs documentation.


## Live migration for preemptible instances
You cannot configure a preemptible instances to live migrate. The maintenance behavior for preemptible instances is always set to TERMINATE by default, and you cannot change this option. It is not possible to set the automatic restart option for preemptible instances, but you can manually restart preemptible instances again after they are preempted.

If you need to change your instance to no longer be preemptible, detach the boot disk from your preemptible instance and attach it to a new instance that is not configured to be preemptible. You can also create a snapshot of the boot disk and use it to create a new instance without preemptibility.


