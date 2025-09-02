---
title: Overview of licensing
description: Learn about licensing in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - Antoine2F
  - v-aangie
ms.topic: concept-article
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 09/02/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Overview of licensing

AI Builder is licensed on a monthly capacity basis. In Power Automate or Power Apps context, the capacity is measured in terms of *AI Builder credits*. Qualifying prerequisites include having a Power Apps, Power Automate, or Dynamics 365 license that allows you to create the Microsoft Power Platform environment.

> [!NOTE]
> In Copilot Studio context, AI Builder features don't require *AI Builder credits*, but consume *Copilot credits*.  Learn more in [AI Builder licensing in Microsoft Copilot Studio: Copilot credit management](message-management.md).

This section provides an overview on *AI Builder credits* management.

**AI Builder credits entitlement**:  AI Builder credits come mostly from purchasing AI Builder capacity add-ons. Some user licenses also give you a certain amount of AI Builder credits per month as part of their benefits.

**AI Builder credits allocation**: Once acquired, AI Builder credits can be allocated (also known as assigned) to a specific environment, or left unallocated at an organization (tenant) level. By default, environments without allocated AI Builder credits can consume unallocated AI Builder credits. An administrator can prevent the use of unallocated AI Builder credits by changing a setting in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home).

Once an environment has AI Builder credits from either allocated or unallocated sources, it can use the AI Builder features.

**AI Builder credits consumption**: Consumption is reset the first of each month. AI Builder credits are used when certain AI Builder actions take place, particularly when an AI Builder model is executed in a Power Automate cloud flow or a Power Apps application. Additionally, AI Builder credit consumption might occur during the training of an AI Builder model. The number of consumed AI Builder credits depends on the AI Builder model.

**AI Builder credit monitoring**: AI Builder credit consumption can be monitored so that the admin and maker know how many AI Builder credits were consumed since the beginning of the month.

**AI Builder credit overage**: Within the month, if you use more AI Builder credits than you have, some features are blocked gradually because of overage. When an environment is in *simple overage*, you can run models and use more AI Builder credits, but you can't edit or create models. When an environment is in *important overage*, model runs are blocked. If this happens, you need to buy more AI Builder credits or reassign them.

**Trials**: You can try AI Builder for free in an organization’s tenants that don't have AI Builder credits. In this case, AI Builder capacity is linked to the user and doesn't need to be allocated.

As consumption is reset each month, the amount of AI Builder credit to purchase and/or allocate should be the consumption of a single month. Unused AI Builder credits don't roll over to the next month. With a 1 million AI Builder credits add-on purchased and allocated to a single environment, the environment can consume up to 1 million AI Builder credits per month. Assuming this environment consumes 800,000 AI Builder credits each month, then total consumption of the year would be 9.6 million AI Builder credits.

## Learn more

- Learn more about licensing in Power Automate and Power Apps context in [AI Builder licensing and credit management](credit-management.md).
- Learn more about licensing in Copilot Studio context in [AI Builder licensing in Copilot Studio](message-management.md).
- Learn more about trials in [AI Builder trial](ai-builder-trials.md).

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
