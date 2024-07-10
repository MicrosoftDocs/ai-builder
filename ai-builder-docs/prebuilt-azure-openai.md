---
title: Text generation model (preview) (deprecated)
description: The text generation prebuilt model in AI Builder is deprecated. It enables you to build AI-powered applications that use text generated from your input.
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

# Text generation model (preview) (deprecated)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature is deprecated and isn't be visible anymore.
> - The [new prompt builder feature](use-a-custom-prompt-in-flow.md) should be used instead.

### Prerequisites

- Your environment in the United States.
- The tenant must be allow-listed while this feature is in private preview.
- A Power Apps or Power Automate license.
- Dataverse database installed on the environment.
- An AI Builder add-on.

The text generation model's capability is a powerful tool in AI Builder. It enables you to quickly and easily build AI-powered applications that use text generated from your input, like these tools that:

- Quickly and accurately summarize long documents and extracts key information.
- Help draft responses to user queries.
- Classify text into different categories.
- Translate text from one language to another.

Text generation is powered by Azure OpenAI Service, which is built on Generative Pre-trained Transformer (GPT) technology. These large language models have been trained on a massive amount of text data. This enables them to generate text that's similar to human written text.

> [!IMPORTANT]
> - This is a preview feature.
> - Preview features aren’t meant for production use and might have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - [View our preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
> - This capability is only available in United States region.
> - This capability might be subject to usage limits or capacity throttling.

## Explore the model

The text generation model has a prompt engineering interface with sample prompts you can try. You can also create your own prompts to instruct the model.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).

1. On the left navigation panel, select **AI Builder** > **Explore** (Power Automate) or **AI models** > **Build an AI model** (Power Apps).

1. Select **Text** > **Text generation**.

    The following screenshot is from Power Automate.

    :::image type="content" alt-text="Screenshot of the text generation capability on the AI Builder Explore page." source="media/prebuilt-azure-openai/text-generation-works.png":::

The next window that opens is where you can create text that can be used for many tasks. [Learn how text generation works](azure-openai-textgen.md).

## Related information

- [How text generation works (preview)](azure-openai-textgen.md)
- [Use the text generation model in Power Apps (preview)](azure-openai-model-papp.md)
- [Use the text generation model in Power Automate (preview)](azure-openai-model-pauto.md)
- [FAQ for text generation](faqs-text-generation.md)
- [Human review for automation with Text generation model (preview)](azure-openai-human-review.md)
