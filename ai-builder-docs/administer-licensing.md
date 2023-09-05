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

AI Builder is licensed as an add-on to your Power Apps, Power Automate, or Dynamics 365 license. This means you need a Power Apps, Power Automate, or Dynamics 365 license that allows you to create a Microsoft Power Platform environment.

Access to AI Builder features within an environment require **AI Builder credits**.

***Credit Entitlement***:  AI Builder credits come mostly from AI Builder Capacity add-on. Some specific user licenses brings AI Builder credits.

***Credit Allocation***:Once acquired, credits can be allocated (aka assigned) to specific environment, or left unallocated at tenant level. Unallocated credits can be accessed by all environments without allocated credits, and can be blocked by admin in Power Platform Admin Center.

Once an environment has access to credits, AI Builder features are enabled in this environment.

***Credit Consumption***:Some AI Builder actions consume credits : mainly when an AI Builder model runs (in a Flow or Apps). In some case when an AI Builder model is trained. Consumption is reset at the beginning of each month.

***Credit Monitoring***:Credit consumption can be monitored, so admin and maker know how many credits have been consumed since the beginning of the month. 

***Credit Overage***:In an environment, when consumption since beginning of the month exceeds available credits, environment is in overage and some features are progressively blocked. When an environment is in **simple overage** models continue to run and consume credits, but editing and creating models is blocked. When environment is in **important overage**, models runs will be blocked. Purchase of new credits and/or reassignment need to happen. 

***Trials***: In tenants without AI Builder credits, users can start AI Builder trial. In that case, AI Builder capacity is linked to the user and don't need to be allocated. see [AI Builder Trial](/#AI-Builder-Trial)


Learn more about AI Builder Licensing and Credit management  in  [Administer/AI Builder Licensing and Credit Management](credit-management.md) page. 


Learn more about AI Builder trials in [AI Builder trial](ai-builder-trials.md) page

### See also

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Power Platform licensing FAQ / AI Builder section](/power-platform/admin/powerapps-flow-licensing-faq.md#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in AI Builder Calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
