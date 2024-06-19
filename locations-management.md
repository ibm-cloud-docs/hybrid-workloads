---
copyright:
  years: 2024
lastupdated: "2024-06-13"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Managing locations
{: #managing_locations}

Managing geographical regions where cloud service providers host their data centers. These locations are equipped to ensure the reliability, security, and performance of cloud services. Managing these locations allows to meet the needs of customers and ensure seamless operation of cloud services.
{: shortdesc}

As an administrator, 

## Before you begin
{: #prerequisites}


## Setting location filters for an account 
{: #location_filters}
 
To set the location filters, complete the following steps.
1. In the IBM console, go to **Manage** > **Catalog** > **Locations**.
1. Switch to an enterprise account. 
1. Select the account group by clicking **Change**. 
1. Specify either **Public** or **Private** based on your requirement:
1. Specify either **On premises** or **Satellite** based on your requirement:
    * **On premise**: 
    * **Satellite**: 
1. Click **Save filter**.
1. Click **Create satellite location**.

### Filtering syntax
{: #filtering_syntax}



## Creating a satellite location 
{: #satellite_location}

Creating satellite locations involves setting up additional instances of your infrastructure, services, or resources in different geographical regions to improve performance, availability, and redundancy. 

To create a satellite location, complete the following steps:
1. Specify the name of the satellite location. 
1. Specify the user tags. 
1. Select the resource group. 
1. Select the region from where the satellite is managed. This allows you to have a better network coverage. 
1. Specify the zones to keep your apps up and running for a high availability of your network, even after a partial or full site failure. For more informtion, see [High availablity and recvovery](/docs/satellite?topic=satellite-ha).
1. Select either **Red Hat CoreOS enabled** or **RHEL hosts only** that impacts host operating system support, footprint, and the availability of extra features. For more information, see [Deciding whether to enable Red Hat CoreOS support for your location](/docs/satellite?topic=satellite-infrastructure-plan#enable-coreos-loc).
1. Click **Create**. For more information, see Satellite less technical content 

## Viewing resources deployed to a satellite location 
{: #viewing_resources}

To view resources deployed to a satellite location, complete the following steps: 
1. 
 Resources 
 exlain how the filtering works 





