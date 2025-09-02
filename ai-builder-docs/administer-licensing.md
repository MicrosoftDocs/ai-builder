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

AI Builder is licensed on a monthly capacity basis.  
In Power Automate or Power Apps context, the capacity is measured in terms of *AI Builder credits*. Qualifying prerequisites include having a Power Apps, Power Automate, or Dynamics 365 license that allows you to create the Microsoft Power Platform environment.  

> [!NOTE]
> In Copilot Studio context, AI Builder features don't require *AI Builder credits*, but consume *Copilot credits*.  [learn more](message-management.md)  

This section provides an overview on *AI Builder credits* management.

**AIB Credits entitlement**:  AI Builder credits come mostly from purchasing AI Builder capacity add-ons. Some user licenses also give you a certain amount of AI Builder credits per month as part of their benefits.

**AIB Credits allocation**: Once acquired, AIB credits can be allocated (also known as assigned) to a specific environment, or left unallocated at an organization (tenant) level. By default, environments without allocated AIB credits can consume unallocated AIB credits. An administrator can prevent the use of unallocated AIB credits by changing a setting in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home).

Once an environment has AIB credits from either allocated or unallocated sources, it can use the AI Builder features.

**AIB Credits consumption**: Consumption is reset the first of each month. AIB Credits are used when certain AI Builder actions take place, particularly when an AI Builder model is executed in a Power Automate cloud flow or a Power Apps application. Additionally, AIB credit consumption might occur during the training of an AI Builder model. The number of consumed AIB credits depends on the AI Builder model.

**AIB Credit monitoring**: AIB Credit consumption can be monitored so that the admin and maker know how many AIB credits were consumed since the beginning of the month.

**AIB Credit overage**: Within the month, if you use more AIB credits than you have, some features are blocked gradually because of overage. When an environment is in *simple overage*, you can run models and use more AIB credits, but you can’t edit or create models. When an environment is in *important overage*, model runs are blocked. If this happens, you need to buy more AIB credits or reassign them.

**Trials**: You can try AI Builder for free in an organization’s tenants that don’t have AI Builder credits. In this case, AI Builder capacity is linked to the user and doesn't need to be allocated.

As consumption is reset each month, the amount of AIB credit to purchase and/or allocate should be the consumption of a single month. Unused AIB credits don't roll over to the next month. With a 1 million AIB credits add-on purchased and allocated to a single environment, the environment can consume up to 1 million AIB credits per month. Assuming this environment consumes 800,000 AIB credits each month, then total consumption of the year would be 9.6 million AIB credits.

## Learn more

- To learn more about licensing in Power Automate and Power Apps context, go to [AI Builder licensing and credit management](credit-management.md).
- To learn more about licensing in Copilot Studio context, go to [AI Builder licensing in Copilot Studio](message-management.md).
- To learn more about trials, go to [AI Builder trial](ai-builder-trials.md).

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
