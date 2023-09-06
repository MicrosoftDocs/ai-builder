---
title: AI Builder Licensing and credit management
description: Learn about licensing and credit management in AI Builder.
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.date: 08/30/2023
ms.author: antode
ms.reviewer: angieandrews
---

# AI Builder Licensing and Credit Management

Access to AI Builder features within an environment requires AI Builder credits.

AI Builder credits come with some specific user licenses, but mostly from AI Builder Capacity add-on. See [Get entitlement to AI Builder credits](credit-management.md#get-entitlement-to-ai-builder-credits) section in this document.

Once acquired, credits can be allocated (aka assigned) to specific environment, or left at organization (tenant) level.  See [Make credits available for an environment ](/credit-management.md#Make-credits-available-for-an-environment--allocated-and-unallocated-credits) section in this document.

Once an environment has access to credits, AI Builder features are enabled in this environment.

Some AI Builder actions consume credits. see [AI Builder Credit Consumption](credit-management.md#ai-builder-credit-consumption) section in this document.

Credit consumption can be monitored. see [Monitor usage](credit-management.md#monitor-usage) section in this document.

In an environment, when consumption exceeds available credits, environment is in overage and some features are progressively blocked. Purchase of new credits and/or reassignment need to happen. see [Overage](credit-management.md#overage) section in this document.

AI Builder credits can also come from AI Builder trial. In that case, they are linked to the user and don't need to be allocated. see [AI Builder Trial](ai-builder-trials.md) documentation page.

## Get entitlement to AI Builder credits

First, you need to be entitled to some AI Builder capacity. This can be through one of the following paid capacities.

Some Microsoft products like Power Apps per app plan, Power Apps per user plan, and Power Automate Premium (previously Power Automate per user with attended RPA) plan include some AI Builder capacity. Your environment admin can check entitlement in Power Platform admin center by following the instructions in [Capacity add-ons](/power-platform/admin/capacity-add-on) documentation page. When this amount isn't enough, you need to complete it with one or more AI Builder capacity add-ons.

To purchase the AI Builder credit add-on in the Microsoft 365 admin center:

1. In the admin center, select **Billing** >  [Purchase services](https://go.microsoft.com/fwlink/p/?linkid=868433).
    You need to be the billing administrator of your organization (tenant) to access this page.

1. On the **Purchase services** page, do the following steps:

    1. Search for **AI Builder**.
    1. Select **Details** of the **AI Builder Capacity add-on** tile
    1. Follow the purchase process.
       

### Entitlement through AI Builder trial
Entitlement can be through a trial. Credits are then linked to a user. Trials are available only when there's no paid capacity within the organization (tenant).
In case of a trial, there is no need of allocating credits to an environment.
Trials can be used in any environment. 
A trial brings 200K credits and is valid 30 days.
Once credits are consumed, AI Builder models are blocked for this user.
At the end of the 30 days, a trial can be renewed, and user receives another 200K credits. Renewal is only allowed for a limited number of times.


See [AI Builder trial](ai-builder-trials.md) documentation page.


## Make credits available for an environment : allocated and unallocated credits

By default, the credits are unallocated (aka unassigned) and available as a pool on the organization (tenant), which can be used on any environment. 

As an administrator, you'll assess which environments must consume AI Builder credits. Use the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) site to define how many predictions will happen in a monthly period on each one and assess the credits to allocate.

Allocation happens in Power Platform admin center: in Resources > Capacity > Summary tab, select "Assign to an environment" in the upper-left menu bar

**The administrator can block the use of unallocated credits** through an organization (tenant) setting in Power Platform admin center: AI Builder credit/allow users to consume unassigned credits. By default, this setting is enabled. When disabled, only environments with allocated credits have access to AI Builder features.
See [Tenant settings](/power-platform/admin/tenant-settings) documentation page.


> [!NOTE]
> This is how administrators stay in control of *where* AI is used in their organization and, with the role assignments described in [Roles and security in AI Builder](security.md#roles) documentation page, *who* is using it.

To learn more about how to allocate credits in the Power Platform admin center, go to [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment) documentation page.

To learn details on how to manage AI Builder capacity, go to [Manage capacity](administer.md#manage-capacity) documentation page.


## AI Builder Credit Consumption
The following list presents AI Builder actions consuming credits.  
It isn't all-inclusive and preview scenarios don't consume credits.

|AI Builder Studio  |Power Apps  |Power Automate  |
|---------|---------|---------|
| Train an object detection model.<br/><br/>Perform a **Quick test** on a trained object detection and document processing model.<br/><br/>Use custom documents, images or text to **try out** prebuilt models when using the tiles in the 'Explore' section.<br/><br/>Batch runs of the prediction and trainable category classification models for each row to be predicted.  | Select...<br/><br/>**Scan a business card** with the business card reader.<br/><br/>**Analyze** with the document processor.<br/><br/>**Detect** with the object detector.<br/><br/>**+ New image** with the text recognizer.<br/><br/>**Use an action** bound to an AI Builder model through [Power Fx](powerfx-in-powerapps.md).  |Run a flow using any of the actions inside the **AI Builder** category.<br/><br/>Run the generic action **Perform a bound action** of Dataverse on the entity AI Models and action name **Predict**.   |

Each AI Builder model has a different credit consumption mechanism. To perform an assessment, go to the [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) site or obtain the full details in the [Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?linkid=2085130).


## Monitor usage

As an administrator, you have access to a [consumption report](administer-consumption-report.md) that provides the AI credits consumption on a chosen period per environment. This will allow you to fine-tune the credits allocation, which can be updated at any time.
This also allows to check the consumption level of an environment for current month, by adding all consumptions of this environment.

Administrators also can access the [AI Builder Activity](activity-monitoring.md) page in the Power Automate portal, showing all predicts made against the AI Builder models in that environment.


## Overage

When browsing AI Builder pages in Power Apps or Power Automate portal, you might get this notification: **You've consumed all of your AI Builder credits. Creating, editing and viewing is blocked. Contact your administrator to get more capacity**. This means the monthly consumption is higher than the available (at environment or organization -tenant- level) credits. 

### Simple Overage
As soon as monthly consumption is higher than the available credits, creating and editing models is blocked. 
- in prebuilt models tile, you can open the tile but cannot test or click on 'Use in Apps or Flow'
- in new custom models tile, you cannot click on 'customize your model' to start a new model
- in existing model, you cannot view, quick test, or edit properties. You can only delete model.

As long as overage is not important, AI Builder models will continue to run and consume credits. We allow some level of overage consumption as a grace period to avoid blocking business processes.

### Important Overage
When monthly consumption becomes higher than the available credits **by a large margin**, running models in flows and apps is blocked. 
- AI Builder actions will fail with 'EntitlementNotAvailable' 'QuotaExceeded' error codes. In flow editor, remediation panel displays "All AI Builder credits in this environment have been consumed"

To get details on your environment allocation, check [Make credits available for an environment ](credit-management.md#Make-credits-available-for-an-environment--allocated-and-unallocated-credits) section in this document.
To get details on your environment consumption, check [Monitor usage](credit-management.md#monitor-usage) section in this document. 

If your environment has no more capacity, you need to provide capacity to your environment. To do this, reallocate existing capacity from the organization (tenant) or environment level. Alternatively, you can purchase more capacity and make it available to your environment.

To help estimate the required add-on capacity based on your estimated consumption, use the [AI Builder calculator](https://powerapps.microsoft.com/en-us/ai-builder-calculator/) site.



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

You need to check entitlement allocation of your environment. If there's no allocation, and no allocation at the organization (tenant) level, [allocate capacity](credit-management.md#make-credits-available-for-an-environment--allocated-and-unallocated-credits) to the environment or organization (tenant) level from other environments or by [purchasing AI Builder add-on](credit-management.md/#get-entitlement-to-ai-builder-credits).

If there are AI Builder credits allocated or available at organization (tenant) level, compare the amount with the [AI Builder consumption report](administer-consumption-report.md).
Then [allocate additional capacity](credit-management.md#make-credits-available-for-an-environment--allocated-and-unallocated-credits) eventually by [purchasing the AI Builder add-on](credit-management.md/#get-entitlement-to-ai-builder-credits).

### Where can I see credit usage for this month?

Get details on your environment consumption by checking the [AI Builder consumption report](administer-consumption-report.md). It gives the amount of consumption per day per user per environment.
Adding all the consumptions of the current month of a specific environment gives you the monthly consumption of this environment.

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
These are same concept. In documentation, we mainly use allocation. In product, we mainly use assignment.
- assignment = allocation
- assigned credits = allocated credits = environment credits
- unassigned credits = unallocated credits = organization (tenant) level credits


### What are the differences between allocated credits and unallocated credits?

When an organization (tenant) has purchased AI Builder capacity, corresponding credits are by default unallocated and available as a pool for the organization (tenant). In this state, credits can be used on any environment without assigned credits, unless usage of unallocated credits is blocked by admin.

The administrator can restrict usage by allocating all credits to specific environments or by blocking the usage of unallocated credits. 
The administrator can  reserve some capacity to an environment by allocating a number of credits to this environment. 

Environments with allocated credits only consume allocated credits. There is no automatic switch to unallocated credit consumption when in overage.
Environments without allocated credits only consume unallocated credits. 

To learn more, go to [Make credits available for an environment](credit-management.md#Make-credits-available-for-an-environment--allocated-and-unallocated-credits) section in this document.

To learn how to allocate capacity in [Power Platform admin center](https://admin.powerplatform.microsoft.com/), go to [Allocate or change capacity in an environment](/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment) documentation page.


### Is there a way to automatically consume organization (tenant) level credits once environment allocated credits are consumed?

No, credits either come from environment allocation or comes from organization (tenant) level unallocated credits but there is no automatic switch from environment credits to organization (tenant) credits.
As soon as environment has allocated credits, credits only come from environment credits.
If environment consumption is higher than allocated credits, then environment is in overage.


### How do you consider the 'large margin' to block Model runs in case of environment and organization (tenant) level credits (important overage)?

For an environment with allocated credits, we will apply the ‘large margin’ when comparing allocated credits and consumed credits. We won’t consider organization (tenant) level credits.
•	**Simple overage**: Limitation will start as soon as consumed credits are higher than allocated credits (no margin here) and will only impact maker experience. (creating/editing models)
•	**Important overage**: Blocking AI Builder models in Flows and Apps will only happen if overage is important. (large margin applies here)


If an environment has no allocated credit, and organization (tenant) level credits are all consumed (**Simple overage**), then editing AI Builder functions will be blocked .
If an environment has no credit allocated, and consumption is much higher than organization (tenant) level credits (**Important overage**), then running AI Builder functions will be blocked. (in case of important overage)

### If an environment is in overage, do the limitations apply to all environments?

No,  limitations only apply to the environment(s) in overage. Other environments, whether consuming environment assignment or organization (tenant) level credits won't be affected.

For example, if an environment has no allocated credit, and organization (tenant) level credits are not all consumed, then editing and running of AI Builder functions will continue to work for this environment, even if other environments (with assigned credits) are in overage.

### Do you have FAQ about AI Builder trials?
Yes, they are [here](ai-builder-trials.md#ai-builder-trial-faq)

## See also
- [AI Builder trial](ai-builder-trials.md) documenation page
- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Power Platform licensing FAQ / AI Builder section](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in AI Builder Calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
