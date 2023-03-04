---
title: Azure OpenAI Service model overview (preview)
description: Learn about text generation with the Azure OpenAI Service prebuilt AI Builder model.
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

# Azure OpenAI Service model overview (preview)

[!INCLUDE[cc-beta-prerelease-disclaimer](./includes/cc-beta-prerelease-disclaimer.md)]

The Azure OpenAI Service generative text capability is a powerful tool in AI Builder. It allows you to create custom AI capabilities quickly and easily for natural language processing (NLP). This preview capability enables you to build scenarios such as summarization, information extraction, autogenerate response, classification, translation, and more. It also allows you to use large language models to generate new text, which can be used for a variety of purposes.

> [!IMPORTANT]
>
> - This is a preview feature.
>
> - [!INCLUDE[cc_preview_features_definition](includes/cc-preview-features-definition.md)]
>
> - This capability is in process of rolling out, and may not be available in your region yet.
>
> - This capability  may be subject to usage limits or capacity throttling.

The text generation capability is powered by Azure OpenAI Service, which is built on Generative Pre-trained Transformer (GPT) technology. These large language models have been trained on a massive amount of text data, which enables them to generate text that's similar to human-written text. This text can be used for a variety of tasks.

## Text generation scenarios

You can take advantage of the current features and capabilities available to create powerful applications that can generate text from a given input. 

The following list provides some real-life scenarios of how your business can use text generation:

- Create a summarization tool that can quickly and accurately summarize long documents and extract key information that's relevant to your business.

- Create a response tool that can help draft responses to user queries.

- Create a classification tool that can help classify text into different categories.

- Create a translation tool that can accurately help translate text from one language to another. The possibilities are endless. 

## Explore the model

Find the Azure OpenAI Service model on the **Explore** page under the **Text** models. This will open a prompt engineering interface. The interface comes with sample prompts to help you try various instructions in this capability. You can also create your own prompts to instruct the model.

To open the model:

1. Sign in to [Power Apps](https://make.powerapps.com) or [Power Automate](https://make.powerautomate.com).

1. On the left navigation panel, select **AI Builder** > **Explore**.

1. On the panel to the right, select **Text** > **Azure OpenAI Service**.

    :::image type="content" alt-text="Screenshot of the Azure OpenAI Service model in the AI Builder Explore screen." source="media/prebuilt-azure-openai/openai-tile.png":::

The next window that opens is where you can create text that can be used for many tasks. To learn how to the Azure OpenAI Service generative text capability in this window, go to [How text generation in Azure OpenAI Service works](azure-openai-textgen.md).

## Application for preview of text generation capability within AI Builder

This new capability within AI Builder enables citizen developers to instruct the Azure OpenAI Service model to generate natural language text. 

This capability is in gated preview, and you'll need to apply for consideration to the trial. To be considered for early access to trial this capability, you can apply [here](https://forms.office.com/Pages/DesignPageV2.aspx?subpage=design&token=3241b6fa9d5a4b958858fea0318f7f87&id=v4j5cvGGr0GRqy180BHbR2LogRPRiTJDo1Rd8KnmcFRUMzlLTDZVQlJKSzNIWkVCMzE0VDFYVzk2QS4u).

### See also

- [How text generation in Azure OpenAI Service works (preview)](azure-openai-textgen.md)
- [Use your Azure OpenAI Service model in Power Apps (preview)](azure-openai-model-papp.md)
- [Use your Azure OpenAI Service model in Power Automate (preview)](azure-openai-model-pauto.md)
- [Training: Introduction to Azure OpenAI Service (module)](/training/modules/explore-azure-openai/)
