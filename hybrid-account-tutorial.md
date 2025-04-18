---
copyright:
  years: 2024
lastupdated: "2024-09-19"

keywords: location management, locations, region

subcollection: hybrid-workloads
content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Setting up catalogs and locations for hybrid workloads
{: #tutorial-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you learn how to set up an account for managing hybrid workloads in {{site.data.keyword.Bluemix_notm}}. You set up a private catalog that includes only the services that users and applications need and define the locations that users can deploy workloads.
{: shortdesc}

Let's say that you're the Chief Technology Officer (CTO) of a retail company. Your current provider is ending support for the power-based systems that you're using to run your Enterprise Resource Planning (ERP) workloads. You come to {{site.data.keyword.IBM_notm}} for a solution and discover that you can get {{site.data.keyword.IBM_notm}} Power Systems Hardware installed in your data center and that it plugs in to the {{site.data.keyword.Bluemix_notm}} console for managing workload deployments, usage monitoring, and billing. You decide that you can run your core business logic on {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud while your front-end services and databases run on a virtual server on {{site.data.keyword.Bluemix_notm}}.

{{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud is on your premises, which is more secure. Running core business logic here uses the performance, security, and reliability of {{site.data.keyword.IBM}} Power Systems.

{{site.data.keyword.IBM_notm}} is a public cloud environment where the front-end services and databases can be easily scaled and managed. Public clouds are designed to handle large-scale and dynamic workloads, making them ideal for services that face external users and might need to scale up or down quickly.

## Before you begin
{: #before-hybrid}

Make sure that you are logged in as the account owner or a user with the Administrator role on all account management services or Administrator role on the IAM Identity Service. For more information, see [IAM Identity service](/docs/account?topic=account-account-services#identity-service-account-management).

## Setting the visibility of the {{site.data.keyword.Bluemix_notm}} catalog
{: #visibility-catalog-hybrid}
{: step}

To restrict user visibility to just products in a private catalog, turn off the {{site.data.keyword.Bluemix_notm}} catalog in the account. This way, users in your account can use the console to create only instances of products that you give them access to in a private catalog.

1. In the {{site.data.keyword.Bluemix_notm}}, go to **Manage > Catalogs > Settings**.
1. Set the **{{site.data.keyword.Bluemix_notm}} catalog** toggle to **Off**.

## Create a private catalog
{: #private-catalog-hybrid}
{: step}

A curated private catalog makes it easier for teams to find and deploy the resources that they need and can help avoid unnecessary resource usage.

In this scenario, infrastructure services such as {{site.data.keyword.powerSys_notm}} and Virtual Private Cloud (VPC) are needed for managing the infrastructure. Developer services such as Cloud Databases, Kubernetes Service, and DevOps toolchains are needed for the development team to build and deploy a retail application.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Create a catalog**.
1. Enter a name and description of your catalog.
1. Select **No products**  in your private catalog. For more information about how this setting affects visibility in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Go to **Available from IBM Cloud Catalog**.
1. Select **Manage filters** to customize which products are available. In the case of our example, select the following filters:
   1. **Category > Compute**
   1. **Category > Containers**
   1. **Category > Networking**
   1. **Category > Databases**
   1. **Category > Developer tools**
   1. Click **Update**.
   1. **Provider > IBM**
1. Click **Create**.

## Set workload deployment locations
{: #manage-location}
{: step}

Enforce deployment location restrictions and help ensure that all deployments comply with regulatory and business requirements. This restriction is important in hybrid cloud setups where teams are managing both on-premises and cloud-based workloads.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Locations**.
1. Allow deployments to **Satellite** locations or public locations in the United States. Use the following syntax: `kind:location | (country:us ^ public:true)`.

Allowing deployments to Satellite locations is necessary to deploy workloads on {{site.data.keyword.powerSys_notm}} on-premises. Restricting deployments to public locations in the United States helps ensure data sovereignty.

## Next steps
{: #next-step-access}

Next, set up access profiles for {{site.data.keyword.powerSys_notm}} administrators in your organization. For more information, see [Customizing access for hybrid workloads](/docs/hybrid-workloads?topic=hybrid-workloads-access-tutorial-hybrid).
