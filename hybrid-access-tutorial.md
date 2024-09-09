---
copyright:
  years: 2024
lastupdated: "2024-09-09"

keywords: location management, locations, region

subcollection: hybrid-workloads
content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Customizing access for managing hybrid workloads
{: #access-tutorial-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you customize how users that manage workloads in a hybrid environment can view and access an account. In this scenario, a retail company wants to run their core business logic on {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} on-premises and run front-end services on {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

Create a trusted profile for the {{site.data.keyword.powerSys_notm}} administrator to grant them consistent access across on-premises and cloud envoronments and tailor their platform experience to their job role.

## Before you begin
{: #before-hybrid}

Make sure that you are logged in as the account owner or a user with the Administrator role on all account management services or Administrator role on the IAM Identity Service. For more information, see [IAM Identity service](/docs/account?topic=account-account-services#identity-service-account-management).

## Create a trusted profile
{: #it-tp}
{: step}

The primary focus of the {{site.data.keyword.powerSys_notm}} administrator is helping ensure that the underlying infrastructure, both cloud and on-premises, runs smoothly, is secure, scalable, and available for other teams.

Complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM) > Trusted profiles** and click **Create**.
1. Enter the profile name `IT infrastructure` and the initials `IT`.
1. Enter a description for the profile, like "Full access to deploy, configure, and manage virtual servers, storage, and networking components in both on-prem and cloud environments."
1. Select a color to represent this trusted profile and click **Continue**. Your users might have access to multiple trusted profiles in multiple accounts.
1. Select **Individual users** and select the {{site.data.keyword.powerSys_notm}} administrators that need access. Then, click **Add to profile**.

## Assign access
{: #it-access}
{: step}

To set up {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud and [manage {{site.data.keyword.powerSys_notm}} instances](/docs/power-iaas?topic=power-iaas-modifying-instance) across on-premises and cloud envoronments, the {{site.data.keyword.powerSys_notm}} administrator needs the following roles and services:

1. Click **Continue** and select **Access policy**.
1. Select the following role and service:
   - Service: Workspace for {{site.data.keyword.powerSys_notm}}
   - Resources: All resources
   - Roles and actions: Administrator
1. Click **Add**.

To optimize and monitor resources once the infrastructure is in place, the {{site.data.keyword.powerSys_notm}} administrator needs the following access:

1. Select the following role and service:
   - Service: {{site.data.keyword.mon_full_notm}}
   - Resources: All resources
   - Roles and actions: Editor
1. Click **Add**.
1. Click **Create**.

## Customize the console
{: #it-experience}
{: step}

After you click create, you can customize the console experience for the trusted profile.

1. Click **Console experience**.
1. Select URL for the landing page and input the {{site.data.keyword.powerSys_notm}} dashboard URL: https://cloud.ibm.com/power/overview.
1. Deselect the Manage navigation items. The {{site.data.keyword.powerSys_notm}} administrator doesn't need to manage account settings, access, or billing. Removing these menu items helps users complete tasks specific to their job role.
1. Select the private catalog that you created in [Setting up catalogs and locations for hybrid workloads](/docs-draft/hybrid-workloads?topic=hybrid-workloads-tutorial-hybrid). This way, the {{site.data.keyword.powerSys_notm}} administrator can provision only resources that they have access to from the curated list of services that you created.
1. Click **Save**.

## Next steps
{: #next-step-order}

Now that access is set up for the {{site.data.keyword.powerSys_notm}} administrator, prepare your data center and order {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud. For more information, see [Ordering on-premises infrastructure for your hybrid cloud](/docs-draft/hybrid-workloads?topic=hybrid-workloads-tutorial-services-hybrid).
