---
title: Create a prompt
description: Learn how to create a custom prompt.
author: ashbhati
contributors:
  - ashbhati
  - phil-cmd
  - CedrickBellarosa
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 03/28/2025
ms.author: ashbhati
ms.reviewer: angieandrews
ms.custom:
  - DevRelAdv
---

# Create a prompt

Custom prompts give makers the freedom to instruct the generative AI model to behave in a certain way or to perform a specific task. By carefully crafting a prompt, you can generate responses that suit your specific business needs. This transforms the model into a flexible tool to accomplish various tasks.

> [!IMPORTANT]
> - AI Builder prompts run on GPT models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Supported languages

The following list of supported languages for prompts in AI Builder is subject to be updated:

Chinese (Simplified), Czech (Czech Republic), Danish (Denmark), Dutch (Netherlands), English (United States), Finnish (Finland), French (France), German (Germany), Greek (Greece), Italian (Italy), Japanese (Japan), Korean (Korea), Polish (Poland), Portuguese (Brazil), Russian (Russia), Spanish (Spain), Swedish (Sweden), Thai (Thailand), Turkish (Türkiye)

## Use specific text for more relevant responses

The goal of prompt engineering is to create an instruction that's as specific as possible to get a more relevant response from the  model. Your prompts should be specific to a topic and convey your intent.

A prompt might include the following  information:

- The topic
- Keywords or phrases that are associated with the topic
- The tone of the response
- The target audience

If the generated text is too long or contains irrelevant information, adjust the prompt. A good prompt has the following characteristics:

- **Clear and concise**: It's written in clear and concise language that's easy to understand.
- **Specific**: It's specific enough to guide the GPT model in the right direction.
- **Contextual**: It provides enough context for the GPT model to generate meaningful output.
- **Relevant**: It's relevant to the task and provides the GPT model with enough information to generate meaningful output.

## Parts of a prompt

There are generally two parts to a prompt: the instruction and the context.

- The instruction is the first part of the prompt. It should provide clear directions on what the GPT model should do, for example, "Summarize this email in three bullets."
- The context is the second part of the prompt. It should provide the information the model needs to generate an appropriate response, for example, "The email contains customer feedback from the past week."

**Example**

A custom prompt can guide the model to answer a question, complete text, translate languages, summarize a document, and identify tasks, to-dos, and action items in text. The complexity of a custom prompt can range from a single sentence to something more intricate, depending on the task.

## Download: AI Builder prompt engineering guide

**Download the guide here: [AI Builder prompt engineering guide (10 pages, 10X13 in.)](https://go.microsoft.com/fwlink/?linkid=2255775)** 

:::image type="content" source="media/create-a-custom-prompt/prompt-engineering-guide.png" alt-text="Screenshot of AI Builder prompt engineering guide.":::

Download and print the AI Builder prompt engineering guide (10 pages, 10X13 inch size) to keep it handy and get help creating prompts.

## Create a prompt

Prompt builder provides the flexibility to create your own custom prompt by defining input variables that enable incorporating dynamic runtime content within a prompt. It gives you the ability to validate the prompt, ensuring optimal prompt performance and correctness of the response before integration into your business solutions.

1. Sign in to [Power Apps](https://make.powerapps.com), [Power Automate](https://make.powerautomate.com), or [Copilot Studio](https://copilotstudio.microsoft.com).
1. For Power Apps and Power Automate, select **AI hub** > **Prompts** > **Build your own prompt**.
1. For Copilot Studio, there are multiple ways to create a prompt
    1. Select **Agents**, pick or create an agent, then select **Actions** > **Add an action** > **New action** > **New prompt**
    2. Select **Agents**, pick or create an agent, then select **Topics**. Pick or create a topic, add a node, then select **Add an action** > **New prompt**
    3. Select **Library** > **Add new** > **Prompt**. Prompts created in the library can then be used in any agent action or topic.

    :::image type="content" source="media/create-a-custom-prompt/custom-prompt.png" alt-text="Screenshot of the fields you fill in to create a custom prompt.":::

### Configure and test your prompt

1. Enter a custom name for your prompt by clicking on the generated name at the top left of the prompt.
   
1. Write your prompt or select a prompt template.

    > [!TIP]
    > To access a larger set of prompt templates, go to the Prompt directory [Sample Solution Gallery](https://aka.ms/power-prompts).

1. Include an input object by typing **/** or selecting **Add content**, then select **Input**. Input objects allow you to pass dynamic values to the prompt at runtime.

   :::image type="content" source="media/create-a-custom-prompt/custom-prompt-add-input.png" alt-text="Add input.":::

   In this view, you can also select a knowledge object in the **Knowledge** section. A knowledge object represents a set of data that is retrieved through a data source connection, like Dataverse. This allows your prompt to generate answers that are related to your business data.
  
1. Enter a sample value for each of your inputs.

   :::image type="content" source="media/create-a-custom-prompt/custom-prompt-input-sample.png" alt-text="Add input.":::
  
1. Select **Test** to run your prompt and review its response.
   
1. When you're satisfied, select **Save**.


## Use your prompt in Power Apps or Power Automate

Your next step is determined by the app you plan to use with your prompt.

- Use in Power Apps
  - Empowers makers to incorporate existing prompts into their apps.
  - [Use a prompt in Power Apps](use-a-custom-prompt-in-app.md)

- Use in Power Automate
  - Empowers makers to incorporate existing prompts into their flows.
  - [Use a prompt in Power Automate](use-a-custom-prompt-in-flow.md)

Learn how to include your prompt in a flow in this quick video:</br>
</br>
  
> [!VIDEO 0b76ebb0-c95c-483b-b29b-7d5c0921f3a9]

## Related information

[Human review for automation with a prompt](azure-openai-human-review.md)
