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

As an administrator on the Catalog service, you can manage the list of allowed workload deployment locations for your account or an enterprise. Deploy your apps to the location that is nearest to your customers to achieve low application latency and to meet data residency requirements.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} has a resilient global network of region and data center locations. Deploying your workload to the public cloud might not always align with your latency or data residency needs, especially for industries with strict data governance regulations. You can leverage {{site.data.keyword.Bluemix_notm}} Satellite to create a representation of an environment in your infrastructure provider, such as an on-prem data center or cloud, and manage your hybrid deployment locations from a single pane of glass in the {{site.data.keyword.Bluemix_notm}} console.

## Before you begin
{: #before_begin}

- You must be an Administrator on the Catalog service to edit the location filters. Otherwise, the page is read-only.
- Editing the location filters for an account, enterprise, or account group affects the resources that users can view in the {{site.data.keyword.Bluemix_notm}} catalog in those accounts.

## Setting location filters for an account
{: #location_filters}

To set the location filters, complete the following steps:

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Catalog** > **Locations**.
1. Switch to the enterprise account, if applicable, by using the account switcher.
   1. Keep the account group scoped to None to apply your allowlist to the entire enterprise.
   1. Click **Change** to scope the allowlist to a specific account group.

   To view and manage locations for an individual account, you must switch to that account.
   {: note}

1. Filter the allowed deployment locations.
   * Enable applicable toggles.
   * Click **More filters** to refine your search.
   * Manually query the filter locations search bar.

   The toggles and filters are most effective for straightforward location combinations or for grasping the workings of the filtering syntax. You can see how the advanced syntax develops in the search bar as you adjust the toggles and filters. To create more complex combinations, see [Filtering syntax](/docs-draft/hybrid-workloads?topic=hybrid-workloads-managing_locations#filtering_syntax).
   {: tip}

1. Specify the **Location type**.
   - Enable Public if you want to deply worklods to only IBM Cloud locations.
   - Enable Private if your data centers are all deployed locally (verify if this is what private means).
1. Specify the **Common filters**.
   - Enable On premises if
   - Enable Power if
   - Enable Satellite to view your satellite locations
1. Based on the selections, the **Allowed**, **Blocked**, and **Total** locations are displayed.

   Click **Revert to saved filter** if you don't want to save your changes. You can use this to explore all available deployment locations.
   {: tip}

1. Click **Save filter**.

### Filtering syntax
{: #filtering_syntax}

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
1. This is the step we created for testing.
