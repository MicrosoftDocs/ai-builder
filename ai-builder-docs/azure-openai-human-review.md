---
title: Human review for automation with a prompt
description: Learn about emphasizing human review for automation with a prompt.
author: phil-cmd
contributors:
  - ashbhati
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: bap-template
ms.date: 1/10/2024
ms.author: plarrue
ms.reviewer: angieandrews
---

# Human review for automation with a prompt

This article emphasizes the critical role of human review in deploying the [Create text with GPT](azure-openai-textgen.md) feature in Power Automate. This feature utilizes the *text generation* model from AI Builder, powered by Azure OpenAI Service. Although these models are highly effective, they can sometimes generate misleading or fabricated information and are susceptible to prompt injection attacks.

> [!IMPORTANT]
>
> - AI Builder prompts are running on GPT-3.5 Turbo model powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Prompt injection attacks

A prompt injection attack occurs when a third-party exploits the model's inherent trust in all input sources. The attacker injects a prompt into content that a legitimate user asks the AI solution to interact with, leading to an alteration in the AI solution's output, and potentially, its actions.

For instance, consider a scenario where a citizen developer uses the **Create text with GPT** action to formulate responses to customer complaints collected from various platforms such as emails, social media, or forums. An attacker could insert a prompt into the content from one of these sources. This scenario could deceive the model into generating a response that deviates from the intended one. Inappropriate, incorrect, or even harmful responses are sent to customers as a result, negatively impacting the company’s reputation and customer relationships.

## Fabrication in AI models

Fabrication, also known as hallucination, is another challenge faced by AI models, including the text generation model. This phenomenon occurs when the AI model generates information that isn't based on provided inputs or pre-existing data, essentially *inventing* or *hallucinating* information.

For instance, if the AI model is asked to generate a summary of a historical event based on a given text, it might include details or events that weren't mentioned in the source text, or even facts that are historically incorrect. For example, a flow creates a synopsis of a meeting based on transcript of the recording. The input data includes details about the attendees, the articles discussed, and the decisions made. However, the model might generate a summary that includes an action item or a decision that was never discussed in the meeting. This situation is an instance of fabrication, where the model has *hallucinated* information that doesn't exist in the input data.

To mitigate the risk of fabrication, it's crucial to implement responsible AI practices. This includes rigorous testing of the prompt and the flow, providing the model with as much grounding information as possible and finally implementing a robust system for human oversight.

## Address risks through responsible AI practices

We advocate for responsible AI practices as a means to mitigate these risks. Despite having strategies in place to moderate the content produced by the model, managing the model's propensity to generate fabricated responses or succumb to prompt injection attacks remains a complex challenge. We acknowledge these risks and reaffirm our commitment to human oversight and control.

In recognition of the necessity for seamless automation, we're proactively enhancing our safety systems and seeking a deeper understanding of these challenges.
Our objective is to further refine the text generation model with appropriate safety measures, in line with our principles of [responsible AI by design](https://blogs.microsoft.com/on-the-issues/2023/02/02/responsible-ai-chatgpt-artificial-intelligence/), returning control to developers wherever feasible.

### See also

[Responsible AI - FAQ](faqs-text-generation.md)
