---
title: Prompts overview
description: Learn about prompt engineering and other key concepts to help you create powerful applications that can generate text from your input.
author: phil-cmd
contributors:
  - ashbhati
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 06/13/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Overview of prompts

This article explains prompts and prompt engineering as key concepts to help you create powerful generative AI capabilities that can be leveraged across Power Platform.

A prompt is a natural language instruction that tells a large language model (LLM) to perform a task. The process is also known as *instruction tuning*. The model follows the prompt to determine the structure and content of the text it needs to generate. Prompt engineering is the process of creating and refining the prompt used by the model.

AI Builder provides a prompt building user experience that allows makers to build, test, and save reusable prompts.

> [!IMPORTANT]
> - AI Builder prompts use GPT-3.5-Turbo or GPT-4 models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new). 
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Prerequisites

- You have a basic understanding of how to write prompts. To learn more, go to the [AI Builder Prompting Guide](aka.ms/promptguide).
- Your environment is in the list of [available regions](availability-region.md).
- You have a Power Apps or Power Automate license.
- A Microsoft Dataverse database is installed on the environment.
- You have an AI Builder add-on.

## What a prompt is and how to use it

Think of a prompt as a task or a goal you give to the large language model (LLM). With prompt builder, you can build, test, and save your custom prompts. You can also use input variables and Dataverse data to provide dynamic context data at runtime. You can share these prompts with others and use them in Power Automate, Power Apps, or Copilot Studio. For instance, you could make a prompt to pick out action items from your company emails and use it in a Power Automate flow to build an email processing automation.

Prompt builder enables makers to devise custom prompts that cater to their specific business needs using natural language. These prompts can be employed for many tasks or business scenarios, such as summarizing content, categorizing data, extracting entities, translating languages, assessing sentiment, or formulating a response to a complaint.

Prompts can be integrated into flows to build intelligent hands-off automation. Makers can also build advanced generative AI capabilities for their applications by describing them as natural language prompts. These prompts can also be used to extend a copilot action and topics, thereby streamlining your daily business operations and boosting efficiency.

## Human oversight

Human oversight is an important step when working with content generated from a GPT model. Large language models like GPT are trained on huge amounts of data. AI-generated content can contain errors and biases. A human should review it before you post it online, send it to a customer, or use it to inform a business decision. Human oversight helps not only to identify potential errors and biases, but also to make sure the content is relevant to the intended use case and aligns with the company's values.

Human review can also help to identify any issues with the GPT model itself. For example, if the model is generating content that isn't relevant to the intended use case, then you might need to adjust the prompt.

## Responsible AI

We're committed to creating [responsible AI](https://blogs.microsoft.com/on-the-issues/2023/02/02/responsible-ai-chatgpt-artificial-intelligence/) by design. Our work is guided by a [core set of principles](https://www.microsoft.com/ai/responsible-ai): fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability. We're putting these principles into practice across the company to develop and deploy AI that has a positive impact on society. We take a comprehensive approach, combining innovative research, exceptional engineering, and responsible governance. Alongside OpenAI's leading research on AI alignment, we're advancing a framework for the safe deployment of our own AI technologies aimed to help guide the industry toward more responsible outcomes.

[Learn more about transparency in the Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?context=%2Fazure%2Fcognitive-services%2Fopenai%2Fcontext%2Fcontext)

### See also

- [Create a prompt](create-a-custom-prompt.md)
- [Human review for automation with a prompt](azure-openai-human-review.md)

