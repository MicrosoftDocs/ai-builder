---
title: Licensing and Copilot Credits
description: Learn about licensing and Copilot Credits in AI tools in Microsoft Copilot Studio
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.contributor:
  - cyanderson
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 10/3/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Licensing and Copilot Credits

This article focuses on AI Tools/AI Builder capabilities in the Microsoft Copilot Studio and agent flows context. Learn how to use AI Tools/AI Builder models and prompts in Power Apps or Power Automate in [Licensing and AI Builder credits](credit-management.md).

Access to AI Tools/AI Builder capabilities in Copilot Studio within an environment requires Copilot Studio capacity, which uses the *Copilot Credit* currency. Learn about Copilot Credit acquisition through prepaid packs and assignment in [Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing).

## AI Tools/AI Builder capabilities in Copilot Studio scenarios

In Copilot Studio, several scenarios involve AI Tools/AI Builder capabilities:

- Use prompts within topics.
- Use prompts within actions.
- Use AI models (such as *document processing* or *text recognition*) or prompts within agent flows.

All these scenarios consume Copilot Credits.

## Copilot Credit consumption rates

Each AI Tools/AI Builder capability maps to one of the following Copilot Studio/AI Tools features.

| Copilot Studio/AI tools features         | Unit        | Rate per unit|
|------------------------------------------|-------------|-------------------|
|Text and generative AI tools (basic)      | response¹    | 0.1 Copilot Credit|
|Text and generative AI tools (standard)   | response¹    | 1.5 Copilot Credit|
|Text and generative AI tools (premium)    | response¹    | 10 Copilot Credits|
| Content processing tools                 | page        | 8 Copilot Credits |  

¹ 1 response is either 1K tokens, or 1K characters, or 1 page, depending on the capability. Review the following table.

Using an AI Tool/AI Builder capability consumes units of these features. For example, extracting information from a two-page document within an agent flow consumes two pages of *content document processing*.

The cost per unit is also published in [Billing rates and management](/microsoft-copilot-studio/requirements-messages-management#copilot-credits-and-events-scenarios).

The following table shows the mapping between AI Tools/ AI Builder capabilities and Copilot Studio features.

 | AI Tools/AI Builder capability                   | Copilot Studio features         |                  Rate and Unit |
|------------------------------------------|------------------------------------------|-----------------------------|
| Prompt using models in Basic category <BR>like GPT-4.1 mini          | Text and generative AI tools (basic)     | 0.1 Copilot Credit per 1K tokens*   |
| Prompt using models in Standard category <BR>like GPT-4.1, GPT-5 chat    | Text and generative AI tools (standard)  | 1.5 Copilot Credit per 1K tokens*   |
| Prompt using models in Premium category <BR>like o3, GPT-5 reasoning    | Text and generative AI tools (premium)   | 10 Copilot Credits per 1K tokens*   |
| Custom document processing model    | Content processing tools                 | 8 Copilot Credits per page                    |
| Invoice processing                  | Content processing tools                 |  8 Copilot Credits per page |
| Receipt processing                  | Content processing tools                 | 8 Copilot Credits per page or image          |
| Identity document reader            | Content processing tools                 | 8 Copilot Credits per page or image          |
| Business card reader                | Content processing tools                 | 8 Copilot Credits per page or image            |
| Object detection                    | Content processing tools                 | 8 Copilot Credits per page or image            |
| Text recognition                    | Text and generative AI tools (basic)     | 0.1 Copilot Credit  per page      |
| Sentiment analysis                  | Text and generative AI tools (basic)     |  0.1 Copilot Credit per 1K characters|
| Language detection                  | Text and generative AI tools (basic)     | 0.1 Copilot Credit per 1K characters|
| Key phrase extraction               | Text and generative AI tools (basic)     |  0.1 Copilot Credit per 1K characters|
| Prediction (scheduled)              | Text and generative AI tools (basic)     |  0.1 Copilot Credit per 5 rows       |
| Prediction (real time)              | Text and generative AI tools (basic)     |  0.1 Copilot Credit per row          |
| Text translation                    | Text and generative AI tools (standard)  |  1.5 Copilot Credits per 1K characters|
| Entity extraction (prebuilt)        | Text and generative AI tools (standard)  |  1.5 Copilot Credits per 1K characters|
| Entity extraction (custom)          | Text and generative AI tools (standard)  |  1.5 Copilot Credits per 1K characters|
| Category classification (custom)    | Text and generative AI tools (standard)  |  1.5 Copilot Credits per 1K characters|
| Code execution (read complex file/sources)   | Text and generative AI tools (premium)  |  10 Copilot Credits per code execution |
| Code generation (response/output generation)   | Text and generative AI tools (premium)  |  10 Copilot Credits per code generation |

\* Sum of input (incl. system prompt) and output (incl. reasoning) tokens. Learn more in [Prompt tokens](licensing-prompt-tokens.md).

## Copilot Credit consumption rules

The following list contains Copilot Credit consumption rules.

- Prompts in topics or actions triggered from the agent-embedded test panel are free.
- Prompts and models in agent flows always consume Copilot Credits, even when triggered from an agent-embedded test panel, or from the flow designer.
- When a classic flow is transformed into an agent flow, AI Builder/AI Tools prompts and models within this flow begin consuming Copilot Credit instead of AI Builder credits.
- Testing a prompt (within prompt builder) or a model (within the **AI models** page) is free.
- Prompts in agents or agent flows consume Copilot Credits, even with models in preview.

## Train a custom model to be used in an agent flow

Training a custom model (for example, *document processing* and *object detection*) happens in the Power Apps or Power Automate portal, in the **AI models** page. Training doesn't require AI Builder credits or Copilot Credits.

Your published model is available in an agent flow and consumes Copilot Credits.

## Copilot Credit consumption examples

The following examples explain the Copilot Credit consumption rules.

### Agent with prompts in topics

A Human Resources (HR) agent is configured with a **Benefit** topic, which uses a prompt (based on 4.1 mini) to retrieve specific information about sick days from a Dataverse table. An employee asks this agent about sick days. This triggers the prompt. The size of the input (including the system prompt) and output is 4,200 tokens (about 16,000 characters).

This employee's request consumed five (5) responses of the **text and generative AI tools (basic)** feature, which equals 0.5 Copilot Credits, plus the cost of the Copilot Studio classic answer or generative answer.

### Agent cloud flow with custom document processing

An agent cloud flow is triggered when receiving email from a specific address. It processes the attached file, which contains three (3) pages, using a custom document processing model.

This consumes three (3) pages of the content processing tools feature, which equals 24 Copilot Credits. This is in addition to the cost of the agent flow actions.
