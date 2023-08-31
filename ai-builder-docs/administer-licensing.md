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

***Credit Entitlement***:  AI Builder credits come with some specific user licenses, most part come from AI Builder Capacity add-on. 

***Credit Allocation***:Once acquired, credits can be allocated (aka assigned) to specific environment, or left at tenant level. Unassigned credits can be accessed by all environments by default, and can be blocked by admin.

Once an environment has access to credits, AI Builder features are enabled in this environment.

***Credit Consumption***:Some AI Builder actions consume credits : mainly when an AI Builder model runs (in a Flow or Apps). In some case when an AI Builder model is trained. Consumption is reset at the beginning of each month.

***Credit Monitoring***:Credit consumption can be monitored, so admin and maker know how many credits have been consumed since the beginning of the month. 

***Credit Overage***:In an environment, when consumption since beginning of the month exceeds available credits, environment is in overage and some features are progressively blocked. Purchase of new credits and/or reassignment need to happen. 

***Trials***:AI Builder credits can also come from AI Builder trial. In that case, they are linked to the user and don't need to be allocated. see [AI Builder Trial](/#AI-Builder-Trial)

Learn more about AI Builder credits  in  [Administer/Credit Management](credit-management.md) page. 
Learn more about AI Builder trials in [AI Builder trial](ai-builder-trials.md) page

Learn more about licenses and license management in Power Apps in [About licensing and license management](/power-platform/admin/wp-license-management).

### See also

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Power Platform licensing FAQ / AI Builder section](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Estimate the AI Builder capacity that’s right for you in AI Builder Calculator](https://powerapps.microsoft.com/ai-builder-calculator/)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
