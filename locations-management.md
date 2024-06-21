---
copyright:
  years: 2024
lastupdated: "2024-06-20"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Managing workload deployment locations
{: #managing_locations}

An IBM Cloud service that can be deployed in a Satellite location, such as a Red Hat OpenShift cluster. The service is administered from the IBM Cloud region where your location is managed, while you supply the infrastructure hosts to operate the service's resources at your site. Managing geographical regions where cloud service providers host their data centers. These locations are equipped to ensure the reliability, security, and performance of cloud services. Managing these locations allows to meet the needs of customers and ensure seamless operation of cloud services.
{: shortdesc}

While managing accounts, you can select between an enterprise account and a standard account. This allows you to specify the account group and the impacted sub-accounts or account groups. 

## Before you begin
{: #prerequisites}


## Setting location filters for an account 
{: #location_filters}

Editing a location allow list impacts resource provisioning. 
 
To set the location filters, complete the following steps.
1. In the IBM console, go to **Manage** > **Catalog** > **Locations**.
1. Switch to an enterprise account. 
1. Select the account group by clicking **Change**. 
1. Specify the **Location type**. 
1. Specify the **Common filters**. 
1. Based on the selections, the **Allowed**, **Blocked**, and **Total** locations are displayed.  
1. Click **Save filter**.
1. Click **Create satellite location**.

### Filtering syntax
{: #filtering_syntax}

Filter locations allows you to view, search, and filter locations. You can either perform one of the following to filter your locations: 
* Enter the syntax to filter locations. 
* Click **More filters** to refine your search based of the allow list. 

Multiple dimensions can be included while filtering a location/region. Hence, a syntax is used to define the combinations of these regions. The following syntax is used for filtering:
* `|` to designate OR 
* `^` to designate AND 
* `(,)` for grouping

Syntax to define regions

| Example | Description |
|---------------|-------------|
| geo_id:na,ap | Geography ID is either `na` or `ap` | 
| country_id:us,ca,jp | Country ID is either `us`, `ca`, or `jp` | 
| id:a,b,c | Region ID is either `a`, `b`, `c` |
| metro_id:dal | Metro ID is `dal` |
| cap:on-prem | capability on-prem is registered |
| cap:power.status:order-placement | power capability with `order-placement` status | 
| tag:t1 | Regions with a `t1` tag | 
| public:false | private regions |
| kind:region| [Group of one or more zones](https://github.ibm.com/ibmcloud/content-catalog/blob/master/design-docs/regions.md#filters){: external}.
{: caption="Table 1. Defining syntax." caption-side="top"}  

Multiple syntax 

| Example | Description |
|---------------|-------------|
| country:de,uk|id:bnpp | All regions in `de` or `uk` countries as well as (OR) region (id) `bnpp`| 
| geo_id:na^cap:name:power | any region in North America geography that has a (AND) power capability | 
{: caption="Table 2. Defining multiple syntax." caption-side="top"}  

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





