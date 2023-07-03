# Azure regions, availability zones, and region pairs  
A region is a geographical area on the planet that contains at least one but potentially multiple datacenters that are nearby and networked together with a low-latency network. Azure intelligently assigns and controls the resources within each region to ensure workloads are appropriately balanced.  
##### Important  
> Some services or VM features are only available in certain regions, such as specific VM sizes or storage types. There are also some global Azure services that don't require you to select a particular region, such as Azure Active Directory, Azure Traffic Manager, and Azure DNS.

## Azure availability zones  

Availability zones are physically separate datacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking. An availability zone is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.  

![изображение](https://github.com/devSLAVUS/AZ-305/assets/91405914/b2b49a19-046a-4e4b-90f2-a9668fc31e8f)  


Not every region has support for availability zones. For an updated list, see Regions that support availability zones in Azure.
https://learn.microsoft.com/en-us/azure/reliability/availability-zones-service-support  


use availability zones to run mission-critical applications and build high-availability into your application architecture. Keep in mind that there could be a cost to duplicating your services and transferring data between zones.  

Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. The following categories of Azure services support availability zones:

    Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
    Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
    Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages and region-wide outages.
