---
copyright:
  years: 2024
lastupdated: "2024-09-04"

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

Let's say that you're the Chief Technology Officer (CTO) of a retail company. Your current provider is ending support for the power systems that you're currently using to run your Enterprise Resource Planning (ERP) workloads. You come to {{site.data.keyword.IBM_notm}} for a solution and discover that you can get {{site.data.keyword.IBM_notm}} Power Systems hardware installed in your data center that plugs in to {{site.data.keyword.Bluemix_notm}} for managing workload deployments, usage monitoring, and billing. You sedice that you can run your core business logic on {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud while your front-end services and databases run on {{site.data.keyword.Bluemix_notm}}.

{{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud is a located on your premises, which is more secure. Running core business logic here uses the performance, security, and reliability of {{site.data.keyword.IBM}} Power Systems.

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

In this scenario, ABC services are needed for managing the infrastructure, and XYZ services are needed for development team to build a retail application.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Create a catalog**.
1. Enter a name and description of your catalog.
1. Select to exclude all products in the {{site.data.keyword.cloud_notm}} catalog in your private catalog. For more information about how this setting affects visibility in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Click **Create**.

## Set workload deployment locations
{: #manage-location}
{: step}

Enforce deployment location restrictions and help ensure that all deployments comply with regulatory and business requirements. This is important in hybrid cloud setups where teams are managing both on-premises and cloud-based workloads.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Locations**.
1. To allow deployment only to **On-premises**, **Power**, and **Satellite**, and Dallas use the following: `kind:location | cap:power | cap:on-prem | metro_id:dal`



## Next steps
{: #next-step-access}

Next, set up access profiles for developers and IT infrastructure engineers in your organization. For more information, see [Customizing access for hybrid workloads]().
