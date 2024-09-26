---
title: Add inputs to a prompt
description: Learn how to add text, image or document input to a prompt.
author: antrod
contributors:
  - antrod
  - v-aangie
ms.topic: conceptual
ms.collection: 
- get-started
- bap-ai-copilot
ms.date: 0926/2024
ms.author: antrod
ms.reviewer: angieandrews
---

# Add text, image or document input to a prompt
Within your prompt, you have the ability to include inputs that will allow users to pass text but also image or document (preview) to the prompt at run time.


> [!IMPORTANT]
> - AI Builder prompts run on GPT 3.5 and GPT 4 models powered by [Azure OpenAI Service](/azure/ai-services/openai/whats-new).
> - This capability is [limited to some regions](availability-region.md#prompts).
> - This capability might be subject to usage limits or capacity throttling.

## Adding an input to a prompt
In the prompt builder experience, you have 2 options to include an input:

- Use the forward slash **/** within your prompt instruction, and select **Text**. Give your input a name and provide a sample data now or later.
:::image type="content" source="media/add-inputs-prompt/add-input-slash.png" alt-text="Add an input using /":::

- Click on the input icon on the top right of the prompt builder experience, then **+ Add input** > **Text**. Give your input a name and provide a sample data now or later.
:::image type="content" source="media/add-inputs-prompt/add-input-menu.png" alt-text="Add an input using /":::
When using this second option, you need to include the input inside the prompt instruction using the "+ Insert" option at the top of the prompt builder experience.


## Text input

## Image or document input (preview)
[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]


[!INCLUDE [cc_preview_features_definition](./includes/cc-preview-features-definition.md)]


## Use your prompt in Power Apps or Power Automate

Your next step is determined by the app you plan to use with your prompt.

- Use in Power Apps
  - Empowers makers to incorporate existing prompts into their apps.
  - [Use a prompt in Power Apps](use-a-custom-prompt-in-app.md)

- Use in Power Automate
  - Empowers makers to incorporate existing prompts into their flows.
  - [Use a prompt in Power Automate](use-a-custom-prompt-in-flow.md)

## Related information

- [Human review for automation with a prompt](azure-openai-human-review.md)
- [FAQ for prompts and text generation capabilities](faqs-text-generation.md)
