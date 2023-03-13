---
title: How text generation in Azure OpenAI Service works (preview)
description: Learn what makes text generation with GPT possible, like prompt engineering, human inspection and oversight, and responsible AI in AI Builder.
author: ashbhati
contributors:
  - ashbhati
  - v-aangie
ms.topic: conceptual
ms.custom: 
ms.date: 03/06/2023
ms.author: ashbhati
ms.reviewer: angieandrews
---

# How text generation in Azure OpenAI Service works (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

This topic explains *prompt engineering* and other key concepts to help you create powerful applications that can generate text from your input.

> [!IMPORTANT]
>
> - This is a preview feature.
>
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - For more information, go to our [preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
>- This capability is in process of rolling out, and may not be available in your region yet.
>
> - This capability  may be subject to usage limits or capacity throttling.

## Prompt engineering

Select the **Azure OpenAI Service** tile to open a *prompt engineering* interface for the maker. This exploratory experience can be used to interact with the model and understand how to instruct the model to generate a desired text. The prompt engineering interface comes with sample prompts to help you try out this capability.

*Prompt* is a natural language instruction for the machine learning model to perform a task. The GPT model uses the prompt to determine the structure and content of the text it needs to generate. *Prompt engineering* is a process used to create and refine the input that's used to generate text with the Azure OpenAI Service generative text capability.

### Use specific text

 The goal of prompt engineering is to create an input that's as specific as possible in order to get a more relevant response from the AI model. For example, if you want to generate text about a specific topic, you should create a prompt that's specific to that topic and conveys the intent to the model.

The prompt could include any of the following:

- The topic itself.

- Relevant keywords or phrases associated with the topic.

- The tone of the writing.

- The target audience.

By providing a more specific prompt, you can ensure that the generated text is more relevant to the topic.

### Refine your text

Prompt engineering can also be used to refine the generated text. For example, if the generated text is too long or contains irrelevant information, you can adjust the prompt to focus on specific aspects of the topic. This can help to ensure that the generated text is more relevant and useful. Citizen developers can take advantage of prompt engineering to get the most out of the text generation model. This can help to create powerful applications that can generate text from a given input. 

A good prompt should have the following characteristics: 

- **Clear and concise language:** Be written in clear and concise language that is easy to understand.

- **Specificity:** Be specific enough to guide the GPT model in the right direction.

- **Context:** Provide enough context for the GPT model to generate meaningful output.

- **Relevance:** Be relevant to the task at hand and  provide the GPT model with enough information to generate meaningful output.

### Parts of a prompt

There are generally two parts of any prompt:

- **Instruction:** The instruction is the first part of a prompt for a GPT model. This part should provide clear instructions on what the model should do. For example, "*Summarize this email into 3 bullets.*"

- **Context:** The context is the second part of a prompt. This part should provide the model with relevant information to help it generate an appropriate response. For example, "*The email contains customer feedback from the past week.*"

Usually in an automation task, the first part of the prompt (the instruction) remains constant. The second part of the prompt (the context) gets replaced by a dynamic content, such that you can reuse the instruction in an automation workflow. For example, we're building automation to summarize weekly customer feedback and to generate a positive toned response. We would build an automation to filter out the weekly emails containing customer feedback and give a prompt to the GPT model with instruction part as follows:

“*Summarize the following customer feedback into bullet points, identify each distinct topic. Additionally, generate a positive tone response, indicating that we will take action on key points they have highlighted.*"

:::image type="content" alt-text="Screenshot of the Azure OpenAI Service model in the AI Builder Explore screen." source="media/azure-openai-textgen/instruction.png":::

 The context would be the entire body of text from the weekly feedback email. The feedback keeps changing weekly based on the previous week’s experience, whereas the instruction part of the prompt remains the same.

## Human oversight

Human oversight is an important step when working with AI generated content from GPT models. The GPT model is a natural language processing (NLP) model that can generate human-like text from a prompt. It's currently in preview and is likely to make mistakes or have biases and other undesirable content.

To ensure that the AI generated content you use is accurate, appropriate and free from bias, it's important to have humans review the content before posting it online, sending it to a customer, or using it to help inform a business decision. The onus on validating the content generated by the GPT model is on the citizen developer. 

Human review is a critical step to ensuring proper oversight. Human oversight can help to identify any potential errors or biases in the content generated by the GPT model, and ensures people have a role in decision-making and can intervene in real time to prevent harm. It can also help to ensure that the content is relevant to the intended use case and is in line with the company’s values and objectives.

Human oversight can also help to identify any potential issues with the GPT model itself. For example, if the model is generating content that is not relevant to the intended use case, then it may be necessary to adjust the prompt of the model by giving more precise instructions like scope, tone, length, and more.

 Human oversight is an important step in ensuring that the content generated by the GPT model is as intended and aligned with goals and objectives of desired solution.

## Responsible AI  

We're committed to creating [responsible AI](https://blogs.microsoft.com/on-the-issues/2023/02/02/responsible-ai-chatgpt-artificial-intelligence/) by design. Microsoft has developed a set of responsible AI principles to ensure that its products are developed and used responsibly. Our work is guided by a core set of principles: fairness, reliability and safety, privacy and security, inclusiveness, transparency, and accountability. We're putting these principles into practice across the company to develop and deploy AI that will have a positive impact on society. We strive to deploy AI that benefits society and take a comprehensive approach, combining innovative research, exceptional engineering, and responsible governance. Alongside OpenAI’s leading research on AI alignment, we're advancing a framework for the safe deployment of our own AI technologies that's aimed to help guide the industry toward more responsible outcomes.

To learn more about responsible AI, go to [Use cases for Azure OpenAI Service](/legal/cognitive-services/openai/transparency-note?context=%2Fazure%2Fcognitive-services%2Fopenai%2Fcontext%2Fcontext).


### See also

- [Azure OpenAI Service model overview (preview)](prebuilt-azure-openai.md)
- [Use your Azure OpenAI Service model in Power Apps (preview)](azure-openai-model-papp.md)
- [Use your Azure OpenAI Service model in Power Automate (preview)](azure-openai-model-pauto.md)
