---
title: AI Builder Licensing - AI Builder | Microsoft Docs
description: Provides information about licensing in AI Builder.
author: Mrigankka
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 12/23/2019
ms.author: mfotedar
ms.reviewer: v-dehaas
---

# AI Builder licensing

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you can start your AI Builder trial after you have a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Common Data Service environment.

For detailed information about AI Builder licensing:

- [Microsoft Power Apps and Power Automate Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130)<!--I don't think you want the locale identifier? -->
- [AI Builder licensing FAQ](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)

## Preview features and trial licenses

Want to get started using AI Builder? Use premium features for a limited time with a trial license, or use preview features without obtaining a license at all.

### Preview features

AI Builder features that are in preview release status are free to use. You don't need to obtain a license to use AI Builder preview features.

### AI Builder trial licenses

An AI Builder trial license enables you to use AI Builder features for free during the 30-day trial period.

What you get with an AI Builder trial license:

- Create and use AI models in any environment (trial or production).
- Store your AI model results in Common Data Service.
- Use AI model in your apps, flows, and more.

> [!NOTE]
> Your AI Builder trial license is applicable at the user level, not the environment level: you can use your trial license on multiple environments. Another user would have to start their own trial or paid license to use your models in any environment.

### After the trial expires

Your AI Builder trial license expires after 30 days.

To continue using AI Builder, purchase AI Builder add-on capacity and allocate AI Builder capacity to your environments. You may also be able to extend the trial period. Trials can be extended a limited number of times. Extension can only occur after the trial expires.

### Trial capacity

An AI Builder trial license includes a limited amount of AI Builder capacity. You use this capacity when running or training models.

If you exceed your AI Builder capacity, you’ll receive a over-capacity  notification. These notifications appear as banners in AI Builder pages or when using the model.

The following functions aren't available when you exceed capacity:

- Create a model or a new version of a model
- Run a model within Power Apps or a in a Power Automate flow.
  - You can still share your model with another user. They can run it using their own AI Builder capacity. 
- Scheduled model run or retrain
  - Some scenarios allow scheduled run or retrain, which is configured on the model settings panel. These scheduled tasks will fail when you exceed capacity. Therefore, data won’t be refreshed , and the model won’t be retrained.

To continue using AI Builder when you exceed capacity, purchase AI Builder add-on capacity, and allocate it to your environments.
>[!NOTE]
>When you have an active trial and you’re working within an environment that has allocated AI Builder capacity, then you consume the environment allocated capacity, not trial capacity.

If you extend a trial after expiration, capacity is reset. You can again run and train your models, and create new ones. Scheduled run and retrain instances will resume according to the existing settings.

## Paid licenses and capacity allocation

First, you have to purchase AI Builder capacity add-on for your Power Apps or Power Automate licenses. Then an administrator has to allocate that capacity to any Power Apps environment where you want to use AI Builder.

### Purchase AI Builder capacity

The  AI Builder capacity add-on can be purchased by a billing administrator in the Power Platform Admin Center, or by using your usual channel.

The [AI Builder calculator](https://powerapps.microsoft.com/ai-builder-calculator/) helps estimate the required add-on capacity based on your estimated consumption.

Some Microsoft products include some AI Builder capacity. Your environment admin can check entitlement in the Power Platform admin center in [Capacity add-ons](https://docs.microsoft.com/en-us/power-platform/admin/capacity-add-on). When this amount is not enough, you can complete it with 1 or several AI Builder capacity add-ons.

### Allocate AI Builder capacity

Once entitled to AI Builder capacity, an environment administrator has to allocate capacity for AI Builder to the environment before you can use it. Information about how to allocate capacity in the Power Platform admin center is available in [Capacity add-ons](https://docs.microsoft.com/en-us/power-platform/admin/capacity-add-on).


### AI Builder paid licenses FAQ

#### I exceeded my trial capacity. What can I do?

- You can purchase AI Builder Add On and allocate capacity to your environment
- You can wait for your trial to expire, then extend your trial: this will add new capacity.
- You can also share your existing model with another user who still has active trial with capacity.

#### How do I convert my trial environment to a production environment?

For more information, see [About trial environments](/power-platform/admin/trial-environments).

#### Where can I find more information about license management in Power Apps and Power Automate?

More information about licenses and license management in Power Apps is available in Microsoft Power Platform [License management](/power-platform/admin/wp-license-management).

#### Where can I find more information about trial environments?

For more information, see [About trial environments](/power-platform/admin/trial-environments).

After your AI Builder trial license expires, or if you exceed capacity:

- You have to [purchase a license](/power-platform/admin/signup-for-powerapps-admin) to continue using your AI models.
- An administrator must allocate AI Builder capacity to any environment where you want to use AI Builder.
- You can't create or modify AI Builder models, and no new inference will be possible when the trial expires if you don't purchase a license.

#### How do I convert my trial environment to a production environment?

For more information, see [About trial environments](https://docs.microsoft.com/power-platform/admin/trial-environments).

