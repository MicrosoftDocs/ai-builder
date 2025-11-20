---
title: Overview of licensing
description: Learn about licensing in AI Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - Antoine2F
  - v-aangie
  - EllenWehrle
ms.topic: concept-article
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 11/20/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Overview of licensing

In Copilot Studio, AI Builder features always consume *Copilot Credits*. Learn more in [Licensing and Copilot Credits](message-management.md).
In Power Apps and Power Automate, AI Builder features consume either *AI Builder credits* ([Licensing and AI Builder credits](credit-management.md)), or *Copilot Credits*  ([Licensing and Copilot Credits](message-management.md)).

AI Builder is licensed on a capacity basis. Building custom and testing models (including prompts) doesn't require AI Builder credits or Copilot Credits. Running them in agents, agent flows, apps, or flows consume these credits.

> [!IMPORTANT]
>
> On November 1, 2025, there are major changes to AI Builder licensing. Starting on this date, AI Builder features in Power Apps and Power Automate can consume both AI Builder credits, or Copilot Credits if there are no available AI Builder credits.
>
> - AI Builder capacity add-ons can only be purchased as a renewal or true-up by existing customers. New customers must purchase Copilot Credits to run AI Builder features.
> - AI Builder credits seeded in Power Platform or Dynamics licenses will be removed in November 2026.
> - AI Builder trials are discontinued.

## Prerequisites

Qualifying prerequisites include having a Microsoft Power Platform environment with Dataverse.

## Entitlement, allocation, and consumption of Copilot Credits and AI Builder credits

Learn more about Copilot Credits and AI Builder credits.

### Entitlement

- Copilot Credits are the common currency across Copilot Studio capabilities. They're available through pay-as-you-go meters, prepurchase plans, and Copilot Credit prepaid pack subscriptions (providing monthly capacity).
- AI Builder credits come mostly from purchasing AI Builder capacity add-ons (providing monthly capacity). Some user licenses also provide an amount of AI Builder credits per month up to November 2026.

### Allocation

- When acquired as prepaid pack subscription, Copilot Credits can be allocated (also known as assigned) to a specific environment in Power Platform admin center (PPAC), or left unallocated at an organization (tenant) level.
- Similarly, AI Builder credits can be allocated to a specific environment, or left unallocated.

Once an environment has Copilot Credits available, it can run the AI Builder features in all contexts. If an environment only has AI Builder credits available, it can only run AI Builder features in Power Apps and Power Automate.

### Consumption

- Consumption is reset the first of each month. When agents, agent flows, apps, or flows run AI Builder features they use Copilot Credits. A billing rate table shows how many Copilot Credits each action consumes.
- Similarly, AI Builder credits are used when AI Builder actions occur in apps and flows, and these AI Builder credits are available. A billing rate table shows how many AI Builder credits each action consumes.
 
Agents and agent flows only consume Copilot Credits. AI Builder features in apps and flows first try to consume AI Builder credits, then, if absent or exhausted, they try to consume Copilot Credits.

### Monitoring

- Copilot Credit and AI Builder credit consumption can be monitored so that admins and makers can track consumption throughout each monthly cycle.

### Overage

- Within the month, if you use more AI Builder credits than available in your environment, features will try to use **Copilot Credits**.
- If there are none, or once you use more Copilot Credits than available in your environment, the model runs are blocked. If this happens, you need to buy more or reassign AI Builder credits or Copilot Credits to your environment.

As consumption is reset each month, the amount of Copilot Credits or AI Builder credits to purchase and/or allocate should only be enough to cover the maximum consumption you expect in a single month. Unused Copilot Credits or AI Builder credits don't roll over to the next month.  

## AI Builder Capability Rate table

| **AI Builder/ AI tool capability**                               | **Unit**       | **Copilot Studio feature**                | **Copilot Credit rate** | **Corresponding $ cost*** | **AI Builder credit rate** | **Corresponding $ cost** ** |
|------------------------------------------------------|---------------|-------------------------------------------|--------------------------|-------------------------|-----------------------------|--------------------------|
| Prompt (basic LLM model)                             | 1k tokens     | Text and generative AI tools (basic)     | 0.1                      | 0.001                   | 1.2<sup>2</sup>            | 0.0006                  |
| Prompt (standard LLM model)                          | 1k tokens     | Text and generative AI tools (standard)  | 1.5                      | 0.015                   | 24<sup>2</sup>             | 0.012                   |
| Prompt (premium LLM model)                           | 1k tokens     | Text and generative AI tools (premium)   | 10                       | 0.1                     | 182<sup>2</sup>            | 0.091                   |
| Contract processing, health insurance card processing,image description<sup>1</sup> | 1 image       | Content processing tools                  | 8                        | 0.08                    | 32                          | 0.016                   |
| Object detection                                     | 1 image       | Content processing tools                  | 8                        | 0.08                    | 8                           | 0.004                   |
| Custom document processing                           | 1 page        | Content processing tools                  | 8                        | 0.08                    | 100                         | 0.05                    |
| Receipt, invoice, identity document analysis         | 1 page        | Content processing tools                  | 8                        | 0.08                    | 32                          | 0.016                   |
| Text recognition (OCR)                               | 1 page        | Text and generative AI tools (basic)      | 0.1                      | 0.001                   | 3                           | 0.0015                  |
| Simple text analysis: sentiment, language detection,key phrase extraction | 1k chars      | Text and generative AI tools (basic)      | 0.1                      | 0.001                   | 2                           | 0.001                   |
| Advanced text analysis: category classification,entity extraction | 1k chars      | Text and generative AI tools (standard)   | 1.5                      | 0.015                   | 20                          | 0.01                    |
| Text translation                                     | 1k chars      | Text and generative AI tools (standard)   | 1.5                      | 0.015                   | 22                          | 0.011                   |
| Business card reader, prediction                     | n/a           | n/a                                       | free                     | n/a                     | free                        | n/a                     |


\* Based on PayGo billing, 1 Copilot Credit = $0.01  
** Based on yearly prepaid Tier 1 AI Builder add-on  : monthly capacity = 1 million AIBuilder credits, $500 per month  
<sup>1</sup> Free as long as in preview  
<sup>2</sup> Estimation per 1K tokens, based on average request where input represents 90% of consumed tokens, and output represents 10%. 
Here are exact rates: 
|AI Builder / AI tool capability                            | AI Builder credit per 1K tokens in input     | AI Builder credit per 1K tokens in output  | 
|----------------------------------------------|----------------------------------------------|--------------------------------------------|
| Prompt (basic LLM model)                     |1                                             |3                                           |  
| Prompt (standard LLM model)                  |20                                            |60                                          | 
| Prompt (premium LLM model)                   |140                                           |560                                         |


## Learn more

- Learn more about AI Builder licensing with Copilot Credits [Licensing and Copilot Credits](message-management.md).
- Learn more about AI Builder licensing with AI Builder credits [Licensing and AI Builder credits](credit-management.md).
- Learn more on the end of AI Builder capacity add-ons and AI Builder seeded credits [End of AI Builder credits](endofaibcredits.md)

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Microsoft Copilot Studio Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?linkid=2320995)
- [Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
