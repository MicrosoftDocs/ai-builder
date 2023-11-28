---
title: AI Builder licensing summary
description: Learn about licensing in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 09/19/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# AI Builder licensing summary

AI Builder is licensed on a capacity basis. This capacity is expressed in the form of *service credits* or *AI Builder credits*. Qualifying prerequisites include having Power Apps, Power Automate, or Dynamics 365 license that allows you to create the Microsoft Power Platform environment.

Access to AI Builder features within an environment requires AI Builder credits.

**Credits entitlement**:  AI Builder credits come mostly from AI Builder capacity add-ons. Some user licenses provide seeded AI Builder credits.

**Credits allocation**: Once acquired, credits can be allocated (also known as assigned) to a specific environment, or left unallocated at an organization (tenant) level. By default, environments without allocated credits can consume unallocated credits. An administrator can block the use of unallocated credits by changing a setting in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/home).

Once an environment has access to credits using allocated or unallocated credits, AI Builder features are enabled in this environment.

**Credits consumption**: Consumption is reset at the beginning of each month. Some AI Builder actions consume credits, mainly when an AI Builder model runs in a flow in Power Automate or an app in Power Apps. In some cases, credits are consumed when an AI Builder model is trained. The number of consumed credits depends on the AI Builder model.

**Credit monitoring**: Credit consumption can be monitored so that the admin and maker know how many credits have been consumed since the beginning of the month.

**Credit overage**: In an environment, when consumption since the beginning of the month exceeds available credits, the environment is in overage and some features are progressively blocked. When an environment is in *simple overage*, models continue to run and consume credits, but editing and creating models is blocked. When an environment is in *important overage*, model runs are blocked. If this happens, you need to either purchase new credits and/or reassign.

**Trials**: In an organization's tenants without AI Builder credits, you can start an AI Builder trial. In this case, AI Builder capacity is linked to the user and doesn't need to be allocated.

## Learn more

To learn more about licensing, go to [AI Builder licensing and credit management](credit-management.md).

To learn more about trials, go to [AI Builder trial](ai-builder-trials.md).

### See also

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in the calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
