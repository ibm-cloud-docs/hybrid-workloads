---
copyright:
  years: 2024

lastupdated: "2024-06-27"

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

Enables you to apply specific settings to add or remove locations from the resource deployment allow list. 

To set the location filters, complete the following steps:

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Catalog** > **Locations**.
1. Switch to the enterprise account, if applicable, by using the account switcher.
   1. Keep the account group scoped to None to apply your allowlist to the entire enterprise.
   1. Click **Change** to scope the allowlist to a specific account group.

   To view and manage locations for an individual account, you must switch to that account.
   {: note}

1. Specify the **Location type**.
   - Enable Public if you want to deply worklods to only IBM Cloud locations.
   - Enable Private if your data centers are all deployed locally (verify if this is what private means).
1. Specify the **Common filters**. Filtering based on these categories allow you to setup the configurations to govern how these different types of filters interact with each other or with external entities ensuring security and efficiency.  
   - Enable **On premises** to view resources hosted locally within an organization's physical infrastructure, typically within their premises.
   - Enable **Power** to access resources hosted on power capabilities. 
   - Enable **Satellite** to view your satellite locations. 
1. Based on the **Location type** and **Common filters** selections, the account group that is scoped to None is assigned to an account. Additionally, the counts for **Allowed**, **Blocked**, and **Total** locations are also diaplyed.

   Click **Revert to saved filter** if you don't want to save your changes. You can use this to explore all available deployment locations.
   {: tip}

1. Click **Save filter**.

1. Filter the allowed deployment locations.
   * Enable applicable toggles.
   * Click **More filters** to refine your search.
   * Manually query the filter locations search bar.

   The toggles and filters are most effective for straightforward location combinations or for grasping the workings of the filtering syntax. You can see how the advanced syntax develops in the search bar as you adjust the toggles and filters. You can customize the search bar to integrate the selected options with filter toggles in various ways, utilizing filtering syntax. To create more complex combinations, see [Filtering syntax](/docs-draft/hybrid-workloads?topic=hybrid-workloads-managing_locations#filtering_syntax).
   {: note}

1. When you click **More filters**, a set of additional filters are displayed. These filters allow you to refine your search criteria. 
   For example, if you specify Dallas in the **Metro** allow list, then all the locations for Dallas is displayed. Similarly, if you specify a particular country in the **Country** allow list, then all the locations for the specified country will only be displayed.

### Filtering syntax
{: #filtering_syntax}

Multiple dimensions can be included while filtering a location/region. Hence, a syntax is used to define the combinations of these regions. The following syntax is used for filtering:
* `|` to designate OR
* `^` to designate AND
* `(,)` for grouping

#### Selecting different dimensions
{: #define_dimensions}

| Example                          | Description                                    |
|----------------------------------|------------------------------------------------|
| geo_id:na,ap                     | Geography ID is either `na` or `ap`            |
| country_id:us,ca,jp              | Country ID is either `us`, `ca`, or `jp`       |
| id:a,b,c                         | Region ID is either `a`, `b`, `c`              |
| metro_id:dal                     | Metro ID is `dal`                              |
| cap:on-prem                      | capability on-prem is registered               |
| cap:power.status:order-placement | power capability with `order-placement` status |
| tag:t1                           | Regions with a `t1` tag                        |
| public:false                     | private regions                                |
| kind:region                      | [Group of one or more zones](/docs/overview?topic=overview-locations#table-mzr)|
{: caption="Table 1. Describing the different dimensions for filter section." caption-side="top"}

#### Pre-determined syntax for filtering different dimensions
{: #predefined_syntax}


| Example                  | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| country:de,uk\id:bnpp    | All regions in `de` or `uk` countries as well as (OR) region (id) `bnpp`|
| geo_id:na^cap:name:power | any region in North America geography that has a (AND) power capability |
{: caption="Table 2. Specifying syntax to filter different dimensions." caption-side="top"}

For example, enter the location filter as `geo:na` and and select the **Show blocked locactions** toggle, and select the **metro** allowlist to view regions that are blocked.

To view who made made changes to the filters, click the email to expand it and view the details in **Change logs**.
