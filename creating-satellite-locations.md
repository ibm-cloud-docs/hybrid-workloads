---
copyright:
  years: 2024
lastupdated: "2024-06-13"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Creating satellite locations
{: #creating_locations}

Creating satellite locations involves setting up additional instances of your infrastructure, services, or resources in different geographical regions to improve performance, availability, and redundancy. 
{: shortdesc}
 
To create a satellite location, complete the following steps:
1. Specify the name of the satellite location. 
1. Specify the user tags. 
1. Select the resource group. 
1. Select the region from where the satellite is managed. This allows you to have a better network coverage. 
1. Specify the zones to keep your apps up and running for a high availability of your network, even after a partial or full site failure. For more informtion, see [High availablity and recvovery](/docs/satellite?topic=satellite-ha)
1. Select either **Red Hat CoreOS enabled** or **RHEL hosts only** that impacts host operating system support, footprint, and the availability of extra features. For more information, see [Deciding whether to enable Red Hat CoreOS support for your location](/docs/satellite?topic=satellite-infrastructure-plan#enable-coreos-loc)
1. Click **Create**. 
