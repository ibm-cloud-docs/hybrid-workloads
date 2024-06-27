---
copyright:
  years: 2024
lastupdated: "2024-06-13"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}

# Viewing resources in a Satellite location
{: #viewing_resource}

You can search for resources from anywhere in the {{site.data.keyword.cloud}} console. Enter the resource or tag in the search field from the console menu bar. You can also use the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI) to search across your resources. The CLI searches for distributed applications and service instances across satellite locations.
{: shortdesc}

## Refining your search results
{: #results} 
{: ui}

To get a clear view of resources deployed in specific Satellite locations, complete the following steps: 
1. On the Catalog page, click **Resource list**
1. Search for satellite locations in the **Location** filter. 
1. Enter the name of the satellite location, the satellite location and the respective region are selected to filter the resources. For example, type `satloc_dal_xyz` (`Dallas` region), the list of resources deployed in this location are displayed. 


## Searching with the CLI
{: #search-cli} 
{: cli}

The following examples can help you search for satellite location resources.
The geographical satellite location where the resource is created. The allowed values are, for example, `sgm-satellite-2q50`, `gm-on-prem-satellite`, etc.


## Search by using the API
{: #searching-api} 
{: api}

To search for resources, call The Global Search and Tagging - Search API. The following example searches for all resources with tag "project:myproject" attached.
