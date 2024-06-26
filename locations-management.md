---
copyright:
  years: 2024

lastupdated: "2024-06-26"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Managing workload deployment locations
{: #managing_locations}

An IBM Cloud Satellite location mirrors an environment within your infrastructure provider, whether it is an on-premises or cloud setting. These locations consist of compute resources known as hosts, which are housed either within your infrastructure provider's environment or locally. Once you have linked your hosts to a Satellite, power, or on-prem location, you can designate them for the location's control plane or utilize them to support your service workloads.
{: shortdesc}

## Before you begin
{: #before_begin}

If you are not a catalog admin in the account you are currently in, you will see a read-only version of it. However, if you are a catalog admin, you will have the ability to edit the filters. Editing the location filters for an account impacts the resources that users can view in the IBM Cloud catalog in the account. 

## Setting location filters for an account 
{: #location_filters}

To set the location filters, complete the following steps.
1. In the IBM console, go to **Manage** > **Catalog** > **Locations**.
1. Switch to an enterprise account. 
1. Select the account group by clicking **Change**. 
1. Specify the **Location type**. 
1. Specify the **Common filters**. 
1. Based on the selections, the **Allowed**, **Blocked**, and **Total** locations are displayed.  
1. Click **Save filter**.

### Filtering syntax
{: #filtering_syntax}

Filter locations allows you to view, search, and filter locations. It is most effective for straightforward location combinations or for grasping the workings of the filtering syntax. You can see how the advanced syntax develops through the toggles and filters in the search bar. You can perform either of the following to filter your locations: 
* Enter the syntax to filter locations. 
* Click **More filters** to refine your search based of the allow list. 
* Select the **Show inactive locations**, **Show blocked locations**, and **Show parent locations (geographies, countries, metros)** toggles. 

Multiple dimensions can be included while filtering a location/region. Hence, a syntax is used to define the combinations of these regions. The following syntax is used for filtering:
* `|` to designate OR 
* `^` to designate AND 
* `(,)` for grouping

#### Syntax to define regions
{: #define_syntax}

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

#### Multiple syntax 
{: #multiple_syntax}

| Example | Description |
|---------------|-------------|
| country:de,uk|id:bnpp | All regions in `de` or `uk` countries as well as (OR) region (id) `bnpp`| 
| geo_id:na^cap:name:power | any region in North America geography that has a (AND) power capability | 
{: caption="Table 2. Defining multiple syntax." caption-side="top"}  

For example, enter the location filter as `geo:na` and and select the **Show blocked locactions** toggle, and select the **metro** allowlist to view regions that are blocked. 

To view who made made changes to the filters, click the email to expand it and view the details in **Change logs**. 

## Creating a satellite location 
{: #satellite_location}

An IBM Cloud service capable of deployment in a Satellite location, like a Red Hat OpenShift cluster. The service is managed from the IBM Cloud region where your location is overseen, while you provide the infrastructure hosts to operate the service's resources at your site.

Creating satellite locations involves setting up additional instances of your infrastructure, services, or resources in different geographical regions to improve performance, availability, and redundancy. Once all the location filters are set in [Setting location filters for an account](/docs/hybrid-workloads?topic=hybrid-workloads-managing_locations), click **Create satellite location** to create a satellite location. For more information, see [Manually creating satellite locations](/docs/satellite?topic=satellite-loc-manual-create). 

## Viewing resources deployed to a satellite location 
{: #viewing_resources}

To view resources deployed to a satellite location, complete the following steps: 
1. 