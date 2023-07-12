---
title: Azure OpenAI Service model overview (preview)
description: Learn how to use text generation with GPT-3 and the Azure OpenAI Service prebuilt model in AI Builder to build a ChatGPT-like experience in Power Platform.
author: ashbhati
contributors:
  - ashbhati
  - v-aangie
ms.topic: conceptual
ms.custom: bap-template
ms.date: 03/06/2023
ms.author: ashbhati
ms.reviewer: angieandrews
---

# Azure OpenAI Service model overview (preview)

[!INCLUDE [cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The Azure OpenAI Service generative text capability is a powerful tool in AI Builder. This preview capability enables you to quickly and easily build AI-powered applications that use text generated from your input, like these:

- A tool that quickly and accurately summarizes long documents and extracts key information.
- A tool that helps draft responses to user queries.
- A tool that classifies text into different categories.
- A tool that translates text from one language to another.

Text generation is powered by Azure OpenAI Service, which is built on Generative Pre-trained Transformer (GPT) technology. These large language models have been trained on a massive amount of text data, which enables them to generate text that's similar to human-written text.

> [!IMPORTANT]
>
> - This is a preview feature.
>
> - [!INCLUDE [cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - [View our preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).
>
> - This capability might not be available in your region yet.
>
> - This capability may be subject to usage limits or capacity throttling.

## Explore the model

The Azure OpenAI Service model has a prompt engineering interface with sample prompts you can try. You can also create your own prompts to instruct the model.

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).

1. On the left navigation panel, select **AI Builder** > **Explore** (Power Automate) or **AI models** > **Build an AI model** (Power Apps).

1. Select **Text** > **Azure OpenAI Service** (Power Automate) or **Text** > **Text generation** (Power Apps).

    :::image type="content" alt-text="Screenshot of GPT Text gneration capability on the AI Builder Explore page." source="media/prebuilt-azure-openai/text-generation-works.png":::

The next window that opens is where you can create text that can be used for many tasks. [Learn how GPT text generation works](azure-openai-textgen.md).

### See also

- [How GPT text generation works (preview)](azure-openai-textgen.md)
- [Use GPT text generation model in Power Apps (preview)](azure-openai-model-papp.md)
- [Use your GPT text generation model in Power Automate (preview)](azure-openai-model-pauto.md)
