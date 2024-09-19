---
copyright:
  years: 2024
lastupdated: "2024-09-11"

keywords: location management, locations, region

subcollection: hybrid-workloads
content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Ordering on-premises infrastructure for your hybrid cloud
{: #tutorial-services-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

In this tutorial, you learn how to estimate pricing, order hardware, and prepare for installing {{site.data.keyword.IBM}} {{site.data.keyword.powerSys_notm}} Private Cloud. You set up an {{site.data.keyword.satellitelong}} location that manages your {{site.data.keyword.powerSys_notm}} environment while you wait for your hardware delivery.
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
1. Next, model metered consumption costs to understand the projected rate.
1. Add the configuration to the estimator and export a PDF to view a total estimate.
1. Share your exported estimate with IBM to get a more detailed quote and possible discounts.

Use IBM professional services to accelerate project delivery.

## Ordering IBM {{site.data.keyword.powerSys_notm}} Private Cloud hardware
{: #ordering}
{: step}

For more information, see [Purchasing infrastructure services deployed on-premises](/docs/billing-usage?topic=billing-usage-service-comit).

After your order is placed, {{site.data.keyword.IBM_notm}} teams contact you to coordinate floor space planning, networking planning, and other items in preparation for the delivery and setup.

## Creating a {{site.data.keyword.satelliteshort}} location
{: #satellite}
{: step}

Create a {{site.data.keyword.satelliteshort}} location within your {{site.data.keyword.Bluemix_notm}} account to manage the lifecycle of your {{site.data.keyword.powerSys_notm}} Private Cloud pod. {{site.data.keyword.satelliteshort}} acts as a connection back to {{site.data.keyword.Bluemix_notm}} that provides a single interface for deploying and managing workloads across your on-premises and cloud environments.

For more information, see [Manually creating {{site.data.keyword.satelliteshort}} locations](/docs/satellite?topic=satellite-loc-manual-create).

After you create this {{site.data.keyword.satelliteshort}} location, {{site.data.keyword.IBM}} manages the lifecycle of the {{site.data.keyword.satelliteshort}} location. The {{site.data.keyword.satelliteshort}} location that you create to connect to {{site.data.keyword.powerSys_notm}} Private Cloud is at no-cost.

## Receiving the hardware delivery
{: #recieve-hardware}
{: step}

{{site.data.keyword.IBM_notm}} service support representatives (SSRs) take care of infrastructure setup and configuration.

- Registering the pod with {{site.data.keyword.Bluemix_notm}}
- Connecting to your {{site.data.keyword.satelliteshort}} location
- Enabling the pod for usage

The commitment term begins and you can start viewing billing information on {{site.data.keyword.Bluemix_notm}}. The pod is almost ready for workload deployments.

## Next steps
{: #next-step-prep}

Next, [Prepare your on-premises environment for deployments](/docs/hybrid-workloads?topic=hybrid-workloads-tutorial-prep-hybrid).
