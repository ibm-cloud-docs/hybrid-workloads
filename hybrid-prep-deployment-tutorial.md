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

# Preparing your on-premises environment for deployments
{: #tutorial-prep-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you set up a workspace and virtual server instance to run your company's enterprise resource planning (ERP) workloads on-premises and other workloads on {{site.data.keyword.Bluemix_notm}}. These are the same steps that you would use to set up {{site.data.keyword.powerSys_notm}} in the cloud.
{: shortdesc}

## Create an {{site.data.keyword.bplong}} workspace
{: #schematics}
{: step}

Create a {{site.data.keyword.bpshort}} workspace in the location associated with the pod that is installed at your site by using the {{site.data.keyword.powerSys_notm}} dashboard.


1. Go to **Menu > {{site.data.keyword.powerSys_notm}} > Workspaces** and click **Create a workspace**.
1. Select On-premises and choose the {{site.data.keyword.satelliteshort}} location that is associated with the pod. Click **Continue**.
1. Enter the workspace name and select a resource group.
1. Click **Create**.

For more information, see [Creating a {{site.data.keyword.powerSys_notm}} workspace](/docs/power-iaas?topic=power-iaas-creating-power-virtual-server#creating-service).

## Create a virtual server instance
{: #create-instance}
{: step}

Create a virtual server instance that runs on your {{site.data.keyword.IBM}} Power Systems hardware on-premises, on which you plan to run your enterprise ERP workloads.



1. Click the **Action icon > View virtual servers** on the workspace that you created.
1. Click **Create instance**.

For more information, see [Configuring a {{site.data.keyword.powerSys_notm}} instance](/docs/power-iaas?topic=power-iaas-creating-power-virtual-server#configuring-instance).

## Deploying workloads on {{site.data.keyword.powerSys_notm}}
{: #integrate-cloud}
{: step}

After the {{site.data.keyword.powerSys_notm}} instance is up and running, you can deploy your workloads, such as applications or databases, onto the instance. You manage the {{site.data.keyword.powerSys_notm}} instance and the workloads running on it through the {{site.data.keyword.Bluemix_notm}} console or using the [Power Cloud API](/apidocs/power-cloud).



## Monitor performance
{: #monitor-hybrid}
{: step}

Use monitoring tools to oversee performance and how much capacity is allocated and available across all of your pods running on {{site.data.keyword.powerSys_notm}}, whether they are on-premises or in the cloud.

For more information, see [Monitoring metrics for IBM Power Virtual Server](/docs/power-iaas?topic=power-iaas-monitor-sysdig).



## Next steps
{: #next-steps-prep}
