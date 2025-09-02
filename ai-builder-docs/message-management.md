---
title: "AI Builder licensing in Microsoft Copilot Studio: Copilot credit management"
description: Learn about licensing and Copilot credit management of AI Builder in Microsoft Copilot Studio
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: article
ms.collection: 
    - bap-ai-copilot
ms.date: 09/02/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# AI Builder licensing in Microsoft Copilot Studio: Copilot credit management

This article focuses on AI Builder in the Microsoft Copilot Studio and agent flows context. Learn how to use AI Builder models and prompts in Power Apps or Power Automate in [AI Builder licensing and credit management](credit-management.md).

Access to AI Builder features in Copilot Studio within an environment requires Copilot Studio capacity, which uses the *Copilot credit* currency. Learn about Copilot credit acquisition through prepaid packs and assignment in [Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing).

## AI Builder capabilities in Copilot Studio scenarios

In Copilot Studio, several scenarios involve AI Builder capabilities:

- Use prompts within topics.
- Use prompts within actions.
- Use AI models (such as *document processing* or *text recognition*) or prompts within agent flows.

All these scenarios consume Copilot credits.

## Copilot credit consumption rates

Each AI Builder capability maps to one of the following Copilot Studio/AI Tools features.
 
| Copilot Studio/AI tools features         | Unit        |
|------------------------------------------|-------------|
|Text and generative AI tools (basic)      | response    |
|Text and generative AI tools (standard)   | response    |
|Text and generative AI tools (premium)    | response    |
| Content processing tools                 | page        |

Using an AI Builder capability consumes units of these features. For example, extracting information from a two-page document within an agent flow consumes two pages of *content document processing*.

The cost per unit is published in [Billing rates and management](/microsoft-copilot-studio/requirements-messages-management#message-scenarios).

The following table shows the mapping between AI Builder capabilities and Copilot Studio features.

 | AI Builder capability                   | Copilot Studio/AI Tools features         |                        Unit |
|------------------------------------------|------------------------------------------|-----------------------------|
| Prompt using GPT-4.1 mini model          | Text and generative AI tools (basic)     | 1 response per 1K tokens*   |
| Prompt using GPT-4.1, GPT-5 chat model   | Text and generative AI tools (standard)  | 1 response per 1K tokens*   |
| Prompt using o3, GPT-5 reasoning model   | Text and generative AI tools (premium)   | 1 response per 1K tokens*   |
| Custom document processing model    | Content processing tools                 | 1 page                      |
| Invoice processing                  | Content processing tools                 | 1 page                      |
| Receipt processing                  | Content processing tools                 | 1 image = 1 page            |
| Identity document reader            | Content processing tools                 | 1 image = 1 page            |
| Business card reader                | Content processing tools                 | 1 image = 1 page            |
| Object detection                    | Content processing tools                 | 1 page = 1 image            |
| Text recognition                    | Text and generative AI tools (basic)     | 1 page = 1 response         |
| Sentiment analysis                  | Text and generative AI tools (basic)     | 1 response per 1K characters|
| Language detection                  | Text and generative AI tools (basic)     | 1 response per 1K characters|
| Key phrase extraction               | Text and generative AI tools (basic)     | 1 response per 1K characters|
| Prediction (scheduled)              | Text and generative AI tools (basic)     | 1 response per 5 rows       |
| Prediction (real time)              | Text and generative AI tools (basic)     | 1 response per row          |
| Text translation                    | Text and generative AI tools (standard)  | 1 response per 1K characters|
| Entity extraction (prebuilt)        | Text and generative AI tools (standard)  | 1 response per 1K characters|
| Entity extraction (custom)          | Text and generative AI tools (standard)  | 1 response per 1K characters|
| Category classification (custom)    | Text and generative AI tools (standard)  | 1 response per 1K characters|

## Copilot credit consumption rules

The following list contains Copilot credit consumption rules.

- Prompts in topics or actions triggered from the agent-embedded test panel are free.
- Prompts and models in agent flows always consume Copilot credits, even when triggered from an agent-embedded test panel, or from the flow designer.
- When a classic flow is transformed into an agent flow, AI Builder prompts and models within this flow begin consuming Copilot credit instead of AI Builder credits.
- Testing a prompt (within prompt builder) or a model (within the **AI models** page) is free.
- Prompts in agents or agent flows consume Copilot credits, even with models in preview.

## Train a custom model to be used in an agent flow

Training a custom model (for example, *document processing* and *object detection*) happens in the Power Apps or Power Automate portal, in the **AI models** page. It requires access to AI Builder credits during training. This access can be removed once the model is published.

For example, to train a custom document processing model, you can assign one (1) AI Builder credit to your environment, train and publish the model, then remove this assigned AI Builder credit.

Your published model is available in an agent flow and consumes Copilot credits.

## Copilot credit consumption examples

The following examples explain the Copilot credit consumption rules.

### Agent with prompts in topics

A Human Resources (HR) agent is configured with a **Benefit** topic, which uses a prompt (based on 4.1 mini) to retrieve specific information about sick days from a Dataverse table. An employee asks this agent about sick days. This triggers the prompt. The size of the input (including the system prompt) and output is 4,200 tokens (about 16,000 characters).

This employee's request consumed five (5) responses of the **text and generative AI tools (basic)** feature, which equals 0.5 Copilot credits, plus the cost of the Copilot Studio classic answer or generative answer.

### Agent cloud flow with custom document processing

An agent cloud flow is triggered when receiving email from a specific address. It processes the attached file, which contains three (3) pages, using a custom document processing model.

This consumes three (3) pages of the content processing tools feature, which equals 24 Copilot credits. This is in addition to the cost of the agent flow actions.
