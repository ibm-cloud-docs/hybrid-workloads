---
copyright:
  years: 2024
lastupdated: "2024-06-13"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Creating satellite locations
{: #creating_satellitelocations}

Creating satellite locations involves setting up additional instances of your infrastructure, services, or resources in different geographical regions to improve performance, availability, and redundancy. 
{: shortdesc}
 
To create a satellite location, complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and select **Locations**.
1. Click **Create Satellite**
    Make sure you have all the prerequisites as mentioned in the [Overview](/docs/hybrid-workloads?topic=hybrid-workloads-locations) section. By default, creating satellite location uses On-premises and edge template.
    {: note}

1. Specify all the details like **Name**, **Tags**, **Resource group**, **Managed from**, **Red Hat CoreOS Support**, and **Object storage**
1. Review your **Total estimate cost** and click **Create location**. 

Now, that your satellite location is created, you can configure your infrastructure by PaaS setup, attach hosts, create services, link endpoints, and Create storage configuration. For more information, see [Attaching on-prem hosts to your location](docs/satellite?topic=satellite-attach-hosts)

## Viewing resources that are deployed to a Satellite location
{: #viewing_resource}


To get a clear view of resources deployed in specific Satellite locations, complete the following steps: 
1. Click the **Resource list**
1. Click the **Location** filter and seach for satellite locations

ibmcloud resource search 'region:satellite'

### Searching with the CLI
{: #search-cli}

The following examples can help you search for location resources.



### Search by using the API
{: #searching-api}

To search for resources, call The Global Search and Tagging - Search API. The following example searches for all resources with tag "project:myproject" attached.


