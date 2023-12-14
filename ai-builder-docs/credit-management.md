---
title: AI Builder licensing and credit management
description: Learn about licensing and credit management in AI Builder.
author: Antoine2F
contributors:
  - jkom1
  - - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.date: 09/19/2023
ms.author: jelenak
ms.reviewer: angieandrews
---

# AI Builder licensing and credit management

Access to AI Builder features within an environment requires AI Builder credits.

AI Builder credits come with some specific user licenses, but mostly from AI Builder capacity add-on. To learn more, go to [Get entitlement to AI Builder credits](credit-management.md#get-entitlement-to-ai-builder-credits).

Once acquired, credits can be allocated (also known as assigned) to a specific environment, or left at the organization (tenant) level. For more information, go to [Make credits available for an environment](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits).

Once an environment has access to credits, AI Builder features are enabled in this environment.

Some AI Builder actions consume credits. To learn more, go to [AI Builder credit consumption](#ai-builder-credit-consumption) in this article.

Credit consumption can be monitored. To learn more, go to [Monitor usage](#monitor-usage) in this article.

In an environment, when consumption exceeds available credits, the environment is in overage and some features are progressively blocked. Purchase of new credits and/or reassignment needs to happen. To learn more, go to [Overage](#overage) in this article.

AI Builder credits can also come from AI Builder trial. In that case, they're linked to the user and don't need to be allocated. To learn more, go to [AI Builder trial](ai-builder-trials.md).

## Get entitlement to AI Builder credits

First, you need to be entitled to some AI Builder capacity. Entitlement can happen through one of the following paid capacities.

- Some Microsoft products like Power Apps per app plan, Power Apps per user plan, and Power Automate Premium (previously Power Automate per user with attended RPA) plan include  AI Builder capacity. Your environment admin can check entitlement in Power Platform admin center by following the instructions in [Capacity add-ons](/power-platform/admin/capacity-add-on). When this number isn't enough, you need to complete it with one or more AI Builder capacity add-ons.

- Main source of credits is AI Builder credit add-on that you can purchase in the Microsoft 365 admin center:

1. In the admin center, select **Billing** > [Purchase services](https://go.microsoft.com/fwlink/p/?linkid=868433).
    You need to be the billing administrator of your organization (tenant) to access this page.

1. On the **Purchase services** page, do the following steps:

    1. Search for **AI Builder**.
    1. Select **Details** of the **AI Builder Capacity add-on** tile
    1. Follow the purchase process.

### Number of AI Builder credits by license

The following table explains the rules for number of credits per license.

|License|Number of credits|Rules|
|-|-|-|
|AI Builder add-on (T1, T2, T3)|1,000,000|None.|
| Power Apps Premium |500| Maximum = 1,000,000 credits per tenant.|
| Power Apps per app |250| Maximum = 1,000,000 credits per tenant. Per app licenses purchased before November 2022 don't include any credits.|
| Power Automate Premium |5,000| Maximum = 1,000,000 credits per tenant.\*|
| Power Automate Process |5,000| Maximum = 1,000,000 credits per tenant.|
| Power Automate Hosted RPA add-on |5,000| Maximum = 1,000,000 credits per tenant.\*|
| Power Automate Unattended RPA add-on |5,000| Maximum = 1,000,000 credits per tenant.\*|
|Dynamics 365 F&O|20,000| Maximum = 20,000 credits per tenant. |

\*This maximum isn't enforced yet.

### Entitlement through AI Builder trial

Entitlement can be through a trial. Credits are then linked to a user. Trials are available only when there's no paid capacity within the organization (tenant).

In a trial, there's no need of allocating credits to an environment. Trials can be used in any environment. A trial brings 200,000 credits and is valid 30 days.

Once credits are consumed, AI Builder models are blocked for this user.
At the end of the 30 days, a trial can be renewed, and user receives another 200,000 credits. Renewal is only allowed for a limited number of times.

To learn more, go to [AI Builder trial](ai-builder-trials.md).

## Make credits available for an environment: allocated and unallocated credits

By default, the credits are unallocated (also known as unassigned) and available as a pool on the organization (tenant), which can be used on any environment.

As an administrator, you assess which environments must consume AI Builder credits. Use the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) site to estimate how many predictions happen in a monthly period on each one and assess the credits to allocate.

Allocation happens in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) when you select **Resources** > **Capacity** > **Summary** tab, and then select **Assign to an environment** in the upper-left menu.

### Block use of unallocated credits

The administrator can block the use of unallocated credits through an organization (tenant) setting in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/). To do this, remove the check from the **Allow users to consume unassigned credits** checkbox.

:::image type="content" source="media/credits.png" alt-text="Screenshot of the option to allow users to consume unassigned credits in Power Platform admin center.":::

By default, this setting is enabled. When disabled, only environments with allocated credits have access to AI Builder features.

To learn more, go to [Tenant settings](/power-platform/admin/tenant-settings).

> [!NOTE]
> This is how administrators stay in control of *where* AI is used in their organization and, with the role assignments described in [Roles and security in AI Builder](security.md#roles), *who* is using it.

To learn more about how to allocate credits in the Power Platform admin center, go to [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

## Monitor usage

As an administrator, you can view your overall credit consumption in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in the **Resources** > **Capacity** > **Summary** tab.  

The **Allocation bar** and the **Consumption bar** display the number of **allocated** credits and **consumed** credits out of the total number of **purchased** credits.

:::image type="content" source="media/credit-management/ppac-consumption.png" alt-text="Screenshot of the overall AI Builder credit consumption in the Power Platform admin center.":::

Credit extensions aren't counted in *purchased* credits.

Administrators also have access to a [consumption report](administer-consumption-report.md) that has the following features:

- Provides the AI credits consumption on a chosen period per environment.
- Allows you to fine-tune the credits allocation, which can be updated at any time.
- Allows administrators to check the consumption level of an environment for the current month by adding all consumptions of this environment.

Administrators also can access the [AI Builder Activity](activity-monitoring.md) page in the Power Automate portal, showing all predicts made against the AI Builder models in that environment.

### AI Builder credit consumption

The following list presents AI Builder actions consuming credits. It isn't all-inclusive and preview scenarios don't consume credits.

|AI Builder Studio  |Power Apps  |Power Automate  |
|---------|---------|---------|
| Train an object detection model.<br/><br/>Perform a **Quick test** on a trained object detection and document processing model.<br/><br/>Use custom documents, images or text to **try out** prebuilt models when using the tiles in the 'Explore' section.<br/><br/>Batch runs of the prediction and trainable category classification models for each row to be predicted.  | Select...<br/><br/>**Scan a business card** with the business card reader.<br/><br/>**Analyze** with the document processor.<br/><br/>**Detect** with the object detector.<br/><br/>**+ New image** with the text recognizer.<br/><br/>**Use an action** bound to an AI Builder model through [Power Fx](powerfx-in-powerapps.md).  |Run a flow using any of the actions inside the **AI Builder** category.<br/><br/>Run the generic action **Perform a bound action** of Dataverse on the entity AI Models and action name **Predict**.   |

Each AI Builder model has a different credit consumption mechanism. To perform an assessment, go to the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) site or obtain the full details in the [Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?linkid=2085130).

## Overage

When browsing AI Builder pages in Power Apps or Power Automate portal, you might get this notification: **You've consumed all of your AI Builder credits. Creating, editing and viewing is blocked. Contact your administrator to get more capacity**. This notification means the monthly consumption of your environment is higher than the available (at environment or organization -tenant- level) credits.

Monthly consumption is computed from first day of the month and is refreshed on a daily basis.
  
Available credits are the assigned credits if credits have been assigned to the environment, or the unassigned credits if no credit has been assigned to the environment.  

### Simple overage

As soon as monthly consumption is higher than the available credits, creating and editing models is blocked.

- On a prebuilt models tile, you can open the tile but can't test or select **Use in Apps or Flow**.
- On a new custom models tile, you can't select **Customize your model** to start a new model.
- On an existing model, you can't view, quick test, or edit properties. You can only delete model.

As long as overage isn't important, AI Builder models continue to run and consume credits. We allow some level of overage consumption&mdash;similar to a grace period&mdash;to avoid blocking business processes.

### Important overage

When monthly consumption becomes higher than the available credits by a large margin, running models in flows and apps is blocked. In this state, AI Builder actions fail with `EntitlementNotAvailable` `QuotaExceeded` error codes. In flow editor, remediation panel displays **All AI Builder credits in this environment have been consumed**.

To get details on your environment allocation, check [Make credits available for an environment ](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits) section in this document.
To get details on your environment consumption, check [Monitor usage](credit-management.md#monitor-usage) section in this article.

If your environment has no more capacity, you need to provide capacity to your environment:  reallocate existing capacity from the organization (tenant) or environment level. Alternatively, you can purchase more capacity and make it available to your environment.

To help estimate the required add-on capacity based on your estimated consumption, use the [AI Builder calculator](https://powerapps.microsoft.com/en-us/ai-builder-calculator/).

### Request credit extension

In the case of simple or important overage, and when additional purchase and/or reallocation of credit can't be done in a timely manner, we allow makers in the AI Builder portal and admins in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home) to request a free credit extension.

Selecting **Request extension** in the overage banner in the AI Builder page or [Power Platform admin center](https://admin.powerplatform.microsoft.com/home) performs following actions:
- Send an email to Power Platform admins.
- Add 200,000 free extension credits for the current month.

These free temporary credits can't be allocated or assigned and can be used directly by any environment in overage after 10 minutes.
In some cases, you may still see the overage banners although extension credits have already unblocked your Models.

Depending on the level of overage, these 200,000 credits may not be enough. They can be requested multiple times, but the number of extension requests per month and per year is limited. Each request grants 200,000 credits and triggers an email. 

The purpose of these free credit extensions is to allow makers and admin to unblock themselves temporarily in case additional purchase and/or re-allocation can't be done in a timely manner. Customer shouldn't rely on credit extensions to cover repetitive overage. Repetitive overage must be managed with additional purchase and/or re-allocation.

## Preview features

AI Builder features that are in preview release status are free to use. You don't need to obtain a license to use AI Builder preview features.

## AI Builder licensing FAQ

### How many AI Builder credits are consumed for each operation?

Each AI Builder capability consumes service credits at a different rate. You can check the consumption rates in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130) in the **AI Builder capacity add-on** section.

### My Power Automate flow or my Power App fails in AI Builder with an error message that contains one of the following. How do I unblock it?

- **EntitlementNotAvailable**
- **NoCapacity**
- **QuotaExceeded**
- **No capacity was found**
- **Credit usage exceeds allocation**

You need to check entitlement allocation of your environment. If there's no allocation, and no allocation at the organization (tenant) level, [allocate capacity](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits) to the environment or organization (tenant) level from other environments or by [purchasing AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits).

If there are AI Builder credits allocated or available at organization (tenant) level, compare the number with the [AI Builder consumption report](administer-consumption-report.md).
Then [allocate more capacity](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits) eventually by [purchasing the AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits).

### I have seeded credits. How many add-ons should I buy to cover my need?

Credits coming from the AI Builder add-on (1,000,000 credits per add-on) and credits coming from licenses with seeded capacity (like Power Automate premium, which brings 5,000 credits) are gathered at the tenant level. They represent your entitlement.

**Example 1**

One (1) add-on + 5 Power Automate premium licenses gives 1,000,000+5*5,000 = 1,025,000 credits that you can assign and consume in any scenario.

**Example 2**

You have a scenario with 32,000 receipts to process each month with receipt processing.

32,000 receipts require 32 credits per receipt (exact rates are in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130)), so you have 1,024,000 credits.

> [!NOTE]
> The [AI Builder calculator](https://powerapps.microsoft.com/en-us/ai-builder-calculator/) doesn’t give the exact number of AI Builder credits. It gives the number of add-ons, which is needed to cover the need. Here, it proposes to buy two (2) add-ons (2,000,000 credits) to cover the 1,024,000 credits.

Supposing you own five (5) Power Automate premium licenses, you're covered with a single add-on:

One (1) add-on + 5 Power Automate premium licenses = 1,025,000 credits, which is greater than your estimated consumption of 1,024,000 credits.

### Where can I see credit usage for this month?

Overall organization (tenant) level credit consumption is available in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) in the **Resources** > **Capacity** > **Summary** tab. The Consumption bar displays the number of *consumed* credits out of the total of *purchased* credits.

The data is aggregated daily. Some data may be delayed; if so, the consumption bar shows all known consumption at the **Last updated** date in the tooltip box.

Get details on your environment consumption by checking the [AI Builder consumption report](administer-consumption-report.md). It gives the amount of consumption per day per user per environment.
Adding all the consumptions of the current month of a specific environment gives you the monthly consumption of this environment.

### How do I find out which model is using the most credits?

Once you have identified which environment consumes the most credits with the [AI Builder consumption report](administer-consumption-report.md), you can leverage the model consumption data in the Dataverse **AI Event** table of that environment, either through the Power Apps portal or through the [AI Builder Activity](activity-monitoring.md) page in Power Automate.

### How do I know the number of purchased credits of my organization (tenant)?

The [consumption bar and allocation bar](https://go.microsoft.com/fwlink/?linkid=2255314)  display the number of *purchased* credits.

Credits come from AI Builder add-ons and are also seeded in premium licenses like Power Automate Premium.

You can go to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) and select **Resources** > **Add-ons** > **Assign to an environment** to see the remaining AI Builder credits. It represents the purchased capacity which hasn't been allocated yet.

### When is credit usage count reset? Is it based on license acquisition date?

Credit usage is counted on a monthly basis, starting the first day of each month. It's not based on the license acquisition date. Credit usage of an environment shouldn't exceed the credit allocation.  

### What happened to the remaining capacity at the end of the month? Can it be used the following month?

No, unused capacity isn't carried over to the next month. Credit usage is counted on a monthly basis and reset on first day of the month. Available capacity is based on allocated capacity.

### What can I do with the 5,000 AI credits included in the per user plan with attended RPA?

Each user license grants you 5,000 credits, allowing you to assess the capabilities in AI Builder. For instance, you could use these credits to extract data from a few documents with [document processing](form-processing-model-overview.md) or perform hundreds of basic OCR extractions with [text recognition](prebuilt-text-recognition.md).

### What happens if a user turns on/off AI Builder per user capacity add-on license?

Some user licenses include seeded AI Builder credits. For example, the Power Apps per user license includes 500 seeded AI Builder credits. If **AI Builder capacity per user add-on** isn't selected, the 500 AI Builder credits are still added to the total number of AI Builder credits owned at your organization (tenant) level and can be used.

### Where can I learn more about license management in Power Apps and Power Automate?

Learn more about licenses and license management in Power Apps in [About licensing and license management](/power-platform/admin/wp-license-management).

### What are the differences between credit assignment and credit allocation?

Credit assignment and credit allocation are same concept. In documentation, we mainly use allocation. In product, we mainly use assignment.

- assignment = allocation
- assigned credits = allocated credits = environment credits
- unassigned credits = unallocated credits = organization (tenant) level credits

### What are the differences between allocated credits and unallocated credits?

When an organization (tenant) has purchased AI Builder capacity, corresponding credits are by default unallocated and available as a pool for the organization (tenant). In this state, credits can be used on any environment without assigned credits, unless admin blocks usage of unallocated credits using the ['AI Builder Credit'](#block-use-of-unallocated-credits) organization (tenant) setting.

The administrator can restrict usage by allocating all credits to specific environments or by blocking the usage of unallocated credits. They can reserve some capacity to an environment by allocating credits to this environment.

Environments with allocated credits only consume allocated credits. There's no automatic switch to unallocated credit consumption when in overage. Environments without allocated credits only consume unallocated credits.

To learn more, go to [Make credits available for an environment](#make-credits-available-for-an-environment-allocated-and-unallocated-credits) in this article.

To learn how to allocate capacity in [Power Platform admin center](https://admin.powerplatform.microsoft.com/), go to [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

### Is there a way to automatically consume organization (tenant) level credits once environment allocated credits are consumed?

No, credits either come from environment allocation or comes from organization (tenant) level unallocated credits but there's no automatic switch from environment credits to organization (tenant) credits.

As soon as environment has allocated credits, credits only come from environment credits.
If environment consumption is higher than allocated credits, then environment is in overage.

### How do you consider the 'large margin' to block model runs in important overage?

For an environment with allocated credits, we apply the ‘large margin’ when comparing allocated credits and consumed credits. We don't consider organization (tenant) level credits.
For an environment without allocated credits, we apply the ‘large margin’ when comparing unallocated credits and consumed credits.

- **Simple overage**: Limitation starts as soon as consumed credits are higher than available credits (no margin here) and only impacts maker experience. (creating/editing models)
- **Important overage**: Blocking AI Builder models in flows and apps only happens if overage is important. (large margin applies here)

### If an environment is in overage, do the limitations apply to all environments?

No. Limitations only apply to the environments in overage. Other environments, whether consuming environment assignment or organization (tenant) level credits won't be affected.

For example, if an environment has no allocated credit, and organization (tenant) level credits aren't all consumed, then editing and running of AI Builder functions is allowed for this environment. This remains true when other environments with assigned credits are in overage.

### Do you have FAQ about AI Builder trials?

Yes. To learn more, go to [AI Builder trial FAQ](ai-builder-trials.md#ai-builder-trial-faq).

### See also

- [AI Builder trial](ai-builder-trials.md)
- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in the calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
