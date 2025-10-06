---
title: Copilot Credits based licensing
description: Learn about the licensing system in 2025 for AI Builder.
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 10/03/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Copilot Credits based licensing

On November 1, 2025, there will be a major change to AI Builder licensing. This article explains the change.  

AI Builder features (AI prompts and AI models) are available in two different contexts:

- **Power Automate and Power Apps context**: Allows you to enrich cloud flows or apps with AI prompts or AI models like document processing tools.
- **Microsoft Copilot Studio context**: Allows you to enrich agents with AI prompts or agent flows with AI prompts or AI models like document processing tools. In this context, AI Builder features are sometimes called *AI tools*.

In Copilot Studio context, AI Builder features are licensed based on Copilot Credits. This doesn't change.  

In Power Automate and Power Apps context, AI Builder features are licensed exclusively based on AI Builder credits up to November 1, 2025.  

Starting November 1, 2025, AI Builder features in Power Automate and Power Apps context will also be licensed based on Copilot Credits. Existing customers with paid or seeded AI Builder credits can continue using their AI Builder credits. When AI Builder credits are in overage or not present, the licensing system checks Copilot Credits availability, and allows the feature to run, if any.

New customers aren't able to purchase paid AI Builder Capacity Add-on, and no longer receive seeded AI Builder credits in Power Automate premium licenses. They need Copilot Credits to access and run AI Builder features in Power Automate and Power Apps context. Existing customers keep AI Builder capacity linked to their Add-on licenses, as long as they're active. Existing customers keep their number of seeded AI Builder credits for 1 year (this number is based on a snapshot taken on October 31). Seeded credits will be removed on November 1, 2026.

The change comes along with many simplifications:

- Access to AI prompts and AI models page in Power Automate and Power Apps portal doesn't require any AI Builder credits or Copilot Credits.
- All custom model trainings are now free.
- Binary classification and business card models are now free.
- AI Builder trials are no longer available.
- There's no distinction between simple and important overage.
- There are no longer extension requests.

## Dual mode for existing customers: Check AI Builder credits first, then fall back to Copilot Credits

This dual mode allows business continuity. All existing cloud flows and apps continue running their AI Builder features based on existing AI Builder credit assignments to their environments.  

When an environment is in overage, maker access isn't blocked. An email is still sent to admins, but extension requests aren't possible, and the licensing system tries to access Copilot Credits. If there are no Copilot Credits available in this environment, the AI Builder feature is blocked without waiting for 'important overage'. If there are Copilot Credits available in this environment, the AI Builder feature runs successfully and consumes these Copilot Credits.

## New customers exclusively rely on Copilot Credits for AI Builder features

It was already the case for AI Builder features in Copilot Studio context. For new customers, it's also the case for AI Builder features in Power Apps and Power Automate context.

## Copilot Credits management

Copilot Credits can be purchased as prepaid packs, and are also available as pay-as-you-go.
Prepaid pack Copilot Credits can be assigned to environments. Each environment has a toggle to indicate whether it can consume unassigned Copilot Credits or not, called 'Draw from the available capacity in my tenant'.

### Copilot Credit rate card

Each AI Builder model or prompt is consuming one of these four Copilot features:  

| Feature                                | Cost per page/image/1K characters/1K tokens | Prompts or models that consume this feature |  
|----------------------------------------|---------------------------------------------|------------------------------------------|  
|Text and generative AI tools (basic)    | 0.1 Copilot Credit                          |Prompts using basic large language model (LLM),  text recognition, sentiment analysis, language detection, or key phrase extraction. |  
|Text and generative AI tools (standard) | 1.5  Copilot Credits                        |Prompts using standard LLM, text translation, entity extraction, or category classification. |  
|Text and generative AI tools (premium)  | 10   Copilot Credits                        |Prompts using premium LLM. |  
|Content processing tools                | 8  Copilot Credits                          |Custom document processing, invoice processing, receipt processing, identity document reader, or object detection. |  

For each prompt using the 'per 1K tokens' unit, the licensing system computes the size of input + output (including system prompt, reasoning) in tokens and rounds it up. This provides the number of 'Feature' that will be consumed.

**Example**: A prompt based on a standard model with 3.1K tokens in input and 1.5K tokens in output consumes 5 * 1.5 Copilot Credits = 7.5 Copilot Credits.

Custom document processing, invoice processing, receipt processing, identity document reader, object detection, and text recognition are using the 'per page' or 'per image' unit.

**Example**: Processing a document with 3 pages using a custom document processing model consumes 3 * 8 Copilot Credits = 24 Copilot Credits.

