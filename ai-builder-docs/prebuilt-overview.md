---
title: Overview of prebuilt AI models - AI Builder
description: Learn about the prebuilt AI models that are available in AI Builder.
author: phil-cmd
ms.topic: overview
ms.date: 11/17/2026
ms.author: jangebhardt
ms.reviewer: angieandrews
---

# Overview of prebuilt AI models

AI Builder prebuilt models help you add intelligence to apps and flows without having to gather data and then build, train, and publish your own models. For example, in Power Apps, you can add a component based on a prebuilt model that recognizes contact information from business cards. You can use a prebuilt model in Power Automate to analyze whether customer feedback was positive or negative.

The following prebuilt models don't use generative AI or large language models (LLMs): business card reader, category classification, entity extraction, ID reader, invoice processing, key phrase extraction, language detection, receipt processing, sentiment analysis, text recognition, text translation, and the preview models contract processing and health insurance card processing. All of these models use Microsoft-managed machine learning models that extract, classify, or translate the content you provide and return a defined set of results. You don't give them instructions in a prompt.

Other prebuilt models:

- **Text generation (preview) (deprecated)**: A generative AI model that uses Azure OpenAI models and responds to prompts.
- **Image description (preview)**: Creates a short description of an image by using a Microsoft-managed machine learning model. You provide an image, not a prompt.

Use prebuilt models in common business scenarios. To help you decide which model to use, determine if you need a model to pull data from documents, evaluate text, or analyze images. The following prebuilt models are currently available in AI Builder.

| Model | Category |
| ----- | -------- |
| [Contract processing (preview)](prebuilt-contract-processing.md) | Documents |
| [Health insurance card processing (preview)](prebuilt-health-insurance-card.md) | Documents |
| [Invoice processing](prebuilt-invoice-processing.md) | Documents |
| [Text recognition](prebuilt-text-recognition.md) | Documents, Images |
| [Sentiment analysis](prebuilt-sentiment-analysis.md) | Text |
| [Receipt processing](prebuilt-receipt-processing.md) | Documents |
| [Entity extraction](prebuilt-entity-extraction.md) | Text |
| [ID reader](prebuilt-id-reader.md) | Documents |
| [Key phrase extraction](prebuilt-key-phrase.md) | Text |
| [Business card reader](prebuilt-business-card.md) | Documents |
| [Category classification (preview)](prebuilt-category-classification.md) | Text |
| [Language detection](prebuilt-language-detection.md) | Text |
| [Text translation](prebuilt-text-translation.md) | Text |
| [Image description (preview)](prebuilt-image-description.md) | Images |

Prebuilt models are available in Power Automate and Power Apps. Learn more in [Use AI Builder models in Power Apps](/ai-builder/powerfx-in-powerapps).

## Model usage limitations

AI Builder prebuilt models don't use models from DeepSeek, Black Forest Labs (FLUX), Moonshot AI, Mistral AI, xAI, or Meta (Llama). This limitation applies in all regions, including Australia.

If an admin turns on supported external models, prompts can use them. Prompts are a separate AI Builder feature that uses generative AI.

> [!NOTE]
> The legacy model [Text generation (preview)](prebuilt-azure-openai.md) is now deprecated and isn't visible. Use the [new prompt builder feature](use-a-custom-prompt-in-flow.md) instead.

## Download the AI Builder prebuilt model combined with Power Fx cheat sheet

Download the AI Builder prebuilt model combined with Power Fx cheat sheet for quick reference. This guide is perfect for those beginning to explore AI Builder’s prebuilt models in Power Apps, offering insights into using Power Fx formulas effectively. It simplifies key concepts to enhance decision-making and ease of use.

Download the guide: [AI Builder prebuilt model combined with Power Fx cheat sheet](https://go.microsoft.com/fwlink/?linkid=2300739)

## Related information

- [AI Builder in Power Automate overview](use-in-flow-overview.md)  
- [AI Builder in Power Apps overview](use-in-powerapps-overview.md)
- [Feature availability by region](availability-region.md)

