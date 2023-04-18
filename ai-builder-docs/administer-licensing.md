---
title: AI Builder licensing
description: Learn about licensing in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.custom: intro-internal
ms.date: 04/13/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# AI Builder licensing

You might receive this notification when you sign in: **You’ve consumed all of your AI Builder credits. Contact your administrator to get more capacity**. If you get this message, read this article to learn how to increase capacity and get details and FAQs on licensing.

:::image type="content" source="media/consumed-all-credits-image-capacity-notification-a.png" alt-text="Screenshot of the AI Builder credits banner notification.":::

## Prerequisite to set up an environment ready for AI Builder

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you need a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment.

## Get entitlement to AI Builder capacity

First, you need to be entitled to some AI Builder capacity. This can be through one of the following paid capacities.

- Purchase an AI Builder capacity add-on, or

- Purchase other licenses offering some seeded capacity.

This can be through a trial. The capacity is then linked to a user. Trials are available only when there's no paid capacity within the tenant.

Then, a tenant administrator has to allocate part or all of the purchased capacity to the environment where you want to use AI Builder.

It's also possible to leave part or all of the purchased capacity unallocated, at the tenant level. In this case, all environments without allocated capacity can consume these tenant-level unallocated credits.

## Check the consumption level of an environment

When browsing AI Builder pages in Power Apps or Power Automate portal, you might get this notification: **You’ve consumed all of your AI Builder credits. Contact your administrator to get more capacity**. This means the monthly consumption is higher than the allocated capacity.