Sentiment analysis, language detection, key phrase extraction, text translation, entity extraction, and category classification are using the 'per 1K characters' unit (rounded up).

**Example**: Translating 3.4K characters consumes 4* 1.5 Copilot Credits = 6 Copilot Credits.

## Consumption monitoring

Copilot Credit consumption now includes consumption coming from Power Automate and Power Apps context. It can be monitored in the [Power Platform admin center](https://admin.powerplatform.microsoft.com) > **Copilot Studio** section. AI Builder credit consumption continues to be monitored in the [Power Platform admin center](https://admin.powerplatform.microsoft.com) > **Licensing** > **Capacity add-ons** section.  

For environments using AI Builder credits first, then Copilot Credits, admins need to check both reports. However, the AI Builder activity in Power Automate helps you understand whether a particular action was billed in AI Builder credit or Copilot Credit.

Banners in the [Power Platform admin center](https://admin.powerplatform.microsoft.com) add-ons section and emails continue to inform admins about AI Builder credit overages.

## End of AI Builder trials

Users who started AI Builder trials are able to use them until the end of the trial period (30 days), within the consumption limit (200,000 AI Builder credits).

Starting November 1, 2025, new customers can't start or renew AI Builder trials. They need to use Copilot Credits to use AI Builder features.  

## End of Extension requests

Extension requests are available up to the end of October 2025.

Starting November 1, 2025, environments in overage block the run of AI Builder features unless Copilot Credits are available, or an admin allocates more AI Builder credits to the environment. This blocking is for business runs only, using features in Power Apps or Power Automate cloud flows. It doesn't impact maker access to AI Builder portal pages such as training or quick testing models.

## Ungated access to AI models and prompts in Power Automate and Power Apps portals

Makers can train custom models and test prebuilt and custom models or prompts in the Power Automate and Power Apps portal, without any AI Builder credits or Copilot Credits. This is also true when environment is in overage of AI Builder credits. Admins can block access to prompts using a specific toggle in [Power Platform admin center](https://admin.powerplatform.microsoft.com).

## AI tool Capability Pricing Comparison Table

|AI tool capability                            | Unit | Copilot Studio feature| Copilot Credit rate| $ cost *| AI Builder credit rate| $ cost **| Number of Copilot packs for 1 AI Builder Add-on|
|----------------------------------------------|------|-----------------------|--------------------|-----|---------------------|--|---|
|Prompt (basic LLM model)                      |1k tokens| Text and generative AI tools (basic) |0.1 | 0.0008|1 (input), 3 (output) |0.0006 ¹|  4|
| Prompt (standard LLM model)                  | 1k tokens  | Text and generative AI tools (standard)        | 1.5 | 0.012 | 20 (input), 60 (output)      | 0.012 ¹                   | 3|
| Prompt (premium LLM model)                   | 1k tokens  | Text and generative AI tools (premium)         | 10                   | 0.08                     | 140 (input), 560 (output)    | 0.091 ¹                   |3|
| Custom Document Processing                   | 1 page     | Content Processing Tools                        | 8                    | 0.064                    | 100                           | 0.05                     |4|
| Text translation                             | 1k chars   | Text and generative AI tools (standard)        | 1.5                  | 0.012                    | 22                            | 0.011                    |3|
| Simple Text analysis: sentiment analysis, <BR>language detection, key phrase extraction | 1k chars   | Text and generative AI tools (basic)           | 0.1                  | 0.0008                  | 2                             | 0.001                    |2|
| Advanced Text analysis: category classification, <BR>entity extraction             | 1k chars   | Text and generative AI tools (standard)        | 1.5                  | 0.012                    | 20                            | 0.01                     |3|
| Text recognition (OCR)                       | 1 page     | Text and generative AI tools (basic)           | 0.1                  | 0.0008                   | 3                             | 0.0015                   |2|
| Receipt, Invoice, Identity document analysis | 1 page     | Content Processing Tools                        | 8                    | 0.064                    | 32                            | 0.016                    |10|
| Contract processing, Health insurance card <BR>processing, Image description ²      | 1 image    | Content Processing Tools                        | 8                    | 0.064                    | 32                            | 0.016                    |10|
| Object detection                             | 1 image    | Content Processing Tools                        | 8                    | 0.064                    | 8                             | 0.004                    |40|
| Business card reader, Prediction             | n/a        |     n/a                                           | free                 |    n/a                      | free                          |   n/a                       | n/a |

\* Using yearly prepaid Copilot Studio pack<br/>
** Using yearly prepaid AI Builder Add-on  
¹ Based on 900 input tokens + 100 output tokens  
² Free as long as in preview  
 
