---
title: Create a custom prompt (preview)
description: Learn how to create a custom prompt with prompt builder.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 11/15/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Create a custom prompt (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]


> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - View our [preview terms](https://powerplatform.microsoft.com/en-us/legaldocs/supp-powerplatform-preview/).
> - This capability is only available in United States region.
> - This capability might be subject to usage limits or capacity throttling.

### Custom prompts

Custom prompts give makers the freedom to instruct the LLM model to behave in a certain way or to perform a specific task. By carefully crafting a prompt, you can generate responses that suit your specific business needs. This transforms the LLM model into a flexible tool to accomplish various tasks.

**Use specific text for more relevant responses**

The goal of prompt engineering is to create an instruction  that's as specific as possible to get a more relevant response from the AI model. Your prompts should be specific to a topic and convey your intent.

A prompt might include the following  information:

- The topic
- Keywords or phrases that are associated with the topic
- The tone of the response
- The target audience

If the generated text is too long or contains irrelevant information, adjust the prompt. A good prompt has the following characteristics:

- Clear and concise: It's written in clear and concise language that's easy to understand.
- Specific: It's specific enough to guide the GPT model in the right direction.
- Contextual: It provides enough context for the GPT model to generate meaningful output.
- Relevant: It's relevant to the task and provides the GPT model with enough information to generate meaningful output.

**Parts of a prompt**

There are generally two parts to a prompt for a GPT model, the instruction and the context.

- The instruction is the first part of the prompt. It should provide clear directions on what the model should do; for example, "Summarize this email in three bullets."
- The context is the second part of the prompt. It should provide the information the model needs to generate an appropriate response; for example, "The email contains customer feedback from the past week."


**Example**

With a language model, a custom prompt can guide the model to answer a question, complete text, translate languages, summarize a document, and identify tasks, to-dos, and action items in text. The complexity of a custom prompt can range from a single sentence to something more intricate, depending on the task.


## Get started

Prompt builder provides the flexibility to create your own custom prompt by defining input variables that enable incorporating dynamic runtime content within a prompt. It gives you the ability to validate the prompt with **Test your prompt**, ensuring optimal prompt performance and correctness of the response before integration into your business solutions.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://flow.microsoft.com).
1. On the left pane, select **Prompts** > **Create text, summarize documents, and more with GPT**.
1. On the lower-right corner, select **Create custom prompt**.

    :::image type="content" source="media/create-a-custom-prompt/custom-prompt-button.png" alt-text="Screenshot of the 'Create custom prompt' button."::: 

### Configure and test your prompt

Use the following screenshot as a guide to build and test your prompt.

:::image type="content" source="media/create-a-custom-prompt/configure-test.png" alt-text="Screenshot of the steps to configure and test your prompt."::: 

1. Enter a name for your prompt.
1. Write or paste your prompt or you can build upon an existing template, to give yourself a starting point.
1. Add a dynamic value, and then select **Enter**.

    In the process of building prompts, makers often need to provide context data to ensure that the model generates appropriate responses. To facilitate this, dynamic values are used in the prompt, serving as placeholders that get filled with actual data at runtime.
  
1. Test your prompt using the sample value.

    The testing of prompts is an essential yet often under-emphasized capability. Manual testing is beneficial for iterative building experiences.

1. Save your custom prompt by selecting **Save custom prompt**.

### Review and save your prompt

Prompt builder allows makers to save prompts to facilitate reusability, archiving, and future improvement of prompts.

After you test your prompt with the sample value (in step 4), review it to see how well your prompt works.

When you're satisfied, select **Save custom prompt**.

:::image type="content" source="media/create-a-custom-prompt/prompt-test.png" alt-text="Screenshot of a prompt response.":::

## Next step

- Use in Power Apps
    - Empowers makers to incorporate existing prompts into their apps.
    - [Use a custom prompt in Power Apps](use-a-custom-prompt-in-app.md)

- Use in Power Automate
  - Empowers makers to incorporate existing prompts into their flows.
  - [Use a custom prompt in Power Flows](use-a-custom-prompt-in-flow.md)

### See also

[Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
