---
title: AI Builder licensing and message management in Microsoft Copilot Studio
description: Learn about licensing and message management of AI Builder in Microsoft Copilot Studio
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.collection: 
    - bap-ai-copilot
ms.date: 04/09/2025
ms.author: antode
ms.reviewer: angieandrews
---

# AI Builder licensing in Microsoft Copilot Studio : Message management

> [!NOTE]
> This pages focuses on AI Builder in the **Copilot Studio and Agent flows context**. The use of AI Builder models and prompts in Power Apps or Power Automate is explained in [AI Builder licensing and credit management](credit-management.md).

Access to AI Builder features in Microsoft Copilot Studio within an environment requires Copilot Studio capacity, which uses the Message currency.  
Message acquisition through prepaid packs and assignment is explained in
[Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing).

## AI Builder capabilities in Copilot Studio scenarios

In Copilot Studio, several scenarios involve AI Builder capabilities:

 - Use Prompts within topics.
 - Use Prompts within actions.
 - Use AI Models (such as Document Processing and Text recognition) or prompts within agent flows.

All these scenarios consume messages.

## Message consumption rates

Each AI Builder capability maps to one of these four Copilot Studio/AI Tools features:
 
| Copilot Studio/AI Tools features         | Unit        |
|------------------------------------------|-------------|
|Text and generative AI tools (basic)      | response    |
|Text and generative AI tools (standard)   | response    |
|Text and generative AI tools (premium)    | response    |
| Content Processing Tools                 | page        |

Using an AI Builder capability consumes units of these features. For example, extracting information from a two-page document within an agent flow consumes two pages of **Content Document Processing**.  
The cost per unit is published in the [Licensing Guide (PDF)](https://go.microsoft.com/fwlink/?linkid=2085130) and in [Billing rates and management](/microsoft-copilot-studio/requirements-messages-management#message-scenarios).

Here is the mapping between AI Builder capabilities and Copilot Studio features:

 | AI Builder capability | Copilot Studio/AI Tools features | Unit |
|------------------------------------------|-------------|-------------|
| Prompt using gpt 4o-mini model      | Text and generative AI tools (basic)     | 1 response per 1K tokens*   |
| Prompt using gpt 4o model           | Text and generative AI tools (standard)  | 1 response per 1K tokens*   |
| Prompt using o1 model               | Text and generative AI tools (premium)   | 1 response per 1K tokens*   |
| Custom document processing model    | Content Processing Tools                 | 1 page                      |
| Invoice processing                  | Content Processing Tools                 | 1 page                      |
| Receipt processing                  | Content Processing Tools                 | 1 image = 1 page            |
| Identity document reader            | Content Processing Tools                 | 1 image = 1 page            |
| Business card reader                | Content Processing Tools                 | 1 image = 1 page            |
| Object Detection                    | Content Processing Tools                 | 1 page = 1 image            |
| Text Recognition                    | Text and generative AI tools (basic)     | 1 page = 1 response         |
| Sentiment analysis                  | Text and generative AI tools (basic)     | 1 response per 1K characters|
| Language detection                  | Text and generative AI tools (basic)     | 1 response per 1K characters|
| Key phrase extraction               | Text and generative AI tools (basic)     | 1 response per 1K characters|
| Prediction (scheduled)              | Text and generative AI tools (basic)     | 1 response per 5 rows       |
| Prediction (real time)              | Text and generative AI tools (basic)     | 1 response per row          |
| Text translation                    | Text and generative AI tools (standard)  | 1 response per 1K characters|
| Entity extraction (prebuilt)        | Text and generative AI tools (standard)  | 1 response per 1K characters|
| Entity extraction (custom)          | Text and generative AI tools (standard)  | 1 response per 1K characters|
| Category classification (custom)    | Text and generative AI tools (standard)  | 1 response per 1K characters|

## Message consumption rules

Prompts in topics or actions triggered from the agent-embedded test panel are free.  
Prompts and models in agent flows always consume messages, even when triggered from an agent-embedded test panel, or from the flow designer.
When a classic flow is transformed into an agent flow, AI Builder prompts and models within this flow begin consuming messages instead of credits.
Testing a prompt (within Prompt Builder) or a model (within the Model page) is free.

### Examples

The following examples illustrate the message consumption rules.

#### Agent with prompts in topics

An HR agent is configured with a **Benefit** topic, which uses a prompt (based on 4o mini) to retrieve specific information about sick days from a Dataverse table. An employee asks this agent about sick days. This triggers the prompt. The size of input (included system prompt) and output is 4200 tokens (~16,000 characters). 
This employee's request has consumed 5 responses of the **Text and generative AI tools (basic)** feature, which equals 0.5 Messages, plus the cost of the Copilot Studio classic answer or generative answer.

#### Agent flow with custom document processing

An agent flow is triggered when receiving email from a specific address. It processes the attached file, which contains 3 pages, using a custom document processing model. 
This consumes 3 pages of the **Content Processing Tools** feature, which equals 24 messages.  
This is in addition to the cost of the agent flow actions. 






