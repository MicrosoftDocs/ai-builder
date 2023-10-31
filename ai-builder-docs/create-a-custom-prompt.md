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

AI Builder guides you through each step to create your custom prompt.

:::image type="content" source="media/create-a-custom-prompt/create-prompt.png" alt-text="Screenshot of the custom prompt page.":::

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - As we traverse this rapidly evolving field, we are dedicated to refining and improving our services based on user feedback and insights. We encourage developers to be cognizant of the risks and incorporate human review when utilizing this capability.

## Prerequisites

- Your environment is in the United States.
- You have a Power Apps or Power Automate license.
- A Microsoft Dataverse database is installed on the environment.
- You have an AI Builder add-on.

## Get started

AI Builder allows you to create a prompt using the date sources and inputs you want. You can also add the prompt to the Dataverse plug-in registry to use it across Power Platform.

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

When you're satisified, select **Save custom prompt**.

:::image type="content" source="media/create-a-custom-prompt/prompt-test.png" alt-text="Screenshot of a prompt response.":::

## Next step

- [Use a custom prompt in a flow](use-a-custom-prompt.md)
- Use your custom prompt in an app <!--add Philippe's content-->

### See also

[Human review for automation with the text generation model (preview)](azure-openai-human-review.md)