To get details on your environment allocation, check environment details in [Administer AI Builder, Manage capacity](administer.md#manage-capacity).

To get details on your environment consumption, check the [AI Builder consumption report](administer-consumption-report.md).

When you add all the consumptions of the current month of a specific environment, you'll get the monthly consumption of this environment.

If your environment has no more capacity, you need to provide capacity to your environment. To do this, reallocate existing capacity (from the tenant or environment level). Alternatively, you can purchase additional capacity and make it available to your environment.

To help estimate the required add-on capacity based on your estimated consumption, use the [AI Builder calculator](https://powerapps.microsoft.com/en-us/ai-builder-calculator/).

## Purchase AI Builder capacity

Some Microsoft products like Power Apps per app plan, Power Apps per user plan, and Power Automate per user plan with attended RPA include some AI Builder capacity. Your environment admin can check entitlement in Power Platform admin center by following the instructions in [Capacity add-ons](/power-platform/admin/capacity-add-on). When this amount isn't enough, you need to complete it with one or more AI Builder capacity add-ons.

To purchase the AI Builder credit add-on in the Microsoft 365 admin center:

1. In the admin center, select **Billing** >  [Purchase services](https://go.microsoft.com/fwlink/p/?linkid=868433).
    You need to be the billing administrator of your tenant to access this page. <!--I don't have perms to test.-->

1. On the **Purchase services** page, do the following steps:

    1. Search for **AI Builder**.
    1. Select **Details** of the **AI Builder Capacity add-on** tile
    1. Follow the purchase process.

## Allocate capacity

When a tenant has purchased AI Builder capacity, corresponding credits are by default unallocated and available as a pool on the tenant. In this state, credits can be used on any environment.

The administrator can restrict usage by allocating all credits to specific environments.The administrator can also reserve some capacity to an environment by allocating an amount of credits to this environment.

To learn how to allocate capacity in [Power Platform admin center](https://admin.powerplatform.microsoft.com/), go to [Allocate or change capacity in an environment] (/power-platform/admin/capacity-add-on#allocate-or-change-capacity-in-an-environment).

To learn details on how to manage AI Builder capacity, go to [Manage capacity](administer.md#manage-capacity).

## Capacity Overuse

When an environment consumption exceeds its credit allocation, the following functions will begin to fail:

- Create a model or a new version of a model.

- Run a model in Power Apps or in a Power Automate flow.

- Scheduled model run or retrain.
  - Some scenarios allow scheduled run or retrain, which is configured on the model settings panel. These scheduled tasks will fail when you exceed capacity.

Only limited overage is allowed. To continue using AI Builder when you exceed capacity, purchase the AI Builder add-on capacity, and allocate it to your environment.

## Trial licenses

To get started using AI Builder, use premium features for a limited time with a [trial license](https://powerapps.microsoft.com/ai-builder/). Alternatively, use preview features without obtaining a license at all.

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you can start your AI Builder trial after you have a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment.

> [!NOTE]
> You can't start an AI Builder trial if you have AI Builder credits already on your tenant by purchasing a capacity add-on or through other products.

### Benefits of a trial license

An [AI Builder trial license](https://powerapps.microsoft.com/ai-builder/) enables you to use AI Builder features for free during the 30-day trial period.

What you get an AI Builder trial license:

- Create and use AI models in any environment (trial or production).

- Store your AI model results in Dataverse.

- Use AI model in your apps, flows, and more.

### Activate an AI Builder trial license

1. Sign in to	[Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).

1. Select **AI Builder** > **Explore**.

1. (If requested) Select **Create a database**, and then choose a currency and language.

1. Select **Create my database**.

    :::image type="content" source="media/administer-licensing/create-db.png" alt-text="Screenshot of the 'New database' screen. ":::

1. Refresh the **Explore** page.
1. At the top of the screen, select **Start free trial**.

    :::image type="content" source="media/administer-licensing/start-free-trial.png" alt-text="Screenshot of Start free trial.":::

> [!NOTE]
> Your AI Builder trial license is applicable at the user level, not the environment level.You can use your trial license on multiple environments. Another user would have to start their own trial or paid license to use your models in any environment.

### After the trial expires

Your AI Builder trial license expires after 30 days.

To continue using AI Builder, purchase AI Builder add-on capacity and allocate AI Builder capacity to your environments. You may also be able to extend the trial period. Trials can be extended a limited number of times. Extension can only occur after the trial expires.

To renew your AI Builder trial license, sign in to Power Apps or Power Automate, select **AI Builder** > **Explore**, and then select **Extend trial** in the banner on the top.

### Trial capacity

An AI Builder trial license includes a limited amount of AI Builder capacity. You use this capacity when running or training models.

If you exceed your AI Builder capacity, you’ll receive an over-capacity notification. These notifications appear as banners in AI Builder pages or when using the model.

The following functions aren't available when you exceed capacity:

- Create a model or a new version of a model.

- Run a model within Power Apps or in a Power Automate flow.
  - You can still share your model with another user. They can run it using their own AI Builder capacity if they have a valid trial.

- Scheduled model run or retrain.
  - Some scenarios allow scheduled run or retrain, which is configured on the model settings panel. These scheduled tasks will fail when you exceed capacity. Therefore, data won’t be refreshed, and the model won’t be retrained.

To continue using AI Builder when you exceed capacity, [purchase AI Builder add-on](administer-licensing.md#purchase-ai-builder-capacity), and [allocate capacity](administer-licensing.md#allocate-capacity) to your environments.

If you extend a trial after expiration, capacity is reset. You can again run and train your models, and create new ones. Scheduled run and retrain instances will resume according to the existing settings.

## Preview features

AI Builder features that are in preview release status are free to use. You don't need to obtain a license to use AI Builder preview features.

## AI Builder licenses FAQ

#### How many AI Builder credits are consumed for each operation?

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
Adding all the consumptions of the current month of a specific environment will give you the monthly consumption of this environment.

### When is credit usage count reset? Is it based on license acquisition date?

Credit usage is counted on a monthly basis, starting the first day of each month. It's not based on the license acquisition date. Credit usage of an environment should not exceed the credit allocation.  

### What happened to the remaining capacity at the end of the month? Can it be used the following month?

No, unused capacity is not carried over to the next month. Credit usage is counted on a monthly basis and reset on first day of the month. Available capacity is based on allocated capacity.

#### I exceeded my trial capacity. What can I do?

- You can [purchase AI Builder Add On](administer-licensing.md#purchase-ai-builder-capacity)  and [allocate capacity](administer-licensing.md#allocate-capacity) to your environment
- You can wait for your trial to expire, then extend your trial: this will add new capacity.
- You can also share your existing model with another user who still has active trial with capacity.

### What happens after my trial license expires?

After your AI Builder trial license expires, or if you exceed capacity:

- Your models are not deleted.

- You have to [purchase AI Builder Add-On](administer-licensing.md#purchase-ai-builder-capacity) to continue using your AI models.

- An administrator must [allocate AI Builder capacity](administer-licensing.md#allocate-capacity) to any environment where you want to use AI Builder.

- You can't create or modify AI Builder models, and no new inference will be possible when the trial expires if you don't purchase a license.

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
