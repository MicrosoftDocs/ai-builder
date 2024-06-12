---
title: AI Builder trial
description: Learn about the AI Builder trial.
author: antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 01/10/2024
ms.author: antode
ms.reviewer: angieandrews
---

# AI Builder trial

To get started using AI Builder, use premium features for a limited time with a [trial license](https://powerapps.microsoft.com/ai-builder/). Alternatively, use preview features without obtaining a license at all.

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you can start your AI Builder trial after you have a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment.

> [!NOTE]
> You can't start an AI Builder trial if you have AI Builder credits already on your tenant by purchasing a capacity add-on or through other premium licenses.

## Benefits of a trial license

An [AI Builder trial license](https://powerapps.microsoft.com/ai-builder/) enables you to use AI Builder features for free during the 30-day trial period.

What you get an AI Builder trial license:

- Create and use AI models in any environment (trial or production).
- Store your AI model results in Dataverse.
- Use AI model in your apps, flows, and more.

Custom prompts, prebuilt prompts, and Create text with GPT aren't available with an AI Builder trial.

## Activate an AI Builder trial license

1. Sign in to	[Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).
1. On the left pane, select **... More** > **AI hub**.
1. If there's no database (you get the message, *no database found*), do the following:
    1. Select **Create a database**, and then choose a currency and language.
    1. Select **Create my database**.  

        :::image type="content" source="media/ai-builder-trials/create-my-db.png" alt-text="Screenshot of creating a database.":::

    1. Refresh the **Hub** page until the *no database found* message disappears.
1. On the top of the screen, select **Start free trial**.  

    :::image type="content" source="media/ai-builder-trials/start-free-trial.png" alt-text="Screenshot of 'Start free trial' button'.":::

> [!NOTE]
> Your AI Builder trial license is applicable at the user level, not the environment level. You can use your trial license on multiple environments. Another user would have to start their own trial or paid license to use your models in any environment.

## After the trial expires

Your AI Builder trial license expires after 30 days.

To continue using AI Builder, purchase AI Builder add-on capacity and allocate AI Builder capacity to your environments. You may also be able to extend the trial period. Trials can be extended a limited number of times. Extension can only occur after the trial expires.

To renew your AI Builder trial license, do the following:

1. Sign in to	[Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).
1. On the left pane, select **... More** > **AI hub**.
1. On the banner at the top of the screen, select **Extend trial**.

## Trial capacity

An AI Builder trial license includes a limited amount of AI Builder capacity. You use this capacity when running or training models.

If you exceed your AI Builder capacity, you receive an over-capacity notification. These notifications appear as banners in AI Builder pages or when using the model.

The following functions aren't available when you exceed capacity:

- Create a model or a new version of a model.
- Run a model within Power Apps or in a Power Automate flow.
  - You can still share your model with another user. They can run it using their own AI Builder capacity if they have a valid trial.
- Scheduled model run or retrain.
  - Some scenarios allow scheduled run or retrain, which is configured on the model settings panel. These scheduled tasks fail when you exceed capacity. Therefore, data isn't refreshed, and the model isn't retrained.

To continue using AI Builder when you exceed capacity, [purchase AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits), and [allocate capacity](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits) to your environments.

When you extend a trial after expiration, capacity is reset. You can again run and train your models, and create new ones. Scheduled run and retrain instances resume according to the existing settings.

You can't extend a trial before expiration.

## AI Builder trial FAQ

For answers to frequently asked questions, go to [AI Builder licensing FAQ](credit-management.md#ai-builder-licensing-faq).

### I exceeded my trial capacity. What can I do?

- You can [purchase the AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits) and [allocate capacity](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits) to your environment.
- You can wait for your trial to expire, then extend your trial. This adds new capacity.
- You can share your existing model with another user who still has active trial with capacity.

### What happens after my trial license expires?

After your AI Builder trial license expires, or if you exceed capacity:

- Your models aren't deleted.
- You need to [purchase AI Builder add-on](credit-management.md#get-entitlement-to-ai-builder-credits) to continue using your AI models.
- An administrator must [allocate AI Builder capacity](credit-management.md#make-credits-available-for-an-environment-allocated-and-unallocated-credits) to any environment where you want to use AI Builder.
- You can't create or modify AI Builder models, and no new inference is possible when the trial expires if you don't purchase a license.
- You can also extend your trial, but only for a limited number of times.

### What happens to my data and models when my AI Builder trial expires?

Data and models are deleted only when the environment is deleted.

### Where can I find more information about trial environments?

To learn more, go to [About trial environments](/power-platform/admin/trial-environments).

### Can I block users in my organization from signing up for an AI Builder trial?

Any individual can try out the features of AI Builder for 30 days and incur no costs to your company. This option is available to any user in an organization (tenant) and can't be disabled by an admin. Once your company purchases some AI credits (for example, through capacity add-ons or inclusion in some licenses), trials aren't proposed to users anymore.

You can block the use of AI Builder trial by disabling the **Allow unassigned credits** tenant setting in [Power Platform admin center](https://admin.powerplatform.microsoft.com/home). If you disable this setting, the only way to perform AI Builder actions in an environment is if you assign credits to this environment.

### See also

- [AI Builder licensing and credit management](credit-management.md)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)
- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in the calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
