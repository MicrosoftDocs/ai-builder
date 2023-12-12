---
title: Prompts Overview
description: Learn about prompt engineering and other key concepts to help you create powerful applications that can generate text from your input.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 12/07/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Overview of prompts

This article explains prompt engineering and other key concepts to help you create powerful applications that can generate text from your input. Prompt is a natural language instruction that tells a large language model (LLM) to perform a task, the process also known as "Instruction tuning". The GPT model follows the prompt to determine the structure and content of the text it needs to generate. Prompt engineering is the process of creating and refining the instruction  that's used to generate text with the GPT text generation capability.

Prompt builder is a prompt engineering tool from AI Builder. This tool lets makers write and test prompts for the GPT model.

> [!IMPORTANT]
> - This capability is [limited to some regions](availability-region?branch=main#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Prerequisites

- Have a basic understanding of how to write prompts.
- Your environment is in the United States.
- You have a Power Apps or Power Automate license.
- A Microsoft Dataverse database is installed on the environment.
- You have an AI Builder add-on. 

## What a prompt is and how to use it

Think of a prompt as a task or a goal you give to the large language model (LLM). With prompt builder, you can build, test, and save your custom prompts. You can also use input variables to provide dynamic context data at runtime. You can share these prompts with others and use them in Power Automate, Power Apps, or Copilot Studio. For instance, you could make a prompt to pick out action items from your company emails and use it in a Power Automate flow to build an email processing automation.

Prompt builder enables makers to devise custom prompts that cater to their specific business needs using natural language. These prompts can be employed for a variety of tasks or business scenarios, such as summarizing content, categorizing data, extracting entities, translating languages, assessing sentiment, or formulating a response to a complaint.

Prompts can be integrated into flows to build intelligent hands-off automation. Makers can also build advanced generative AI capabilities for their applications by describing them as natural language prompts. These prompts can be used to extend a custom copilot, thereby streamlining your daily business operations and boosting efficiency."

## Human oversight

Human oversight is an important step when working with content that's generated from a GPT model. Large language models like GPT are trained on huge amounts of data. AI-generated content can contain errors and biases. A human should review it before it's posted online, sent to a customer, or used to inform a business decision. Human oversight helps not only to identify potential errors and biases, but also to make sure the content is relevant to the intended use case and aligns with the company's values.

Human review can also help to identify any issues with the GPT model itself. For example, if the model is generating content that isn't relevant to the intended use case, then you may need to adjust the prompt.

## Responsible AI

We're committed to creating [responsible AI](https://blogs.microsoft.com/on-the-issues/2023/02/02/responsible-ai-chatgpt-artificial-intelligence/) by design. Our work is guided by a [core set of principles](https://www.microsoft.com/ai/responsible-ai): fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability. We're putting these principles into practice across the company to develop and deploy AI that has a positive impact on society. We take a comprehensive approach, combining innovative research, exceptional engineering, and responsible governance. Alongside OpenAI's leading research on AI alignment, we're advancing a framework for the safe deployment of our own AI technologies that's aimed to help guide the industry toward more responsible outcomes.

[Learn more about transparency in the Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?context=%2Fazure%2Fcognitive-services%2Fopenai%2Fcontext%2Fcontext)


