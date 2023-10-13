---
title: How text generation works (preview)
description: Learn what makes text generation with GPT possible, like prompt engineering, human inspection and oversight, and responsible AI in AI Builder.
author: ashbhati
contributors:
  - ashbhati
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.custom: bap-template
ms.date: 07/13/2023
ms.author: ashbhati
ms.reviewer: angieandrews
---

# How text generation works (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

This article explains *prompt engineering* and other key concepts to help you create powerful applications that can generate text from your input. *Prompt* is a natural language instruction that tells the machine learning model to perform a task. The GPT model uses the prompt to determine the structure and content of the text it needs to generate. *Prompt engineering* is the process of creating and refining the input that's used to generate text with the GPT text generation capability.

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - [View our preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
> - This capability is available only in the United States region.
> - This capability  may be subject to usage limits or capacity throttling.

## Open the prompt engineering interface

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).

1. On the left navigation panel, select **AI Builder** > **Explore** (Power Automate) or **AI models** > **Build an AI model** (Power Apps).

1. Select **Text** > **Text generation**.

    The following screenshot is from Power Automate.

    :::image type="content" alt-text="Screenshot of the Azure OpenAI Service model on the AI Builder Explore page in Power Automate." source="media/prebuilt-azure-openai/text-generation-works.png":::

    The prompt engineering window opens. Use this exploratory experience to learn how to instruct the model to generate desired text. The prompt engineering interface comes with sample prompts to help you try out the capability.

## Use specific text for more relevant responses

 The goal of prompt engineering is to create an input that's as specific as possible to get a more relevant response from the AI model. Your prompts should be specific to a topic and convey your intent.

A prompt might include the following information:

- The topic
- Keywords or phrases that are associated with the topic
- The tone of the response
- The target audience

For example:

`Generate a response to the text below. Be apologetic, humble, and creative with the response. The response should restate the problem to acknowledge the issue. The response should indicate that the problem will be addressed shortly.`

:::image type="content" source="media\azure-openai-model-papp\azure-openai-model-prompt-window.png" alt-text="Screenshot of the OpenAI prompt engineering window in Power Apps, with a sample prompt and response.":::

If the generated text is too long or contains irrelevant information, adjust the prompt. A good prompt has the following characteristics:

- **Clear and concise:** It's written in clear and concise language that's easy to understand.

- **Specific:** It's specific enough to guide the GPT model in the right direction.

- **Contextual:** It provides enough context for the GPT model to generate meaningful output.

- **Relevant:** It's relevant to the task and provides the GPT model with enough information to generate meaningful output.

### Parts of a prompt

There are generally two parts to a prompt for a GPT model, the *instruction* and the *context*.

- **The instruction** is the first part of the prompt. It should provide clear directions on what the model should do; for example, "Summarize this email in three bullets."

- **The context** is the second part of the prompt. It should provide the information the model needs to generate an appropriate response; for example, "The email contains customer feedback from the past week."

Usually in an automation task, the instruction remains constant. The context gets replaced by dynamic content so that the instruction can be reused in an automated workflow.

For example, you're building a workflow to summarize customer feedback every week and generate a response. You might build an automation to filter email that contains customer feedback and include a prompt like this:

"Summarize the following customer feedback into bullet points, identify each distinct topic. Additionally, generate a positive tone response, indicating that we'll take action on key points they have highlighted."

:::image type="content" alt-text="Screenshot of the OpenAI prompt engineering window in Power Apps, with a sample customer feedback prompt and response." source="media/azure-openai-textgen/instruction.png":::

 The context is the entire body of text from the weekly feedback emails. The feedback changes weekly, but the instruction part of the prompt remains the same.

## Human oversight

Human oversight is an important step when working with content that's generated from a GPT model. Large language models like GPT are trained on huge amounts of data. AI-generated content can contain errors and biases. A human should review it before it's posted online, sent to a customer, or used to inform a business decision. Human oversight helps not only to identify potential errors and biases, but also to make sure the content is relevant to the intended use case and aligns with the company's values.

Human review can also help to identify any issues with the GPT model itself. For example, if the model is generating content that isn't relevant to the intended use case, then you may need to adjust the prompt.

## Responsible AI  

We're committed to creating [responsible AI](https://blogs.microsoft.com/on-the-issues/2023/02/02/responsible-ai-chatgpt-artificial-intelligence/) by design. Our work is guided by a [core set of principles](https://www.microsoft.com/ai/responsible-ai): fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability. We're putting these principles into practice across the company to develop and deploy AI that has a positive impact on society. We take a comprehensive approach, combining innovative research, exceptional engineering, and responsible governance. Alongside OpenAI's leading research on AI alignment, we're advancing a framework for the safe deployment of our own AI technologies that's aimed to help guide the industry toward more responsible outcomes.

[Learn more about transparency in the Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?context=%2Fazure%2Fcognitive-services%2Fopenai%2Fcontext%2Fcontext).

### See also

- [Text generation overview (preview)](prebuilt-azure-openai.md)  
- [Use the text generation model in Power Apps (preview)](azure-openai-model-papp.md)  
- [Use the text generation model in Power Automate (preview)](azure-openai-model-pauto.md)  
- [Responsible AI - FAQ for text generation](faqs-text-generation.md)
- [Human review for automation with text generation model (preview)](azure-openai-human-review.md)
