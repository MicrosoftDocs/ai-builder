---
title: AI Builder licensing in Microsoft Copilot Studio - Message management
description: Learn about licensing and message management of AI Builder in Microsoft Copilot Studio
author: Antoine2F
contributors:
  - Antoine2F
  - v-aangie
ms.topic: conceptual
ms.collection: 
    - bap-ai-copilot
ms.date: 04/08/2025
ms.author: Antoine2F
ms.reviewer: angieandrews
---

> [!NOTE]
> This pages focuses on AI Builder **in Copilot Studio and Agent flows context**. The use of AI Builder - Prompts and Models - in Power Apps or Power Automate follows another licensing : [AI Builder licensing and credit management
](credit-management.md)

# AI Builder licensing in Microsoft Copilot Studio : Message management
Access to AI Builder features in  Copilot Studio within an environment requires Copilot Studio capacity : Messages.  
Message acquisition (through prepaid Packs) and assignment is explained here:
[Copilot Studio licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)

## AI Builder capabilities in Copilot Studio senarios
In Copilot Studio, there are several scenarios involving AI Builder capabilities:
 - use Prompts within Topics
 - use Prompts within Actions
 - use AI Models (Document Processing, Text recognition, ...) or Prompts within Agent flows

All these different scenarios consume Messages.

## Message consumption rates
Each AI Builder capability is mapped to one of these 4 Copilot Studio/AI Tools features : 
| Copilot Studio/AI Tools features         | Unit        |
|------------------------------------------|-------------|
|Text and generative AI tools (basic)      | response    |
|Text and generative AI tools (standard)   | response    |
|Text and generative AI tools (premium)    | response    |
| Content Processing Tools                 | page        |

Using an AI Builder capability will consume units of these features. For instance, extracting information from a 2 pages document within an Agent Flow will consume 2 pages of 'Content Document Processing'.  
The cost per unit is published in Licensing Guide [pdf](https://go.microsoft.com/fwlink/?linkid=2085130) and in this Copilot Studio documentation page: [Billing rates and management](https://learn.microsoft.com/microsoft-copilot-studio/requirements-messages-management#message-scenarios)

Here is the mapping between AI Builder capability and Copilot Studio features:
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
Prompts in Topics or Actions triggered from the Agent embedded Test panel are free.  
Prompts and Models in Agent flows always consume Messages, even when triggered from an Agent embedded Test panel, or from flow designer.
As soon as a classic flow is transformed into an Agent flows, AI Builder Prompts and Models within this flow begin consuming Messages instead of Credits.
Testing a prompt (within Prompt Builder) or a model (within the Model page) is free.

### Examples
###Agent with Prompts in Topics
An HR agent is configured with a 'Benefit' topic, which uses a Prompt (based on 4o mini) to retrieve specific information about sick days from a Dataverse table. An employee asks this agent about sick days. This triggers the Prompt. The size of input (included system prompt) and output is 4200 tokens (~16 000 characters). 
This employee's request has consumed 5 responses of "Text and generative AI tools (basic)" feature, so 0.5 Messages, plus the cost of the Copilot Studio classic answer or generative answer.

### Agent flow with Custom document processing
An agent flow is triggered when receiving email from a particular address. It process the attached file which contains 3 pages, using a custom Document processing model. 
This consumes 3 pages of "Content Processing Tools" feature, so 24 messages.  
This is in addition to the cost of the Agent flow actions. 






