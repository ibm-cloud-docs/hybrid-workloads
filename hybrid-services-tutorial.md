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

To generate an estimated price, use the [Power Virtual Server Estimate](/power/estimate) pricing tool.

## Ordering IBM {{site.data.keyword.powerSys_notm}} Private Cloud hardware
{: #ordering}

[Purchasing services deployed on-premises](/docs/billing-usage?topic=billing-usage-service-comit)

## Creating a satellite location
{: #satellite}

Create a Satellite location within your {{site.data.keyword.Bluemix_notm}} account to manage the lifecycle of your {{site.data.keyword.powerSys_notm}} Private Cloud pod. Satellite acts as a management layer that provides a single pane of glass for deploying and managing workloads across your on-premises and cloud environments.

## Integrating with {{site.data.keyword.Bluemix_notm}} services
{: #integrate-cloud}

Grant PowerVS access to other {{site.data.keyword.Bluemix_notm}} services like IBM Cloud Object Storage, IBM Cloud Pak solutions, and IBM Cloud Key Management Service (KMS). This way, your on-premises workloads can benefit from cloud-native services like backup, data management, and security.
