---
title: Create a custom prompt (preview)
description: Learn how to create a custom prompt.
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

# Create a custom prompt (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The Power Platform AI prompt builder empowers makers to create custom prompts tailored to unique business requirements, utilizing natural language prompts. Examples of some prompts are summarizing, classifying, extracting entities, translating, assessing sentiment, crafting a response to a complaint, and much more.

The AI prompt builder leverages Power Platform objects like flows and apps to define a specific behavior. These objects can be added to a copilot and help you to gain efficiency in your daily business routine.

:::image type="content" source="media/create-a-custom-prompt/create-prompt.png" alt-text="Screenshot of the custom prompt page.":::

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - As we traverse this rapidly evolving field, we are dedicated to refining and improving our services based on user feedback and insights. We encourage developers to be cognizant of the risks and incorporate human review when utilizing this capability.

## Types of AI prompts

 The two types of prompts, *custom* and *prebuilt*, are described in this section, and an example of each type is provided.

### Custom prompt

Custom prompts allow makers to customize the behavior of the AI model and make it useful for a wide variety of applications. By crafting a prompt, you can obtain responses that align with your specific requirements, making the AI model a versatile tool for a wide range of tasks.

**Example**

When using a language model, you can provide a custom prompt to instruct the model on how to answer a question, complete a text, translate a language, summarize a document, or identify tasks, to-dos, or action items from text.

The custom prompt can be as simple as a single sentence or more complex, depending on the task you want to accomplish.

### Prebuilt prompt

A prebuilt prompt is a predefined prompt that's created and optimized by Power Platform to help makers easily accomplish common tasks. Prebuilt prompts are designed to simplify interactions by offering templates to see how to use generative AI for a various use cases.

**Example**

A prebuilt prompt for a language model could be something like:

`Extract as a numbered list the action points from the: [TextToExtract]`

In this case, the user only needs to provide the text in `[TextToExtract]` that they want to extract action points, and the prebuilt prompt handles the rest.

## Prerequisites

- Have a basic understanding of how to write prompts 
- Your environment is in the United States.
- You have a Power Apps or Power Automate license.
- A Microsoft Dataverse database is installed on the environment.
- You have an AI Builder add-on.

## Get started

AI Builder allows you this flexibility to create your own custom prompt by defining input variables you want. It gives you the ability to validate steps with **Test your prompt**, ensuring optimal prompt performance and rightness before integration into solutions.

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
1. Test your prompt using the sample value.
1. Save your custom prompt by selecting **Save custom prompt**.

### Review your prompt

After you test your prompt with the sample value (in step 4), review it see how well your prompt works.

When you're satisfied, select **Save custom prompt**.

:::image type="content" source="media/create-a-custom-prompt/prompt-test.png" alt-text="Screenshot of a prompt response.":::

## Next step

- Use in a Power Automate flow
    - Grants the ability to incorporate an existing prompt as a flow action.
    - [Use a custom prompt in a Power Automate flow](use-a-custom-prompt-in-flow.md)

- Use in Power Apps
    - Empowers makers to incorporate existing prompts into their apps.
    - [Use a custom prompt in Power Apps](use-a-custom-prompt-in-app.md)

### See also

[Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
