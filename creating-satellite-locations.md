---
copyright:
  years: 2024
lastupdated: "2024-06-13"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Creating a satellite location
{: #satellite_location}

The first step to getting started with Satellite is to create a Satellite location. A Satellite location is a representation of an environment in your infrastructure provider, such as an on-prem data center or cloud. Locations are made up of compute sources, called hosts, from separate zones of your backing infrastructure environment.

Creating satellite locations involves setting up additional instances of your infrastructure, services, or resources in different geographical regions to improve performance, availability, and redundancy. Once all the location filters are set in [Setting location filters for an account](/docs/hybrid-workloads?topic=hybrid-workloads-managing_locations), click **Create satellite location** to create a satellite location. 
{: shortdesc}
 
To create a satellite location, complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and select **Locations**.
1. Click **Create Satellite**
    Make sure you have all the prerequisites as mentioned in the [Overview](satellite?topic=satellite-locations#create-host-os) section. By default, creating satellite location uses On-premises and edge template.
    {: note}

1. Specify all the details like **Name**, **Tags**, **Resource group**, **Managed from**, **Red Hat CoreOS Support**, and **Object storage**
1. Review your **Total estimate cost** and click **Create location**. For more information, see [Manually creating satellite locations](/docs/satellite?topic=satellite-loc-manual-create).

Now, that your satellite location is created, you can configure your infrastructure by PaaS setup, attach hosts, create services, link endpoints, and Create storage configuration. For more information, see [Attaching on-prem hosts to your location](docs/satellite?topic=satellite-attach-hosts)

## Viewing resources that are deployed to a Satellite location
{: #viewing_resource}

### Refining your search results
{: #results} {: ui}

To get a clear view of resources deployed in specific Satellite locations, complete the following steps: 
1. On the Catalog page, click **Resource list**
1. Search for satellite locations in the **Location** filter. 
1. Enter the name of the satellite location, the satellite location and the respective region are selected to filter the resources. For example, type `satloc_dal_xyz` (`Dallas` region), the list of resources deployed in this location are displayed. 


### Searching with the CLI
{: #search-cli} {: cli}

Locations
The following examples can help you search for satellite location resources.
The geographical satellite location where the resource is created. The allowed values are, for example, `sgm-satellite-2q50`, `gm-on-prem-satellite`, etc.


### Search by using the API
{: #searching-api} {: api}

To search for resources, call The Global Search and Tagging - Search API. The following example searches for all resources with tag "project:myproject" attached.


