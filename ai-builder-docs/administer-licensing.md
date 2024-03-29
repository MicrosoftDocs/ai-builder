---
title: Overview of licensing
description: Learn about licensing in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 01/10/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Overview of licensing

AI Builder is licensed on a monthly capacity basis. The capacity is measured in terms of *service credits* or *AI Builder credits*. Qualifying prerequisites include having a Power Apps, Power Automate, or Dynamics 365 license that allows you to create the Microsoft Power Platform environment.

Access to AI Builder features within an environment requires AI Builder credits.

**Credits entitlement**:  AI Builder credits come mostly from purchasing AI Builder capacity add-ons. Some user licenses also give you a certain amount of AI Builder credits per month as part of their benefits.

**Credits allocation**: Once acquired, credits can be allocated (also known as assigned) to a specific environment, or left unallocated at an organization (tenant) level. By default, environments without allocated credits can consume unallocated credits. An administrator can prevent the use of unallocated credits by changing a setting in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home).

Once an environment has credits from either allocated or unallocated sources, it can use the AI Builder features.

**Credits consumption**: Consumption is reset the first of each month. Credits are used when certain AI Builder actions take place, particularly when an AI Builder model is executed in a Power Automate flow or a Power Apps application. Additionally, credit consumption may occur during the training of an AI Builder model. The number of consumed credits depends on the AI Builder model.

**Credit monitoring**: Credit consumption can be monitored so that the admin and maker know how many credits have been consumed since the beginning of the month.

**Credit overage**: Within the month, if you use more credits than you have, you will have some features blocked gradually because of overage. When an environment is in *simple overage*, you can run models and use more credits, but you can’t edit or create models. When an environment is in *important overage*, model runs are blocked. If this happens, you need to buy more credits or reassign them.

**Trials**: You can try AI Builder for free in an organization’s tenants that don’t have AI Builder credits. In this case, AI Builder capacity is linked to the user and doesn't need to be allocated.

As consumption is reset each month, the amount of credit to purchase and/or allocate should be the consumption of a single month. Unused credits don't roll over to the next month. With a 1 million credits add-on purchased and allocated to a single environment, the environment can consume up to 1 million credits per month. Assuming this environment consumes 800,000 credits each month, then total consumption of the year would be 9.6 million credits.

## Learn more

To learn more about licensing, go to [AI Builder licensing and credit management](credit-management.md).

To learn more about trials, go to [AI Builder trial](ai-builder-trials.md).

### See also

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in the calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
