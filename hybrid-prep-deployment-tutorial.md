---
copyright:
  years: 2024
lastupdated: "2024-08-30"

keywords: location management, locations, region

subcollection: hybrid-workloads
content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Preparing your on-premises environment for deployments
{: #tutorial-prep-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you set up a workspace. Then, you grant PowerVS access to other {{site.data.keyword.Bluemix}} services.

## Creating an {{site.data.keyword.bplong}} workspace for on-premises workloads
{: #schematics}
{: step}

Create a {{site.data.keyword.bpshort}} workspace in the location associated with the pod that is installed at your site by using the {{site.data.keyword.powerSys_notm}} dashboard.


1. Go to **Menu > Power Virtual Server > Workspaces** and click **Create a workspace**.
1. Select On-premises and choose the {{site.data.keyword.satelliteshort}} location that is associated with the pod. Click **Continue**.
1. Enter the workspace name and select a resource group.
1. Click **Create**.

## Creating a virtual server instance
{: #create-instance}
{: step}

Quickly deploy SAP, Red Hat OpenShift and other supported workloads. Detailed views of storage pool and host level.

1. Click the **Action icon > View virtual servers** on the workspace that you created.
1. Click **Create instance**.

For more information, see [Configuring a Power Virtual Server instance](/docs/power-iaas?topic=power-iaas-creating-power-virtual-server#configuring-instance).



## Integrating with {{site.data.keyword.Bluemix_notm}} services
{: #integrate-cloud}
{: step}

Grant PowerVS access to other {{site.data.keyword.Bluemix_notm}} services like {{site.data.keyword.cos_short}}, {{site.data.keyword.Bluemix_notm}} Pak solutions, and key management services, such as {{site.data.keyword.keymanagementservicefull}} or {{site.data.keyword.hscrypto}}. This way, your on-premises workloads can benefit from cloud native services like backup, data management, and security.
