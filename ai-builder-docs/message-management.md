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
ms.date: 11/1/2025
ms.update-cycle: 180-days
ms.author: antode
ms.reviewer: angieandrews
---

# Licensing and Copilot Credits

This article focuses on the management of Copilot Credits to use AI tools/AI Builder capabilities in the Microsoft Copilot Studio, Power Automate, and Power apps context.
Copilot Credits are mandatory to use AI tools/AI Builder capabilities in Copilot Studio agents, and agent flows.
In Power Automate and Power Apps context, Copilot Credits can be used in conjunction with AI Builder credits, or as the only licensing mechanism.

Learn how to use AI Builder credits in Power Apps or Power Automate context in [Licensing and AI Builder credits](credit-management.md).  

Access to AI tools/AI Builder capabilities in Copilot Studio within an environment requires Copilot Studio capacity. 
Access to AI tools/AI Builder capabilities in Power Apps or Power Automate within an environment without AI Builder credit capacity requires Copilot Studio capacity. 

Copilot Studio capacity uses the *Copilot Credit* currency. 
Learn about Copilot Credit acquisition through Copilot Studio license (prepaid packs) or pay go or prepurchase packs in [Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing).
The same documentation will provide details about Copilot Credit allocation, and Copilot Credit consumption monitoring.

## AI Tools/AI Builder capabilities in Copilot Studio scenarios

In Copilot Studio, several scenarios involve AI Tools/AI Builder capabilities:

- Use prompts within topics.
- Use prompts within actions.
- Use AI models (such as *document processing* or *text recognition*) or prompts within agent flows.

All these scenarios consume Copilot Credits.

## AI Tools/AI Builder capabilities in Power Apps or Power Automate

In Power Apps and Power Automate, prompts and models capabilities will consume Copilot Studio when there is no AI Builder credits available, or when AI Builder credits computed consumption is in overage compared to initial capacity. 

- Use prompts (custom or prebuilt), or AI functions within apps or cloud flows.
- Use AI models (such as *document processing* or *text recognition*) or prompts within cloud flows.

## Copilot Credit consumption rates

Each AI Tools/AI Builder capability maps to one of the following Copilot Studio/AI Tools features.

| Copilot Studio/AI tools features         |  Rate per unit                                                          |
|------------------------------------------|------------------------------------------------------------------------------|
|Text and generative AI tools (basic)      |  0.1 Copilot Credit per 1K tokens, or 1K characters, or 1 image, or 1 page   |
|Text and generative AI tools (standard)   |  1.5 Copilot Credit per 1K tokens, or 1K characters, or 1 image, or 1 page   |
|Text and generative AI tools (premium)    |  10 Copilot Credits per 1K tokens, or 1K characters, or 1 image, or 1 page   |
| Content processing tools                 |  8 Copilot Credits per image or per page                                     |  


Using an AI tool/AI Builder capability consumes units of these features. For example, extracting information from a two-page document within an agent flow consumes two pages of *content document processing*.

The cost per unit is also published in [Billing rates and management](/microsoft-copilot-studio/requirements-messages-management#copilot-credits-and-events-scenarios).

The rate of each AI tools/ AI Builder capabilities is detailed in [AI Builder capability rate table](administer-licensing.md#aibuildercapabilityrate-table)

## Copilot Credit monitoring
In addition to the generic Copilot Credit monitoring ( see [Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing)), AI tools/AI Builder capabilities can be monitored in real time:

Administrators can access the [AI Builder Activity](activity-monitoring.md) page in the Power Automate portal, showing each consumption, either in AI Builder credits or in Copilot Credits. 

## Copilot Credit consumption rules 

The following list contains Copilot Credit consumption rules.

- Prompts in topics or actions triggered from the agent-embedded test panel are free.
- Prompts and models in agent flows always consume Copilot Credits, even when triggered from an agent-embedded test panel, or from the flow designer.
- When a classic flow is transformed into an agent flow, AI Builder/AI Tools prompts and models within this flow can only consume Copilot Credit (prompts and models in classic flows try to consume first AI Builder credits, then Copilot Credits)
- Testing a prompt (within prompt builder) or a model (within the **AI models** page) is free.
- Prompts in agents or agent flows consume Copilot Credits, even with models in preview.

## Train a custom model to be used in an agent flow

Training a custom model (for example, *document processing* and *object detection*) happens in the Power Apps or Power Automate portal, in the **AI models** page. Training doesn't require AI Builder credits or Copilot Credits.

Your published model is then available in agent flow, where it will consume Copilot Credits.

## Copilot Credit consumption examples

The following examples explain the Copilot Credit consumption rules.

### Agent with prompts in topics

A Human Resources (HR) agent is configured with a **Benefit** topic, which uses a prompt (based on a basic model) to retrieve specific information about sick days from a Dataverse table. An employee asks this agent about sick days. This triggers the prompt. The size of the input (including the system prompt) and output is 4,200 tokens (about 16,000 characters).

This employee's request consumed five (5) responses of the **text and generative AI tools (basic)** feature, which equals 0.5 Copilot Credits, plus the cost of the Copilot Studio classic answer or generative answer.

### Agent cloud flow with custom document processing

An agent cloud flow is triggered when receiving email from a specific address. It processes the attached file, which contains three (3) pages, using a custom document processing model.

This consumes three (3) pages of the content processing tools feature, which equals 24 Copilot Credits. This is in addition to the cost of the agent flow actions.
