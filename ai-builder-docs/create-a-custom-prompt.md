---
title: Create a custom prompt with Prompt Builder (preview)
description: Learn how to create a custom prompt with Prompt Builder.
author: phil-cmd
contributors:
  - phil-cmd
  - v-aangie
ms.topic: conceptual
ms.collection: get-started
ms.date: 11/14/2023
ms.author: plarrue
ms.reviewer: angieandrews
---

# Create a custom prompt with Prompt Builder (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

Prompt Builder is a prompt engineering tool from AI Builder. This tool lets makers write and test prompts for the text generation model.

## What a prompt is and how to use it

Think of a prompt as a task or a goal you give to the large language model (LLM). With Prompt Builder, you can make, test, and save your custom prompts. You can also use input variables to provide dynamic context data at runtime. You can share these prompts with others and use them in Power Automate, Power Apps, or Copilot Studio. For instance, you could make a prompt to pick out action items from your company emails and use it in a Power Automate flow to build an email processing automation.

Prompt Builder enables makers to devise custom prompts that cater to their specific business needs using natural language. These prompts can be employed for a variety of tasks or business scenarios, such as summarizing content, categorizing data, extracting entities, translating languages, assessing sentiment, or formulating a response to a complaint.

Prompts can be integrated into flows to build intelligent hands-off automation. Makers can also build advanced generative AI capabilities for their applications by describing them as natural language prompts. These prompts can be used to extend a custom copilot, thereby streamlining your daily business operations and boosting efficiency."

:::image type="content" source="media/create-a-custom-prompt/create-prompt.png" alt-text="Screenshot of the custom prompt page.":::

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - View our [preview terms](https://powerplatform.microsoft.com/en-us/legaldocs/supp-powerplatform-preview/).
> - This capability is only available in United States region.
> - This capability might be subject to usage limits or capacity throttling.

## Understand AI prompts

This section describes the two types of prompts: custom and prebuilt.

### Custom prompts

Custom prompts give makers the freedom to instruct the LLM model to behave in a certain way or to perform a specific task. By carefully crafting a prompt, you can generate responses that suit your specific business needs. This transforms the LLM model into a flexible tool to accomplish various tasks.

**Example**

With a language model, a custom prompt can guide the model to answer a question, complete text, translate languages, summarize a document, and identify tasks, to-dos, and action items in text. The complexity of a custom prompt can range from a single sentence to something more intricate, depending on the task.

### Prebuilt prompts

Prebuilt prompts are pre-configured prompts created and fine-tuned by the Microsoft team to assist makers in accomplishing common tasks easily. They offer templates to demonstrate how to use generative AI across various use cases, which simplifies interactions.

**Example**

A language model's prebuilt prompt could look like this:

`Extract as a numbered list the action points from the: [TextToExtract]`

In this case, the user only needs to supply the text in `[TextToExtract]` from which they want to extract action points. The prebuilt prompt takes care of the rest.

## Prerequisites

- Have a basic understanding of how to write prompts.
- Your environment is in the United States.
- You have a Power Apps or Power Automate license.
- A Microsoft Dataverse database is installed on the environment.
- You have an AI Builder add-on.

## Get started

Prompt Builder provides the flexibility to create your own custom prompt by defining input variables that enable incorporating dynamic runtime content within a prompt. It gives you the ability to validate the prompt with **Test your prompt**, ensuring optimal prompt performance and correctness of the response before integration into your business solutions.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://flow.microsoft.com).
1. On the left pane, select **Prompts** > **Create text, summarize documents, and more with GPT**.
1. On the lower-right corner, select **Create custom prompt**.

    :::image type="content" source="media/create-a-custom-prompt/custom-prompt-button.png" alt-text="Screenshot of the 'Create custom prompt' button."::: 

### Configure and test your prompt

Use the following screenshot to guide you through configuring and testing your prompt.

:::image type="content" source="media/create-a-custom-prompt/configure-test.png" alt-text="Screenshot of the steps to configure and test your prompt."::: 

1. Enter a name for your prompt.
1. Write or paste your prompt.
1. Add a dynamic value, and then select **Enter**.

    In the process of building prompts, makers often need to provide context data to ensure that the model generates appropriate responses. To facilitate this, dynamic values are used in the prompt, serving as placeholders that get filled with actual data at runtime.
  
1. Test your prompt using the sample value.

    The testing of prompts is an essential yet often under-emphasized capability. Manual testing is beneficial for iterative building experiences.

1. Save your custom prompt by selecting **Save custom prompt**.

### Review and save your prompt

Prompt Builder allows makers to save prompts to facilitate reusability, archiving, and future improvement of prompts.

After you test your prompt with the sample value (in step 4), review it to see how well your prompt works.

When you're satisfied, select **Save custom prompt**.

:::image type="content" source="media/create-a-custom-prompt/prompt-test.png" alt-text="Screenshot of a prompt response.":::

## Next step

<!--use this only if it's ready for Ignite - Use in a Power Automate flow
    - Grants the ability to incorporate an existing prompt as a flow action.
    - [Use a custom prompt in a Power Automate flow](use-a-custom-prompt-in-flow.md) -->

- Use in Power Apps
    - Empowers makers to incorporate existing prompts into their apps.
    - [Use a custom prompt in Power Apps](use-a-custom-prompt-in-app.md)

### See also

[Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
