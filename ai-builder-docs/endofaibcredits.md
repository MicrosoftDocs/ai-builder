---
title: End of AI Builder credits 
description: Learn about the end of AI Builder credits 
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 10/30/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# End of AI Builder credits

In October 2025, Microsoft announced a progressive end of AI Builder credits. This article explains the change.  
The progressive end of AI Builder credits doesn't impact AI Builder features: they will continue to be supported in all contexts, using Copilot Credits.  
AI Builder credits were available as capacity packs (AI Builder capacity add-ons) which provided 1 million AI Builder credits, and as seeded capacity in Power Platform licenses, like Power Apps premium licenses, or Power Automate premium licenses.

Both AI Builder capacity add-ons and seeded credits in premium licenses are impacted by this end of AI Builder credits, with different calendars.

## Detailed  calendar

|Date                         |Event                                        | Who is involved                                                           | How are they impacted |
|----------------------------|----------------------------------------------|---------------------------------------------------------------------------|-------------------------- |
|11/01/2025                  | End of Sales for AI Builder capacity add-ons | New 'add-on' customers  = customers without any active AI Builder capacity add-ons | New 'add-on' customers can't purchase AI Builder capacity add-ons. |
|11/01/2025                  |(no change)                                   | Existing 'add-on' customers with active AI Builder capacity add-ons                | Existing 'add-on' customers can still use their AI Builder credits linked to their AI Builder capacity add-ons, but also renew them, and purchase new ones. |
|11/01/2025                  |(no change)                                   | New 'seeded' customers = customer without any active seeded AI Builder credits     | New 'seeded' customers can purchase premium licenses which will provide AI Builder seeded credits that they can use to run AI Builder features.  |
|11/01/2025                  |(no change)                                   | Existing 'seeded' customers = customers with active seeded AI Builder credits      | Existing 'seeded' customers can  use their seeded AI Builder credits linked to their premium licenses, renew or add new premium licenses. |
|11/01/2026                  | End of Life of AI Builder capacity add-ons   | Existing add-on customers with active AI Builder capacity add-ons                  | Existing 'add-on' customers can still use their credits linked to their active AI Builder capacity add-ons, but cannot renew them, or purchase new ones. |
|11/01/2026                  | End of seeded AI Builder credits             | Existing 'seeded' customers with active seeded AI Builder credits                  | Existing 'seeded' customers won't receive seeded AI Builder credits any more. These seeded AI Builder credits will be definitively removed from their premium licenses. |
| after 11/01/2026           | (no change)                                  | Existing add-on customers with active AI Builder capacity add-ons                  | Customers with active AI Builder capacity add-ons continue using their AI Builder credits to run AI Builder features until their licenses expire|

## FAQ

Use the following FAQ to learn more about Copilot Credits based licensing for AI Builder.

### How will this transition affect our existing contracts and current license entitlements?

Existing 'add-ons' customers will retain access to their AI Builder credits coming from AI Builder add-ons until their AI Builder add-ons contracts expire. Existing 'seeded' customers will retain access to their AI Builder credits coming from seeded premium licenses up to November 1, 2026.

When using AI Builder features in Power Apps or Power Automate context, these AI Builder credits will be consumed first. If AI Builder credits are exhausted or unavailable, the system will attempt to use Copilot Studio Credits. If no Copilot Credits are available, usage will be blocked.

### Will there be automatic conversion or migration of AI Builder credits to Copilot Studio Credits?

There's no automatic conversion of AI Builder credits to Copilot Studio Credits. Instead, a dual-mode licensing model will apply: environments first consume AI Builder credits, then Copilot Studio Credits, if needed.
In order to replace the AI Builder credits which will progressively end, customers are invited to purchase Copilot Credits.

### What happens to AI Builder credits currently included in licenses such as Power Apps Premium, Power Automate Premium, and Dynamics 365 Finance, and others?

The seeded AI Builder credits from licenses like Power Apps Premium or Dynamics 365 will remain usable (on a monthly basis) until November 1, 2026, based on the number of active licenses.

After Nov 1, 2026, these seeded credits will be removed for all new and existing customers, including those with an Enterprise Agreement. Copilot Studio Credits will be required for continued access (or active AI Builder add-ons).

### How long do these credits remain available, and will they transition to Copilot Studio Credits after November 2026?

Seeded Credits are available to use until November 1, 2026. After that date, they'll become unavailable. There won't be a transition to Copilot Studio Credits.
Credits coming from AI Builder add-ons will remain available until the end of contracts.

### What's the exact conversion ratio between AI Builder service credits and Copilot Studio Credits in AI Builder usage?

There isn't a conversion of entitlement from one currency into the other currency. Rates are different for each scenario.

### New segmentation (Basic, Standard, Premium, Content Processing) is unfamiliar. How does this mapping apply to existing AI Builder workloads?

The new segmentation (Basic, Standard, Premium, Content Processing) refers to tiers of AI capabilities. Existing AI Builder workloads will map to these tiers based on the type of model or prompt used. For instance, the sentiment analysis model is mapped to *text and generative AI tools (Basic)*, and entity extraction maps to *text and generative AI tools (Standard)*.

### What new administrative controls will be available in Power Platform admin center to monitor, allocate, or restrict Copilot Studio Credit usage?

The Power Platform admin center now includes detailed capacity management tools:

- Daily usage tracking per environment
- Allocation of prepaid or pay-as-you-go Copilot Studio Credits
- Product level consumption insights
- Governance features like environment routing, DLP (data loss prevention) policies, and audit logs
