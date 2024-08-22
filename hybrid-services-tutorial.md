---
copyright:
  years: 2024
lastupdated: "2024-08-20"

keywords: location management, locations, region

subcollection: hybrid-workloads
content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Setting up your on-premises private cloud
{: #tutorial-services-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you learn how to estimate pricing, order and prepare for installing IBM {{site.data.keyword.powerSys_notm}} Private Cloud by using the {{site.data.keyword.Bluemix_notm}} console. You set up a Satellite locationmanages your PowerVS environment. Then, you grant PowerVS access to other {{site.data.keyword.Bluemix_notm}} services for an integrated hybrid cloud environment.
{: shortdesc}

## Before you begin
{: #before-priate cloud}

Review the documentation on preparing your site for physical hardware installation.
- [Prerequisites for installing the pod](/docs/power-iaas?topic=power-iaas-pre_installation_checklist)
- [Site readiness](/power-iaas?topic=power-iaas-site-readiness)
- [Site access requirements](/docs/power-iaas?topic=power-iaas-site-access-requirements)
- [Environmental requirements](/power-iaas?topic=power-iaas-environmental-requirements)
- [Power requirements](/docs/power-iaas?topic=power-iaas-power-requirements)
- [Network requirements](/docs/power-iaas?topic=power-iaas-network-requirements)
- [Planning your environment for Satellite locations](/docs/satellite?topic=satellite-infrastructure-plan)
- [Direct Link Connect prerequisites](/docs/direct-link?topic=direct-link-ibm-cloud-dl-connect-prerequisites)


## Estimating costs
{: #estimate}
{: step}

To generate an estimated price, use the [Power Virtual Server Estimate](/power/estimate) pricing tool.

1. Configure a pod by specifying your required compute and storage needs.
1. Then, select a term commitment.
1. Next, model metered consumption costs to understand projected rate.
1. Add the configuration to the estimator and export a PDF to view a total estimate.
1. Share your exported estimate with IBM to get a more detailed quote and possible discounts.

Leverage IBM professional services to accelerate project delivery.

## Ordering IBM {{site.data.keyword.powerSys_notm}} Private Cloud hardware
{: #ordering}
{: step}

[Purchasing services deployed on-premises](/docs/billing-usage?topic=billing-usage-service-comit).

After ordering, IBM teams reach out to coordinate floorspacwe planning, networking planning, and in other items in preparation for the delivery and setup.

## Creating a satellite location
{: #satellite}
{: step}

Create a Satellite location within your {{site.data.keyword.Bluemix_notm}} account to manage the lifecycle of your {{site.data.keyword.powerSys_notm}} Private Cloud pod. Satellite acts as a management layer that provides a single pane of glass for deploying and managing workloads across your on-premises and cloud environments.

For more information, see [Manually creating Satellite locations](/docs/satellite?topic=satellite-loc-manual-create).



## Recieving the hardware delivery
{: #recieve-hardware}
{: step}

IBM personnel take care of infrastructure setup and configuraiton.

- Registering the pod with IBM Cloud
-  Connecting to the client's IBM Cloud Satellite location
- Enabling the pod for usage

The commitment term begins and you can start viewing billing information on IBM Cloud. The pod is ready for workload deployments.

## Creating a schematics workspace for on-premisis workloads
{: #schematics}
{: step}

Create a schematics workspace in the location associated with the pod installed on-premises by using the PowerVS interface. Use out of the box images to jumpstart deployments for your 

1. Go to **Menu > Power Virtual Server > Workspaces** and click **Create a workspace**.
1. Select On-premises and choose the satellite location associated with the pod. Click **Continue**.
1. Enter the workspace name and select a resource group.
1. Click **Create**.

## Creating a virtual server instance
{: #create-instance}
{: step}

Quickly deploy SAP, Redhat Openshift and other supported workloads. Detailed views of storage pool and host level. 

1. Click the **Action icon > View virtual servers** on the workspace that you created.
1. Click **Create instance**.
1. 



## Integrating with {{site.data.keyword.Bluemix_notm}} services
{: #integrate-cloud}

Grant PowerVS access to other {{site.data.keyword.Bluemix_notm}} services like IBM Cloud Object Storage, IBM Cloud Pak solutions, and IBM Cloud Key Management Service (KMS). This way, your on-premises workloads can benefit from cloud-native services like backup, data management, and security.
