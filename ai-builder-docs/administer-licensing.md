---
title: AI Builder licensing
description: Learn about licensing in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 04/13/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# AI Builder licensing in a nutshell

AI Builder is licensed on a capacity basis. This capacity is expressed in the form of “service credits” or “AI Builder credits.” Qualifying prerequisites include having a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment

Access to AI Builder features within an environment requires **AI Builder credits**.

***Credits Entitlement***:  AI Builder credits come mostly from AI Builder Capacity add-ons. Some user licenses provide 'seeded' AI Builder credits.

***Credits Allocation***: Once acquired, credits can be allocated (as known as assigned) to specific environment, or left unallocated at organization (tenant) level. By default, environments without allocated credits can consume unallocated credits. Administrator can block the use of unallocated credits by changing a setting in Power Platform Admin Center.

Once an environment has access to credits (using allocated or unallocated credits), AI Builder features are enabled in this environment.

***Credits Consumption***: Consumption is reset at the beginning of each month. Some AI Builder actions consume credits: mainly when an AI Builder model runs (in a Flow or Apps). In some case, when an AI Builder model is trained. Number of consumed credits depends on AI Builder Model.

***Credit Monitoring***: Credit consumption can be monitored, so admin and maker know how many credits have been consumed since the beginning of the month. 

***Credit Overage***: In an environment, when consumption since beginning of the month exceeds available credits, environment is in overage and some features are progressively blocked. When an environment is in **simple overage** models continue to run and consume credits, but editing and creating models is blocked. When environment is in **important overage**, models runs are blocked. Purchase of new credits and/or reassignment needs to happen. 

***Trials***: In organizations (tenants) without AI Builder credits, users can start AI Builder trial. In that case, AI Builder capacity is linked to the user and doesn't need to be allocated. 



## Learn more
Learn more about  Licensing  in  [AI Builder Licensing and Credit Management](credit-management.md) page in 'Administration and Security' section. 

Learn more about AI Builder trials in [AI Builder trial](ai-builder-trials.md) page in 'Administration and Security' section.

## See also

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Power Platform licensing FAQ / AI Builder section](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in AI Builder Calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
