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

# Customizing access for hybrid workloads
{: #tutorial-hybrid}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

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
1. Select **Individual users** and the IT infrastructure engineers that need access. Then, click **Add to profile**.
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
{: #next-step-order}

Prepare your data center and order {{site.data.keyword.IBM_notm}} {{site.data.keyword.powerSys_notm}} Private Cloud. For more information, see [Ordering on-premises infrastructure for your hybrid cloud]()
