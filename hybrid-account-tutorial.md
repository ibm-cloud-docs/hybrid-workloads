---
copyright:
  years: 2024
lastupdated: "2024-08-16"

keywords: location management, locations, region

subcollection: hybrid-workloads
content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Setting up an account for hybrid workloads
{: #tutorial-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you learn how to set up an account for managing hybrid workloads by using the {{site.data.keyword.Bluemix_notm}}. You set up a private catalog that includes only the services that account users and applications need and define the locations that users can deploy workloads. Then, you set up an access profiles for developers and IT infrastructure engineers in your organization.
{: shortdesc}

## Before you begin
{: #before-hybrid}

- Make sure that you are logged in as the account owner or a user with the Administrator role on all account management services or Administrator role on the IAM Identity Service. For more information, see [IAM Identity service](/docs/account?topic=account-account-services#identity-service-account-management).

## Setting the catalog visibility
{: #visibility-catalog-hybrid}
{: step}

Turn off users visibility of the {{site.data.keyword.Bluemix_notm}} catalog. Users in your account can use the console to create only instances of products that you give them access to a private catalog.

1. In the {{site.data.keyword.Bluemix_notm}}, go to **Manage > Catalogs > Settings**.
1. Set the **{{site.data.keyword.Bluemix_notm}} catalog** toggle to **Off**.

## Create a private catalog
{: #private-catalog-hybrid}
{: step}

A curated private catalog makes it easier for teams to find and deploy the resources that they need and can help avoid unnecessary resource usage.

In a private catalog, you can enforce deployment location restrictions and ensure that all deployments comply with regulatory and business requirements. This is important in hybrid cloud setups where teams are managing both on-prem and cloud-based workloads.

In this scenario, ABC services are needed for the infrastructure, and XYZ services are needed for dev team to build [healthcare chatbot] applicaiton.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Create a catalog**.
1. Enter a name and description of your catalog.
1. Select to exclude or include all products in the {{site.data.keyword.cloud_notm}} catalog in your private catalog. For more information about how this affects visibility in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Click **Create**.

## Customizing access and platform experience
{: #tp-customize}
{: step}

The roles of an IT infrastructure engineer and a developer are distinct, but they might interact with the same resources for different purposes within the same account.

### IT infrastructure engineer
{: #it-tp}

The primary focus of the IT infrastructure engineer is ensuring that the underlying infrastructure, both cloud and on-premises, runs smoothly, is secure, scalable, and available for other teams, like development.

- Needs access to PowerVS Private Cloud (Network, PVM Instance, Cloud Snapshot, Cloud Storage Volume)
- Needs access to CEPH as a service?
- Needs access to private catalog

### Developer
{: #dev-tp}

The primary focus of the developer is building, testing, and deploying applications or services that run on the infrastructure set up by the IT infrastructure engineer.

- Needs access to cloud resources and maybe limited access to the data stored on-premises?
- Needs access to private catalog

## Next steps
{: #next-steps-hybrid}
{: step}

- Order Power and Storage (Tutorial)
   - Preparing your datacenter for PowerVS Private Cloud (Link to)
   - Creating Satellite locations
- Monitoring, event notifications, billing (Tutorial)

----

## Questions

- Are we in a stand-alone account or an enterprise with multiple accounts (how is the enterprise structured? Is there a sinlge account for serivices deployed on-prem or do on-prem services live in the same account as cloud resources?)
- Multiple private catalogs?
- Is the developer also the IT infrastructure person? It's still a good idea to have separate trusted profiles for the two separate "jobs" even if it's the same person

----


