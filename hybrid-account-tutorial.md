---
copyright:
  years: 2024
lastupdated: "2024-08-26"

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

In this tutorial, you learn how to set up an account for managing hybrid workloads by using the {{site.data.keyword.Bluemix_notm}} console. You set up a private catalog that includes only the services that account users and applications need and define the locations that users can deploy workloads. Then, you set up access profiles for developers and IT infrastructure engineers in your organization.
{: shortdesc}

Let's say that you are a retail company that wants to deploy a hybrid cloud application where the core business logic runs on {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud, while front-end services and databases run on {{site.data.keyword.Bluemix_notm}}.

{{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} is a private cloud, which is more secure, customizable, and on-premises. Running core business logic here uses the performance, security, and reliability of IBM Power Systems.

{{site.data.keyword.IBM_notm}} is a public cloud environment where the front-end services and databases can be easily scaled and managed. Public clouds are designed to handle large-scale and dynamic workloads, making them ideal for services that face external users and might need to scale up or down quickly.

## Before you begin
{: #before-hybrid}

Make sure that you are logged in as the account owner or a user with the Administrator role on all account management services or Administrator role on the IAM Identity Service. For more information, see [IAM Identity service](/docs/account?topic=account-account-services#identity-service-account-management).

## Setting the catalog visibility
{: #visibility-catalog-hybrid}
{: step}

Turn off users visibility of the {{site.data.keyword.Bluemix_notm}} catalog. Users in your account can use the console to create only instances of products that you give them access to in a private catalog.

1. In the {{site.data.keyword.Bluemix_notm}}, go to **Manage > Catalogs > Settings**.
1. Set the **{{site.data.keyword.Bluemix_notm}} catalog** toggle to **Off**.

## Create a private catalog
{: #private-catalog-hybrid}
{: step}

A curated private catalog makes it easier for teams to find and deploy the resources that they need and can help avoid unnecessary resource usage.

In a private catalog, you can enforce deployment location restrictions and help ensure that all deployments comply with regulatory and business requirements. This is important in hybrid cloud setups where teams are managing both on-premises and cloud-based workloads.

In this scenario, ABC services are needed for the infrastructure, and XYZ services are needed for dev team to build [retail] application.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud}} console, and click **Create a catalog**.
1. Enter a name and description of your catalog.
1. Select to exclude all products in the {{site.data.keyword.cloud_notm}} catalog in your private catalog. For more information about how this setting affects visibility in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Click **Create**.

## Assigning access and customizing platform experience
{: #tp-customize}
{: step}

The roles of an IT infrastructure engineer and a developer are distinct, but they might interact with the same resources for different purposes within the same account. Create separate trusted profiles for the IT infrastructure engineer and the development team to assign each persona the access that they need and customize their platform experience to do their job.

### IT infrastructure engineer
{: #it-tp}

The primary focus of the IT infrastructure engineer is helping ensure that the underlying infrastructure, both cloud and on-premises, runs smoothly, is secure, scalable, and available for other teams, like development.

To set up {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud and manage {{site.data.keyword.powerSys_notm}} instances, the IT infrastructure engineer needs the following roles and services:
- Administrator on {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}}
- Administrator on {{site.data.keyword.satellitelong_notm}}
- Administrator on {{site.data.keyword.dl_full_notm}}

To optimize and monitor resources once the infrastructure is in place, the IT infrastructure engineer needs the following roles and services:
- Administrator on monitoring tools and logs (Administator on X service)
- Administrator on compute resources to adjust them based on the application's performance ( Administrator on Kubernetes)


Complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM) > Trusted profiles** and click **Create**.
1. Enter the profile name `IT infrastructure` and the initials `IT`.
1. Enter a description for the profile, like ""
1. Select a color to represent this trusted profile and click **Continue**. Your users might have access to multiple trusted profiles in multiple accounts.
1. Select **Individual users**  and the IT infrastructure engineers that need access. Then, click **Add to profile**.
1. Click **Continue** and select **Access policy**.

### Developer
{: #dev-tp}

The primary focus of the developer is building, testing, and deploying the retail applications that run on the infrastructure set up by the IT infrastructure engineer.

To containerize, deploy, and scale applications on Kubernetes clusted running on {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}}, the developers need the following rolse and service:
- Writer on {{site.data.keyword.powerSys_notm}}
- Writer on Kubernetes
- Writer on CI/CD pipelines

Complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM) > Trusted profiles** and click **Create**.
1. Enter the profile name `IT infrastructure` and the initials `IT`.
1. Enter a description for the profile, like ""
1. Select a color to represent this trusted profile and click **Continue**. Your users might have access to multiple trusted profiles in multiple accounts.
1. Select **Individual users**  and the IT infrastructure engineers that need access. Then, click **Add to profile**.
1. Click **Continue** and select **Access policy**.



## Next steps
{: #next-steps-hybrid}

Prepare your data center and order {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud. For more information, see [Setting up your on-premises private cloud]()
