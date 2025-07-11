---
title: Human review for automation with a prompt
description: Learn about emphasizing human review for automation with a prompt.
author: ashbhati
contributors:
  - antrodfr
  - ashbhati
  - phil-cmd
  - v-aangie
ms.topic: article
ms.custom: bap-template
ms.date: 06/23/2025
ms.update-cycle: 180-days
ms.author: antrod
ms.reviewer: angieandrews
ms.collection: 
    - bap-ai-copilot
---

# Human review for automation with a prompt

This article explains the critical role of human review when running a prompt in Power Automate. Prompts use generative AI models powered by Azure OpenAI Service. Although these models are highly effective, they can sometimes generate misleading or fabricated information and are susceptible to prompt injection attacks.

> [!IMPORTANT]
>
> - AI Builder prompts are running on GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Prompt injection attacks

A prompt injection attack occurs when a third-party takes advantage of the model's inherent trust in all input sources. The attacker injects a prompt into content that a legitimate user asks the AI solution to interact with, leading to a change in the AI solution's output, and potentially, its actions.

Consider a scenario where a citizen developer uses a prompt to create responses to customer complaints collected from various platforms such as emails, social media, or forums. An attacker might insert a prompt into the content from one of these sources, deceiving the model into generating an unintended response. The response can be inappropriate, incorrect, or harmful. Sending incorrect information to customers might harm the company's reputation and customer relationships.  

## Fabrication in AI models

Fabrication, also known as hallucination, is another challenge faced by AI models, including generative AI models used by prompts. Fabrication occurs when the AI model generates information that isn't based on provided inputs or pre-existing data, essentially *inventing* or *hallucinating* information.

For instance, if the AI model is asked to generate a summary of a historical event based on a given text, it might include details or events that weren't mentioned in the source text. For example, a cloud flow creates a synopsis of a meeting based on the transcript of the recording. The input data includes details about the attendees, the articles discussed, and the decisions made. However, the model might generate a summary that includes an action item or a decision that was never discussed in the meeting. This situation is an instance of fabrication, where the model has *hallucinated* information that doesn't exist in the input data.

To mitigate the risk of fabrication, it's crucial to implement responsible AI practices. This includes rigorous testing of the prompt and the cloud flow, providing the model with as much grounding information as possible and finally implementing a robust system for human oversight.

## Address risks through responsible AI practices

We advocate for responsible AI practices as a means to reduce risks. Despite having strategies in place to moderate the content produced by the model, managing the model's propensity to generate fabricated responses or succumb to prompt injection attacks remains a complex challenge. We acknowledge these risks and reaffirm our commitment to human oversight and control.

In recognition of the necessity for seamless automation, we're proactively enhancing our safety systems and seeking a deeper understanding of these challenges.
Our objective is to further refine the generative AI models used by prompts with appropriate safety measures, in line with our principles of [responsible AI by design](https://blogs.microsoft.com/on-the-issues/2023/02/02/responsible-ai-chatgpt-artificial-intelligence/), returning control to developers wherever feasible.

## Related information

[FAQ for prompts and text generation capabilities](faqs-text-generation.md)
