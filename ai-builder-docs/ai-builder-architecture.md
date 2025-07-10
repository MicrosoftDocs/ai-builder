---
title: AI Builder architecture
description: Learn how data you provide to AI Builder is processed, used, and stored.
author: jekom1
contributors: 
  - jekom1
  - phil-cmd
  - v-aangie
ms.topic: article
ms.custom: 
ms.date: 01/09/2025
ms.update-cycle: 180-days
ms.author: jelenak
ms.reviewer: angieandrews
ms.collection: bap-ai-copilot
---

# AI Builder architecture

This article explains how data you provide to AI Builder is processed, used, and stored. AI Builder stores and processes data to provide the service and allow you to monitor its use.

The following screenshot shows the AI Builder architecture.

:::image type="content" source="media/ai-builder-architecture/aib-architecture.png" alt-text="Screenshot of AI Builder architecture.":::

Behind the scenes, AI Builder generates or uses Azure AI models for most scenarios, as shown in the following screenshot.

:::image type="content" source="media/ai-builder-architecture/aib-models.png" alt-text="Screenshot of scenarios that use AI models.":::

> [!IMPORTANT]
> Your input or output data, your embeddings, and your training data:
>
> - Aren't available to other customers.
> - Aren't available to OpenAI.
> - Aren't used to improve OpenAI or Azure AI models.
> - Aren't used to train, retrain, or improve Azure AI foundation models.
> - Aren't used to improve any Microsoft or 3rd party products or services without your permission or instruction.

## Enterprise data protection

This section emphasizes Microsoft's commitment to data privacy, security, and compliance in the context of AI Builder.

- **We secure your data**: We help protect your data with encryption at rest and in transit, rigorous physical security controls, and data isolation between tenants.​

- **Your data is private**: We don’t use your data except as you instruct. Our commitments to privacy include support for [General Data Protection Regulation](/compliance/regulatory/gdpr), [ISO/IEC 27018](/compliance/regulatory/offering-ISO-27018), and our [Data Protection Addendum](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA).​

- **You're protected against AI security risks**: We help safeguard against AI-focused risks such as harmful content and prompt injections.​

- **Your data isn’t used to train foundation models**: AI Builder uses your context to create relevant responses. Consistent with our other AI offers, prompts, responses, and data accessed aren't used to train foundation models.​

## Geo boundary compliance

For AI prompts where Azure OpenAI Service is available, customer data doesn't leave the geo boundary.​

If Azure OpenAI Service isn't available in a geo, admins have [granular controls](/power-platform/admin/geographical-availability-copilot#enable-data-movement-across-regions) to manage cross geo data movement per environment.​

Learn more about features available in a region in [Feature availability per region](availability-region.md).

For all AI Builder models or prompts, all data remains within the Azure Trust Boundary.

The data required to train the Azure model is encrypted during transfer, remains in the environment’s geography, and is deleted soon after the model is created. Data is only stored at rest in Dataverse, under your full control.

## AI prompts workflow

The following screenshot shows the AI prompts workflow. After AI Builder creates a prompt leveraging Dataverse, it can be consumed through Power Platform or Microsoft 365 products. To ensure responsible AI compliance of the prompt, AI Builder services communicate with Azure OpenAI and Azure AI Content Safety. The result is sent back as the prompt answer.

:::image type="content" source="media/ai-builder-architecture/aib-prompts-workflow.png" alt-text="Screenshot of the AI prompts workflow.":::

## Related information

[FAQ for Copilot data security and privacy for Dynamics 365 and Power Platform](/power-platform/faqs-copilot-data-security-privacy)
