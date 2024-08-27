---
copyright:
  years: 2024
lastupdated: "2024-08-16"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}

# Best practices for hybrid cloud management
{: #bp-hybrid}

Review the following best practices for hybrid cloud management that can help ensure efficiency, security, and scalability across on-premises and cloud environments.
{: shortdesc}

What is the recommended base setup? Is there a DA for the depoloyment of some services?

## Leveraging cloud native services
{: #cloud-native}

Use cloud native services that are designed for hybrid architectures, like IBM Cloud Satellite for unified management across environments, IBM Cloud Pak for Data for integrated data management, and Power Virtual Server for seamless extension of on-premises IBM Power Systems to the cloud.

## Supporting multi-cloud
{: #multi-cloud}

Prioritize an infrastructure that supports integration with multiple cloud providers. {{site.data.keyword.Bluemix_notm}} supports a multi-cloud strategy with IBM Cloud Satellite, which allows consistent management across different clouds.

## Managing hybrid access
{: #hybrid-access}

Ensure that security policies are consistent across all environments by using IAM solutions that span on-premises and cloud resources.

## Unifying monitoring and management
{: #unify-hybrid}

Use a single platform to monitor and manage resources across on-premises and cloud environments. Leverage tools like IBM Cloud Satellite, which provides centralized management, monitoring, and control for hybrid environments

## Optimizing workloads
{: #optimize-workloads}

Monitor usage patterns and optimize workloads for performance and cost. Use Cost Analysis to analyze spending and identify inefficiencies. Classify and place workloads based on their requirements, like latency, data residency, compliance, or performance.

For more information on how enterprises can configure and govern {{site.data.keyword.Bluemix_notm}} at scale, see [Enterprise architecture](/docs/enterprise-account-architecture).
