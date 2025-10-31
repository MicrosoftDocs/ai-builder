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
ms.date: 11/01/2025
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

- Copilot Credits come from Microsoft Copilot Studio licenses that that can be set up as pay-as-you-go credits or prepaid capacity packs.
- AI Builder credits come mostly from purchasing AI Builder capacity add-ons. Some user licenses also provide an amount of AI Builder credits per month up to November 2026.

### Allocation

- When acquired as Copilot Studio licenses, Copilot Credits can be allocated (also known as assigned) to a specific environment in Power Platform admin center (PPAC), or left unallocated at an organization (tenant) level.
- Similarly, AI Builder credits can be allocated to a specific environment, or left unallocated.

Once an environment has Copilot Credits available, it can run the AI Builder features in all contexts. If an environment only has AI Builder credits available, it can only run AI Builder features in Power Apps and Power Automate.

### Consumption

- Consumption is reset the first of each month. When agents, agent flows, apps, or flows run AI Builder features they use Copilot Credits. A billing rate table shows how many Copilot Credits each action consumes.
- Similarly, AI Builder credits are used when AI Builder actions occur in apps and flows, and these AI Builder credits are available. A billing rate table shows how many AI Builder credits each action consumes.

### Monitoring

- Copilot Credit and AI Builder credit consumption can be monitored so that admins and makers can track consumption throughout each monthly cycle.

### Overage

- Within the month, if you use more AI Builder credits than available in your environment, features will try to use **Copilot Credits**.
- If there are none, or once you use more Copilot Credits than available in your environment, the model runs are blocked. If this happens, you need to buy more or reassign AI Builder credits or Copilot Credits to your environment.

As consumption is reset each month, the amount of Copilot Credits or AI Builder credits to purchase and/or allocate should only be enough to cover the maximum consumption you expect in a single month. Unused Copilot Credits or AI Builder credits don't roll over to the next month.  

## AI Builder Capability Rate table

|AI tool capability                            | Unit       | Copilot Studio feature| Copilot Credit rate| $ cost *| AI Builder credit rate| $ cost **| Number of Copilot packs for 1 AI Builder Add-on|
|----------------------------------------------|------------|-----------------------|--------------------|-----|---------------------|--|---|
| Prompt (basic LLM model)                     |1k tokens   | Text and generative AI tools (basic) |0.1 | 0.0008|1 (input), 3 (output) |0.0006 <sup>1</sup>|  4|
| Prompt (standard LLM model)                  | 1k tokens  | Text and generative AI tools (standard)        | 1.5 | 0.012 | 20 (input), 60 (output)      | 0.012 <sup>1</sup>                   | 3|
| Prompt (premium LLM model)                   | 1k tokens  | Text and generative AI tools (premium)         | 10                   | 0.08                     | 140 (input), 560 (output)    | 0.091 <sup>1</sup>                   |3|
| Custom document processing                   | 1 page     | Content processing tools                        | 8                    | 0.064                    | 100                           | 0.05                     |4|
| Text translation                             | 1k chars   | Text and generative AI tools (standard)        | 1.5                  | 0.012                    | 22                            | 0.011                    |3|
| Simple text analysis: sentiment analysis, <br/>language detection, key phrase extraction | 1k chars   | Text and generative AI tools (basic)           | 0.1                  | 0.0008                  | 2                             | 0.001                    |2|
| Advanced text analysis: category classification, <br/>entity extraction             | 1k chars   | Text and generative AI tools (standard)        | 1.5                  | 0.012                    | 20                            | 0.01                     |3|
| Text recognition (OCR)                       | 1 page     | Text and generative AI tools (basic)           | 0.1                  | 0.0008                   | 3                             | 0.0015                   |2|
| Receipt, invoice, identity document analysis | 1 page     | Content processing tools                        | 8                    | 0.064                    | 32                            | 0.016                    |10|
| Contract processing, health insurance card <br/>processing, image description <sup>2</sup>      | 1 image    | Content processing tools                        | 8                    | 0.064                    | 32                            | 0.016                    |10|
| Object detection                             | 1 image    | Content processing tools                        | 8                    | 0.064                    | 8                             | 0.004                    |40|
| Business card reader, prediction             | n/a        |     n/a                                           | free                 |    n/a                      | free                          |   n/a                       | n/a |

\* Using yearly prepaid Copilot Studio license (prepaid pack)<br/>
** Using yearly prepaid AI Builder add-on  
<sup>1</sup> Based on 900 input tokens + 100 output tokens (eg: 0.9 + 0.3  = 1.2 credits/1K tokens for basic)
<sup>2</sup> Free as long as in preview  

## Learn more

- Learn more about AI Builder licensing with Copilot Credits [Licensing and Copilot Credits](message-management.md).
- Learn more about AI Builder licensing with AI Builder credits [Licensing and AI Builder credits](credit-management.md).
- Learn more on the end of AI Builder capacity add-ons and AI Builder seeded credits [End of AI Builder credits](endofaibcredits.md)

## Related information

- [Microsoft Power Platform Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?LinkId=2085130)
- [Microsoft Copilot Studio Licensing Guide (pdf)](https://go.microsoft.com/fwlink/?linkid=2320995)
- [Licensing FAQ for AI Builder](/power-platform/admin/powerapps-flow-licensing-faq#ai-builder)
- [Training: Get started with AI Builder licensing (module)](/training/modules/get-started-with-ai-builder-licensing/)

[!INCLUDE[footer-include](includes/footer-banner.md)]
