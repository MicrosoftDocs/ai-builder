---
title: AI Builder credit assignment, consumption and overage
description: Learn about credit management in AI Builder.
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.date: 08/30/2023
ms.author: antode
ms.reviewer: angieandrews
---

# AI Builder Credit Management Overview

Access to AI Builder features within an environment require AI Builder credits.

AI Builder credits come with some specific user licenses, but mostly from AI Builder Capacity add-on. See [Get entitlement to AI Builder credits](/#get-entitlement-to-ai-builder-credits)

Once acquired, credits can be allocated (aka assigned) to specific environment, or left at tenant level.  See [Make credits available for an environment ](/#Make-credits-available-for-an-environment)

Once an environment has access to credits, AI Builder features are enabled in this environment.

Some AI Builder actions consume credits. see [AI Builder Credit Consumption](/#AI-Builder-Credit-Consumption)

Credit consumption can be monitored. see [Monitor usage](/#monitor-usage)

In an environment, when consumption exceeds available credits, environment is in overage and some features are progressively blocked. Purchase of new credits and/or reassignment need to happen. see [Overage](/#overage)

AI Builder credits can also come from AI Builder trial. In that case, they are linked to the user and don't need to be allocated. see [AI Builder Trial](/#AI-Builder-Trial)

## Get entitlement to AI Builder credits

First, you need to be entitled to some AI Builder capacity. This can be through one of the following paid capacities.

Some Microsoft products like Power Apps per app plan, Power Apps per user plan, and Power Automate Premium (previously Power Automate per user with attended RPA) plan include some AI Builder capacity. Your environment admin can check entitlement in Power Platform admin center by following the instructions in [Capacity add-ons](/power-platform/admin/capacity-add-on). When this amount isn't enough, you need to complete it with one or more AI Builder capacity add-ons.

To purchase the AI Builder credit add-on in the Microsoft 365 admin center:

1. In the admin center, select **Billing** >  [Purchase services](https://go.microsoft.com/fwlink/p/?linkid=868433).
    You need to be the billing administrator of your tenant to access this page.

1. On the **Purchase services** page, do the following steps:

    1. Search for **AI Builder**.
    1. Select **Details** of the **AI Builder Capacity add-on** tile
    1. Follow the purchase process.
       

### Entitlement through AI Builder trial
Entitlement can be through a trial. Credits are then linked to a user. Trials are available only when there's no paid capacity within the tenant.
In case of a trial, there is no need of allocating credits to an environment.
Trials can be used in any environment. 
A trial brings 200K credits and is valid 30 days.
Once credits are consumed, AI Builder models are blocked for this user.
At the end of the 30 days, a trial can be renewed, and user receives another 200K credits. Renewal is only allowed for a limited number of times.

## AI Builder Credit Consumption
The following list isn't all-inclusive and preview scenarios don't consume credits.

|AI Builder Studio  |Power Apps  |Power Automate  |
|---------|---------|---------|
| Train an object detection model.<br/><br/>Perform a **Quick test** on a trained object detection and document processing model.<br/><br/>Use custom documents, images or text to **try out** prebuilt models when using the tiles in the 'Explore' section.<br/><br/>Batch runs of the prediction and trainable category classification models for each row to be predicted.  | Select...<br/><br/>**Scan a business card** with the business card reader.<br/><br/>**Analyze** with the document processor.<br/><br/>**Detect** with the object detector.<br/><br/>**+ New image** with the text recognizer.<br/><br/>**Use an action** bound to an AI Builder model through [Power Fx](powerfx-in-powerapps.md).  |Run a flow using any of the actions inside the **AI Builder** category.<br/><br/>Run the generic action **Perform a bound action** of Dataverse on the entity AI Models and action name **Predict**.   |

Each AI Builder model has a different credit consumption mechanism. To perform an assessment, go to the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) or obtain the full details in the [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130).

## Make credits available for an environment 

By default, the credits are unallocated and available as a pool on the tenant, which can be used on any environment. 

As an administrator, you'll assess which environments must consume AI Builder credits. Use the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) to define how many predictions will happen in a monthly period on each one and assess the credits to allocate.

Allocation happens in Power Platform admin center: in Resources > Capacity > Summary tab, select "Assign to an environment" in the upper-left menu bar

To learn more about how to allocate credits in the Power Platform admin center, go to [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

The administrator can block the use of unallocated credits through a tenant setting in Power Platform admin center: AI Builder credit/allow users to consume unassigned credits. By default, this setting is enabled. When disabled, only environments with allocated credits have access to AI Builder features.
See [Tenant settings](/power-platform/admin/tenant-settings)

> [!NOTE]
> This is how administrators stay in control of *where* AI is used in their organization and, with the role assignments described in [Roles and security in AI Builder](security.md#roles), *who* is using it.


## Monitor usage

As an administrator, you have access to a [consumption report](administer-consumption-report.md) that provides the AI credits consumption on a chosen period per environment. This will allow you to fine-tune the credits allocation, which can be updated at any time.
This also allows to check the consumption level of an environment for current month, by adding all consumptions of this environment.

Administrators also can access the [AI Builder Activity](activity-monitoring.md) page in the Power Automate portal, showing all predicts made against the AI Builder models in that environment.


## Overage

When browsing AI Builder pages in Power Apps or Power Automate portal, you might get this notification: **You’ve consumed all of your AI Builder credits. Contact your administrator to get more capacity**. This means the monthly consumption is higher than the available credits. (at environment or tenant level)

To get details on your environment allocation, check [Make credits available for an environment ](/#Make-credits-available-for-an-environment) section in this document.
To get details on your environment consumption, check [Monitor usage](/#monitor-usage) section in this document. 



If your environment has no more capacity, you need to provide capacity to your environment. To do this, reallocate existing capacity (from the tenant or environment level). Alternatively, you can purchase more capacity and make it available to your environment.

To help estimate the required add-on capacity based on your estimated consumption, use the [AI Builder calculator](https://powerapps.microsoft.com/en-us/ai-builder-calculator/).



## Allocate capacity

When a tenant has purchased AI Builder capacity, corresponding credits are by default unallocated and available as a pool on the tenant. In this state, credits can be used on any environment.

The administrator can restrict usage by allocating all credits to specific environments. The administrator can also reserve some capacity to an environment by allocating a number of credits to this environment.

To learn how to allocate capacity in [Power Platform admin center](https://admin.powerplatform.microsoft.com/), go to [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

To learn details on how to manage AI Builder capacity, go to [Manage capacity](administer.md#manage-capacity).

## Capacity Overuse

When an environment consumption exceeds its credit allocation, the following functions begin to fail:

- Create a model or a new version of a model.

- Run a model in Power Apps or in a Power Automate flow.

- Scheduled model run or retrain.
  - Some scenarios allow scheduled run or retrain, which is configured on the model settings panel. These scheduled tasks fail when you exceed capacity.

Only limited overage is allowed. To continue using AI Builder when you exceed capacity, purchase the AI Builder add-on capacity, and allocate it to your environment.

## Preview features

AI Builder features that are in preview release status are free to use. You don't need to obtain a license to use AI Builder preview features.

## AI Builder licenses FAQ

### How many AI Builder credits are consumed for each operation?

Each AI Builder capability consumes service credits at a different rate. You can check the consumption rates in the [Microsoft Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130) in the **AI Builder capacity add-on** section.

### My Power Automate flow or my Power App fails in AI Builder with an error message that contains one of the following. How do I unblock it?

- **EntitlementNotAvailable**
- **NoCapacity**
- **QuotaExceeded**
- **No capacity was found**
- **Credit usage exceeds allocation**

You need to check entitlement allocation of your environment. If there's no allocation, and no allocation at the tenant level, [allocate capacity](administer-licensing.md#allocate-capacity) to the environment or tenant level from other environments or by [purchasing AI Builder add-on](administer-licensing.md#purchase-ai-builder-capacity).

If there are AI Builder credits allocated or available at tenant level, compare the amount with the [AI Builder consumption report](administer-consumption-report.md).
Then [allocate additional capacity](administer-licensing.md#allocate-capacity) eventually by [purchasing the AI Builder add-on](administer-licensing.md#purchase-ai-builder-capacity).

### Where can I see credit usage for this month?

Get details on your environment consumption by checking the [AI Builder consumption report](administer-consumption-report.md). It gives the amount of consumption per day per user per environment.
Adding all the consumptions of the current month of a specific environment gives you the monthly consumption of this environment.

### When is credit usage count reset? Is it based on license acquisition date?

Credit usage is counted on a monthly basis, starting the first day of each month. It's not based on the license acquisition date. Credit usage of an environment shouldn't exceed the credit allocation.  

### What happened to the remaining capacity at the end of the month? Can it be used the following month?

No, unused capacity isn't carried over to the next month. Credit usage is counted on a monthly basis and reset on first day of the month. Available capacity is based on allocated capacity.

### I exceeded my trial capacity. What can I do?

- You can [purchase AI Builder Add On](administer-licensing.md#purchase-ai-builder-capacity)  and [allocate capacity](administer-licensing.md#allocate-capacity) to your environment

- You can wait for your trial to expire, then extend your trial: this adds new capacity.

- You can also share your existing model with another user who still has active trial with capacity.

### What happens after my trial license expires?

After your AI Builder trial license expires, or if you exceed capacity:

- Your models aren't deleted.

- You have to [purchase AI Builder Add-On](administer-licensing.md#purchase-ai-builder-capacity) to continue using your AI models.

- An administrator must [allocate AI Builder capacity](administer-licensing.md#allocate-capacity) to any environment where you want to use AI Builder.

- You can't create or modify AI Builder models, and no new inference is possible when the trial expires if you don't purchase a license.

- You can also extend your trial, but only for a limited number of times.

### What happens to my data and models when my AI Builder trial expires?

Data and models are deleted only when the environment is deleted.

### Where can I find more information about trial environments?

To learn more, go to [About trial environments](/power-platform/admin/trial-environments).

### Can I block users in my organization from signing up for an AI Builder trial?

Any individual can try out the features of AI Builder for 30 days and incur no costs to your company. This option is available to any user in a tenant and can't be disabled by an admin. Once your company purchases some AI credits (for example, through capacity add-ons or inclusion in some licenses), trials aren't proposed to users anymore.

### What can I do with the 5,000 AI credits included in the per user plan with attended RPA?

Each user license grants you 5,000 credits, allowing you to assess the capabilities in AI Builder. For instance, you could use these credits to extract data from a few documents with [document processing](form-processing-model-overview.md) or perform hundreds of basic OCR extractions with [text recognition](prebuilt-text-recognition.md).

### What happens if a user turns on/off AI Builder per user capacity add-on license?

Some user licenses include seeded AI Builder credits. For example, the Power Apps per user license includes 500 seeded AI Builder credits. If **AI Builder capacity per user add-on** isn't selected, the 500 AI Builder credits are still added to the total number of AI Builder credits owned at your tenant level and can be used.

### Where can I learn more about license management in Power Apps and Power Automate?

Learn more about licenses and license management in Power Apps in [About licensing and license management](/power-platform/admin/wp-license-management).

### See also

- [Microsoft Power Apps and Power Automate Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [AI Builder licensing FAQ](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you](https://powerapps.microsoft.com/ai-builder-calculator/)
- [AI Builder consumption report](administer-consumption-report.md)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
