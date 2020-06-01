---
title: Key phrase extraction prebuilt AI model - AI Builder | Microsoft Docs
description: Describes the prebuilt key phrase extraction AI model in AI Builder.
author: alanabrito
ms.service: powerapps
ms.topic: conceptual
ms.custom: 
ms.date: 05/11/2020
ms.author: alanab
ms.reviewer: v-dehaas
---

# Key phrase extraction model

The key phrase extraction prebuilt model identifies the main points in a text document. For example, given input text "The food was delicious and there were wonderful staff",<!--Can this be rewritten as "the staff was wonderful", or if that would foil the model, "there were wonderful servers"? US English doesn't treat "staff" as plural.--> the model returns the main talking points: "food"<!--Not "delicious food," I see.--> and "wonderful staff". This model can extract a list of key phrases from unstructured text documents.

## Use in Power Apps

### Explore key phrase extraction

You can try out the key phrase extraction model before you import it into your flow by using the "try it out" feature.

1. Sign in to [Power Apps](https://make.powerapps.com).
1. In the left pane, select **AI Builder** > **Build**.
1. Under **Get straight to productivity**, select **Key Phrase Extraction**.
1. In the **Key Phrase Extraction** window, select **Try it out**. 
1. Select predefined text samples to analyze, or add your own text in the **Add your own here** box to see how the model analyzes your text.

### Use the formula bar

You can integrate your AI Builder key phrase extraction model in Power Apps Studio by using the formula bar. More information: [Use formulas for text AI models](use-model.md#use-formulas-for-text-ai-models)

## Use in Power Automate

If you want to use this prebuilt model in Power Automate, you can find more information in [Use the key phrase extraction prebuilt model in Power Automate](flow-key-phrase-extraction.md).
 
## Supported language and data format

- Documents can't exceed 5,120 characters.
- For information about language support, see [Text Analytics API v3 language support](https://docs.microsoft.com/azure/cognitive-services/text-analytics/language-support?tabs=key-phrase-extraction).

## Model output

If text is detected, the key phrase extraction model outputs the following information:

- **Results**: A list of phrases from the document
- **Phrase**: Strings denoting the key talking points in the document text
