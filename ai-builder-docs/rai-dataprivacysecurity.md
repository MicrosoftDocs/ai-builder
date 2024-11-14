---
title: Data, privacy, and security for AI Builder
description: AI Builder responsible AI data, privacy and security overview
author: jekom1
contributors: 
  - jekom1
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 11/5/2024
ms.author: jelenak
ms.reviewer: angieandrews
---

# Data, Privacy, and Security

This article provides details regarding how data provided by you to AI Builder is processed, used, and stored. AI Builder stores and processes data to provide the service and allow you to monitor its use. Behind the scenes, AI Builder generates or uses Azure AI models for most scenarios.

![AIB Architecture](https://github.com/user-attachments/assets/b134645a-9680-49dc-b911-0cf37a0cefcf)


> [!IMPORTANT]
> Your input or output data, your embeddings, and your training data:
> - are NOT available to other customers.
> - are NOT available to OpenAI.
> - are NOT used to improve OpenAI or Azure AI models.
> - are NOT used to train, retrain, or improve Azure AI foundation models.
> - are NOT used to improve any Microsoft or 3rd party products or services without your permission or instruction.

## Enterprise data protection

**We secure your data**: We help protect your data with encryption at rest and in transit, rigorous physical security controls, and data isolation between tenants.​

**Your data is private**: We won’t use your data except as you instruct. Our commitments to privacy include support for [GDPR](https://learn.microsoft.com/compliance/regulatory/gdpr), [ISO/IEC 27018](https://learn.microsoft.com/compliance/regulatory/offering-ISO-27018), and our [Data Protection Addendum](https://www.microsoft.com/licensing/docs/view/Microsoft-Products-and-Services-Data-Protection-Addendum-DPA).​

**You're protected against AI security risks**: We help safeguard against AI-focused risks such as harmful content and prompt injections.​

**Your data isn’t used to train foundation models**: AI Builder uses the user’s context to create relevant responses. Consistent with our other AI offers, prompts, responses, and data accessed, aren't used to train foundation models.​

## Geo boundary compliance

For AI prompts, where Azure Open AI is available, customer data does not leave geo boundary.​
If Azure Open AI is not available in a geo, admins have [granular controls](https://review.learn.microsoft.com/power-platform/admin/geographical-availability-copilot#enable-data-movement-across-regions) to manage cross geo data movement per environment.​

For all AI Builder models or prompts, all data remains within the Azure Trust Boundary.
The data required to train the Azure model is encrypted during transfer, remains in the environment’s geography, and is deleted soon after the model has been created. Data is only stored at rest in Dataverse, under your full control.
